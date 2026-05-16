<?php
// 连接本地SQLite数据库 文件名为lyb.db
$db = new PDO('sqlite:lyb.db');
// 设置数据库编码
$db->exec("PRAGMA encoding='UTF-8'");

// 自动创建留言数据表 不存在则新建
$createSql = "CREATE TABLE IF NOT EXISTS liuyan(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    username TEXT NOT NULL,
    content TEXT NOT NULL,
    addtime TEXT NOT NULL
)";
$db->exec($createSql);

// 接收提交留言数据
if($_POST){
    $name = trim($_POST['name']);
    $msg = trim($_POST['msg']);
    $time = date('Y-m-d H:i:s');
    if(!empty($name) && !empty($msg)){
        // 插入留言语句
        $ins = $db->prepare("INSERT INTO liuyan(username,content,addtime) VALUES(?,?,?)");
        $ins->execute([$name,$msg,$time]);
        header('Location:index.php');
        exit;
    }
}

// 查询所有留言 倒序最新在前
$list = $db->query("SELECT * FROM liuyan ORDER BY id DESC")->fetchAll(PDO::FETCH_ASSOC);
?>
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<!-- 手机端适配标签 -->
<meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1.0,user-scalable=no">
<title>手机留言板</title>
<style>
/* 全局样式 手机居中美化 */
*{margin:0;padding:0;box-sizing:border-box;font-family:"微软雅黑",sans-serif;}
body{background:#f5f7fa;padding:15px;}
/* 主容器居中 限制手机宽度 */
.main{max-width:500px;margin:0 auto;background:#fff;border-radius:12px;padding:20px;box-shadow:0 2px 10px #eee;}
h2{text-align:center;color:#333;margin-bottom:20px;font-size:18px;}
/* 输入框样式 */
.inp{width:100%;padding:12px;border:1px solid #ddd;border-radius:8px;margin-bottom:12px;font-size:15px;}
textarea{height:100px;resize:none;}
/* 提交按钮渐变美化 */
.btn{width:100%;padding:12px;background:linear-gradient(135deg,#409eff,#67c23a);color:#fff;border:none;border-radius:8px;font-size:16px;}
/* 留言列表样式 */
.liuy_list{margin-top:25px;}
.item{padding:15px;border-bottom:1px solid #f0f0f0;margin-bottom:10px;border-radius:8px;background:#fafafa;}
.name{color:#409eff;font-weight:bold;margin-bottom:5px;}
.time{font-size:12px;color:#999;margin:5px 0;}
.content{color:#555;line-height:1.6;}
/* 后台入口 */
.admin_in{text-align:center;margin-top:15px;}
.admin_in a{color:#e64340;text-decoration:none;}
</style>
</head>
<body>
<div class="main">
    <h2>在线留言板</h2>
    <!-- 留言提交表单 -->
    <form method="post">
        <input class="inp" type="text" name="name" placeholder="请输入你的昵称" required>
        <textarea class="inp" name="msg" placeholder="请输入留言内容" required></textarea>
        <button class="btn" type="submit">提交留言</button>
    </form>

    <!-- 留言展示区域 -->
    <div class="liuy_list">
        <?php if(empty($list)){ ?>
        <p style="text-align:center;color:#999;padding:20px;">暂无留言，快来抢沙发吧~</p>
        <?php }else{ ?>
            <?php foreach($list as $v){ ?>
            <div class="item">
                <div class="name">昵称：<?php echo $v['username'] ?></div>
                <div class="time">时间：<?php echo $v['addtime'] ?></div>
                <div class="content"><?php echo $v['content'] ?></div>
            </div>
            <?php } ?>
        <?php } ?>
    </div>

    <div class="admin_in">
        <a href="admin.php">进入后台管理</a>
    </div>
</div>
</body>
</html>