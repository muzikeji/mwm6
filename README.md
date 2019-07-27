
<html>
<head>
<meta charset="utf-8"> 
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black">
<style type="text/css">
h1 { display:none; }
body {
/* 加载背景图 */
background-image: url();
/* 背景图垂直、水平均居中 */
background-position: center center;
/* 背景图不平铺 */
background-repeat: no-repeat;
/* 当内容高度大于图片高度时，背景图像的位置相对于viewport固定 */
background-attachment: fixed;
/* 让背景图基于容器大小伸缩 */
background-size: cover;
/* 设置背景颜色，背景图加载过程中会显示背景色 */
background-color: #7ba0f1;
}
	#box{
		width:340px;
		height:185px;
		border:1px solid black;
		position:relative;
		overflow:hidden;
margin:0 auto;
	}
body{ text-align:center} 
div.cd {border-radius: 10px;
border: #e9e9e9 solid 1px;
width:90%;
	height:60px;
margin:0 auto;
border-radius: 5px;
   }
div.sm {border-radius: 10px;
border: #e9e9e9 solid 1px;
width:100px;
	height:100px;
margin:0 auto;
border-radius: 50%;
   overflow:hidden;}
div.mc {border-radius: 10px;
border: #e9e9e9 solid 1px;
width:80px;
	height:20px;
margin:0 auto;
border-radius: 35px;
   overflow:hidden;}

div  img {width:100%}

	#red{
		background-image: url(https://i.loli.net/2019/07/27/5d3c170ee773143216.jpg);
		width:340px;
	}
	#green{
		background-image: url(https://i.loli.net/2019/07/27/5d3c170e622fd23976.jpg);
		width:340px;
	}
	#blue{
		background-image: url(https://i.loli.net/2019/07/27/5d3c170f4d0e255749.jpg);
		width:340px;
	}
	.slide{
		width:340px;
		height:185px;
		position:absolute;
	}

.thumbnail 
{
	float:left;
	width:110px;
	height:90px;
	margin:5px;
}
p.date {text-align: justify; color:#ffffff; font-size:14px;}
h3  {text-align: center; color:#ffffff; font-size:20px;}
h2  {text-align: center; color: #ffffff; font-size:20px;}
p.cc  {text-align: center; color:#ffffff; font-size:15px;}

a {
color: #0508b9;
text-decoration: none;
}
a:active {
text-decoration: none;
color: #001997;
}

a:link {text-decoration:none;}
a:visited {text-decoration:none;}
a:hover {text-decoration:none;}
a:active {text-decoration:none;}

	
</style>
<script type="text/javascript">
	onload=function(){
		var arr = document.getElementsByClassName("slide");
		for(var i=0;i<arr.length;i++){
			arr[i].style.left = i*340+"px";
		}
	}
	function LeftMove(){
		var arr = document.getElementsByClassName("slide");//获取三个子div
		for(var i=0;i<arr.length;i++){
			var left = parseFloat(arr[i].style.left);
			left-=2;
			var width = 340;//图片的宽度
			if(left<=-width){
				left=(arr.length-1)*width;//当图片完全走出显示框，拼接到末尾
				clearInterval(moveId);
			}
			arr[i].style.left = left+"px";
		}
	}
	function divInterval(){
		moveId=setInterval(LeftMove,10);//设置一个10毫秒定时器
	}
	
	
	timeId=setInterval(divInterval,3000);//设置一个3秒的定时器。
	
	function stop(){
		clearInterval(timeId);
	}
	function start(){
		clearInterval(timeId);
		timeId=setInterval(divInterval,3000);
	}
	
	//页面失去焦点停止
	onblur = function(){
		stop();
	}
	//页面获取焦点时开始
	onfocus = function(){
		start();
	}
</script>
</head>
<body>
<div  class="sm" style="background-color: #7fc4e5"> <img src="https://i.loli.net/2019/07/27/5d3c317ee785b81349.jpg" alt=""> </div>
<div  class="mc" style="background-color: #7fc4e5"> <p class="cc">木子科技</p></div>
	<a href="http://muzikeji.cn" target="_blank"><div id="box" onmouseover="stop()" onmouseout="start()">
		<div id="red" class="slide"></div>
		<div id="green" class="slide"></div>
		<div id="blue" class="slide"></div>
	</div></a>

</body>
</html>
