<html>
<head>
<meta charset="utf-8"> 
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>

    <script src="jquery-3.2.1.min.js"></script>
    <style>
    </style>
</head>
<body>
<div style="width:250px;height:150px;background-color:#ff6600;">小图</div>
<div style="position:fixed;top:0px;left:0px;height:100%;width:100%;overflow:hidden;background-color:rgba(0,0,0,0.5);display:none;">
    <div style="width:500px;height:300px;background-color:#ff6600;position:fixed;top:50%;left:50%;margin-left:-250px;margin-top:-150px">
        大图
    </div>
</div>
</body>
</html>
<script>
$(document).ready(function(){
    $("div").eq(0).click(function(){
        $("div").eq(1).show();
    });
    $("div").eq(1).click(function(){
       $(this).hide();
    });
})
</script>
