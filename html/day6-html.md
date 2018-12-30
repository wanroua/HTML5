#### 颜色半透明(CSS3)

```bash
color:rgba(0,0,0,0.5),a是alpha透明的意思，取值范围0~1之间
```

#### 文章阴影(CSS3)

```bash
text-shadow：水平位置、垂直位置、模糊距离、阴影颜色、
#前两项是必须写的，后两项可以选写
实例：
p {
    text-shadow: 10px 2px 3px rgba(0,0,0,0.5)
    #10px:水平，2px:垂直   3px:模糊距离     rgba：颜色和模糊度(0.5模糊度)
}
```

| 值       | 描述                           |
| -------- | ------------------------------ |
| h-shadow | 必须，水平阴影的位置。允许负值 |
| v-shadow | 必须。垂直阴影的位置。允许负值 |
| blur     | 可选。模糊的距离               |
| color    | 可选。阴影的颜色。             |



#### 内部样式表

```bash
内嵌式是将CSS代码集中写在HTML文档的head头部标签中，并启用style标签定义，其基本语法格式如下：
<head>
<style type="text/css">
选择器 {属性1：属性值1}
<style>
</head>
语法中，style标签一般位于head标签中title标签之后，也可以把他放在HTML文档的任何地方。
type="text/CSS"在html5中可以省略，写上也比较符合规范，所有这个地方也可以写也可以忽略
```



#### 行内式(内联样式)

```bash
内联样式，又有人称行内样式、行间样式、内嵌样式。是通过标签的style属性来设置元素的样式，其基本语法格式如下：
<标签名 styple="属性1：属性值1">内容</标签名>
```



#### 外部样式表(外联式)

```bash
链入式是将所有的样式放在一个或多个以.css为扩展名的外部样式表文件中，通过link标签将外部样式表文件链接到HTML文档中，其基本语法格式如下：
<head>
<link href="CSS文件的路径"  type="text/css" rel="styleshenet">
</head>

#注意：link是但标签
该语法中，link标签需要放在head头部标签中，并且必须制定link标签的三个属性，具体如下：
-href:定义所连接外部样式表文件的URL，可以是相对路径，也可以是绝对路径
-type:定义所连接文档的类型，在这里需要制定为"text/css"，表示连接的外部文件为CSS样式表
-rel:定义当前文档与被连接文档之间的关系，在这里需要指定为"stylesheet",表示被连接的文档是一个样式表文件
```



#### 总结(三种样式表)

| 样式表     | 优点                     | 缺点                     | 使用情况       | 控制范围         |
| ---------- | ------------------------ | ------------------------ | -------------- | ---------------- |
| 行内样式表 | 书写方便，权重高         | 没有实现样式和结构相分高 | 较少           | 控制一个标签(少) |
| 内嵌样式表 | 部分结构和样式相分离     | 没有彻底分离             | 较多           | 控制一个页面(中) |
| 外部样式表 | 完全实现结构和样式相分离 | 需要引入                 | 最躲，强烈推荐 | 控制整个站点(多) |



#### 外部样式表实例

```html
	<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<link rel="stylesheet" href="1.css">
</head>
<body>
	<p class="d">1111</p>
	
</body>
</html>
#index.html

1.css 
.d {
color:red;
}
```

#### 行内元素(inline-level)

```abash
常见的行内元素有<a>、<strong>、<b>、<em>、<i>、<del>、<s>、<ins>、<u>、<span>等，其中<span>标签最典型的行内元素
```

#### 块级元素和行内元素区别

```bash
块级元素的特点：
1、总是从新行开始
2、高度，行高、外边距以及内距都可以控制
3、宽度默认是容器的100%
4、可以容纳内联元素和其他快元素

行内元素的特点：
1、和相邻行内元素在一行上
2、高、宽无效，但水平方向的padding和margin可以设置，垂直方向无效
3、默认宽度就是它本身内容的宽度
```



#### 行内快元素(inline-block)

```bash
在行内元素中有几个特殊的标签:img 、input、td,可以对它们设置宽高和对齐属性，有些资料可能会称它们为行内块元素

行内块元素的特点：
1、和相邻行内元素(行内快)，在一行上，但是之间会有空白缝隙
2、默认宽度就是它本身内容的宽度
3、高度、行高、外边距以及内边距都可以控制
```

#### 转换实例：

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		div {
	background: #3c3c3c;   /*由块转成行*/
	width: 30px;
	height: 40px;
	display: inline;
}

span {
	background: #7b7b7b;  /*由行转成块*/
	width: 40px;
	height: 50px;
	display: block;
}

a {
	background: #888;     /*转成行内块*/
	width: 30px;
	height: 20px;
	display: inline-block;
}
	</style>
</head>
<body>
	<div>123</div>
	<div>456</div>
	<div>789</div>
	<span>abc</span>
	<span>edg</span>
	<span>sdk</span>
	<a href="">123</a>
	<a href="">456</a>
	
</body>
</html>

#display：转换
```

