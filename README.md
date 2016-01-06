###countdown.html
```html
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>js倒计时功能</title>
	<style>
		.content1{
			width: 700px;
			height: 100px;
			background: #0088cc;
			margin: 0 auto;
			margin-top: 50px;
			text-align: center;
			line-height: 100px;
			font-size: 40px;
			color: #fff;
			border-radius: 50px;
			border-bottom: solid 1px #09f;
			box-shadow: 0px 10px 0px #0088aa;
		}
	</style>
</head>
<body>

	<div class="content1">
		<div id="show"></div>
	</div>
	
	<script>
		window.onload=function(){
		
			time();

	
		}

		function time(){
			var mydate=new Date();
			var year=mydate.getFullYear();
			var month=mydate.getMonth()+1;
			var date=mydate.getDate();
			
			var week;
			var day=mydate.getDay();
			switch(day){
			case 0:week="星期日";break;
			case 1:week="星期一";break;
			case 2:week="星期二";break;
			case 3:week="星期三";break;
			case 4:week="星期四";break;
			case 5:week="星期五";break;
			case 6:week="星期六";break;
			}
			//默认输出星期的格式是0~6，通过switch循环转化输出格式，用变量week保存
			
			var hour=mydate.getHours();
			if(hour<10){
				hour='0'+hour;
			}
			//当hour<10，hour前面追加0

			var minute=mydate.getMinutes();
			if(minute<10){
				minute='0'+minute;
			}
			//当minute<10，minute前面追加0
			
			var second=mydate.getSeconds();
			if(second<10){
				second='0'+second;
			
			}
			//当second<10，second前面追加0
			document.getElementById("show").innerHTML=year+'年'+month+'月'+date+'日 '+week+' '+hour+':'+minute+':'+second
			
			setTimeout(time,500);
			//setTimeout函数。每隔500毫秒执行time一次
		}
	</script>
</body>
</html>
```

###效果图
![Alt text](./tu.png)
