<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>魔方/立方体</title>
		<style type="text/css">
			body{
				perspective: 1000px;	/* 透视眼 */
			}
			.cube{
				width:200px;
				height: 200px;
				margin:200px auto;
				position:relative;	/* 相对定位*/
				
				/* 设置transform-style:保留子元素3D效果 */
				transform-style: preserve-3d;
				transform: rotate3d(1,1,1,0deg);
				transition: all 5s;
			}
			.cube:hover{
				transform:rotate3d(1,1,1,720deg);
			}
			.page{
				width:200px;
				height: 200px;
				position: absolute;	/* 绝对定位 */
				left:0;
				top:0;
				/* 设定透明的 */
				opacity: 0.6;
			}
			
			.front{
				background-image:url(img/lisa1.jpg);
				background-size: 100% auto;
				transform: translateZ(100px);
			}
			.back{
				background-image:url(img/lisa2.jpg);
				background-size: 100% auto;
				transform: translateZ(-100px);
			}
			.right{
				background-image:url(img/lisa3.jpg);
				background-size: 100% auto;
				transform: rotateY(90deg) translateZ(100px);
			}
			.left{
				background-image:url(img/lisa4.jpg);
				background-size: 100% auto;
				transform: rotateY(-90deg) translateZ(100px);
			}
			.top{
				background-image:url(img/lisa5.jpg);
				background-size: 100% auto;
				transform: rotateX(90deg) translateZ(100px);
			}
			.bottom{
				background-image:url(img/lisa6.jpg);
				background-size: 100% auto;
				transform: rotateX(-90deg) translateZ(100px);
			}
			
		</style>
	</head>
	<body>
		<div class="cube">
			<div class="page front"></div>
			<div class="page back"></div>
			<div class="page left"></div>
			<div class="page right"></div>
			<div class="page top"></div>
			<div class="page bottom"></div>
		</div>
	</body>
</html>
