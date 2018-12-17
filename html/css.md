### `如何使用CSS`

```bash
内联样式，实例：
<h1 style="color:red";font-size:40px;>abc</h1>
#在标签内部设置css样式，颜色为红色，字体大小为40px

内部样式表，实例：
<head>
	<style type="text/css" media="screen">
		h1 {
            color:blue;
		}
		#针对<body>标签下的h1进行css配色
</head>
<body>
	<h1>abc</h1>
</body>



外联样式,实例：
在当前目录下创建css目录，然后创建结尾为.css的文件
<head>
	<link rel="stylesheet" href="./css/style.css">
	#href：指定css文件路径
</head>
<body>
	<h2>abc</h2>
</body>

vim style.css
h2 {
    color:red;
}
```

### `使用标签的class来定义颜色`

```bash
<head>
<style type="text/css"  media="screen">
	.class1 {
        color:red;
	}
	#在head的style中调用body中h1标签中class的值，以".class1"名称来调用
	.class2 {
        color:rgb(255,0,0);
	}
	.class3 {
        color:#00ff00;
	}
</style>
</head>

<body>
	<h1 class="class1">这是一个段落</h1>
	<h1 class="class2">这是一个段落</h1>
	<h1  class="class3">这是一个段落</h1>
</body>
```

### `backgroud背景颜色`

```bash
<head>
	<style media="screen">
	body{
	background-color: #FF0000;
	#背景颜色
	background:url(./cloth.png)
	#背景颜色，指定图片
	background-repeat:no-repeat/repeat(默认)
	#控制图片的拼接方式,repeat：重复拼接 ,repeat-y:y轴 ，repeat-x：x轴
	backgroud-position: 50% 50%  left  center;
	#控制图片的位置，可以设置一个参数或者两个参数
	background-attachment: fixed;  #图片固定
	#简写方式：
	background: #FF0000 url(./1.jpg) no-repeat
	}
	</style>
</head>
<body></body>
```

### `padding:属性设置元素的内边框`

```bash
实例：
<style>
border:1px  solid blue;  #border:边框， solid:边框颜色
padding:50px  #所有四个边的padding都是50px
</style>
```



