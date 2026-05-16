<?php
// 连接本地lyb.db数据库
$db = new PDO('sqlite:lyb.db');
$db->exec("PRAGMA encoding='UTF-8'");

// 后台登录账号密码
$admin_user = "admin";
$admin_pwd = "123456";
session_start();

// 登录验证逻辑
if(isset($_POST['login'])){
    $user = $_POST['user'];
    $pwd = $_POST['pwd'];
    if($user==$admin_user && $pwd==$admin_pwd){
        $_SESSION['admin_ok'] = 1;
        header('Location:admin.php');
        exit;
    }else{
        $err = "账号或密码错误";
    }
}

// 退出登录
if(isset($_GET['out'])){
    session_destroy();
    header('Location:admin.php');
    exit;
}

// 删除留言功能
if(isset($_GET['del'])){
    $id = (int)$_GET['del'];
    $db->exec("DELETE FROM liuyan WHERE id=$id");
    header('Location:admin.php');
    exit;
}

// 未登录显示登录界面
if(empty($_SESSION['admin_ok'])){
?>
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>后台登录</title>
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{background:#f5f7fa;padding:15px;}
.box{max-width:450px;margin:50px auto;background:#fff;padding:25px;border-radius:12px;}
h3{text-align:center;margin-bottom:20px;color:#333;}
.inp{width:100%;padding:12px;margin:10px 0;border:1px solid #ddd;border-radius:8px;}
.btn{width:100%;padding:12px;background:linear-gradient(135deg,#e64340,#ff7875);color:#fff;border:none;border-radius:8px;font-size:16px;}
.err{color:red;text-align:center;margin:10px 0;}
.back{text-align:center;margin-top:15px;}
.back a{color:#409eff;text-decoration:none;}
</style>
</head>
<body>
<div class="box">
    <h3>留言板后台登录</h3>
    <?php if(isset($err))echo "<div class='err'>$err</div>"; ?>
    <form method="post">
        <input class="inp" type="text" name="user" placeholder="管理员账号" required>
        <input class="inp" type="password" name="pwd" placeholder="登录密码" required>
        <button class="btn" name="login" type="submit">立即登录</button>
    </form>
    <div class="back"><a href="index.php">返回留言首页</a></div>
</div>
</body>
</html>
<?php
exit;
}

// 已登录 显示管理页面
$all_ly = $db->query("SELECT * FROM liuyan ORDER BY id DESC")->fetchAll(PDO::FETCH_ASSOC);
?>
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>留言后台管理</title>
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{background:#f5f7fa;padding:15px;}
.manage{max-width:600px;margin:0 auto;background:#fff;padding:20px;border-radius:12px;}
.top{display:flex;justify-content:space-between;align-items:center;margin-bottom:20px;}
h3{color:#333;}
.tc{color:#e64340;text-decoration:none;}
.ly_item{padding:15px;border-bottom:1px solid #eee;margin-bottom:10px;border-radius:8px;background:#fafafa;}
.del{display:inline-block;margin-top:8px;padding:5px 12px;background:#f56c6c;color:#fff;text-decoration:none;border-radius:4px;font-size:13px;}
.empty{text-align:center;padding:30px;color:#999;}
</style>
</head>
<body>
<div class="manage">
    <div class="top">
        <h3>留言数据管理中心</h3>
        <a class="tc" href="?out=1">退出登录</a>
    </div>

    <?php if(empty($all_ly)){ ?>
    <div class="empty">暂无任何留言数据</div>
    <?php }else{ ?>
        <?php foreach($all_ly as $ly){ ?>
        <div class="ly_item">
            <p>昵称：<?php echo $ly['username'] ?></p>
            <p>时间：<?php echo $ly['addtime'] ?></p>
            <p>内容：<?php echo $ly['content'] ?></p>
            <a class="del" href="?del=<?php echo $ly['id'] ?>" onclick="return confirm('确定删除这条留言吗？')">删除留言</a>
        </div>
        <?php } ?>
    <?php } ?>
</div>
</body>
</html>