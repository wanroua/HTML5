#### 符合选择器

```html
复合选择器是由两个或多个基础选择器，通过不同的方式组合而成的，目的是为了可以选择更准确更精细的目标元素标签。
```

#### 1.1、交集选择器

```bash
交集选择器由两个选择器构成，其中第一个为标签选择器，第二个为class选择器，两个选择器之前不能有空格，如h3
```

![image](https://www.wanrou.io/html/jj-xzq.png)

#### 技巧记忆

```bash
交集选择器是 并且的意思，即。。。又。。的意思
比如：p.one选择的是：类名为.one的段落标签
用的相对来说比较少，不太建议使用。 
```

#### 交集选择器实例

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		.color {
			color:red;
		}
		div.color {    /* 选择标签，并指定选择器，来修改元素*/
			font-size: 20px;
		}
	</style>
</head>
<body>
		<div class="color">歌手</div>
		<div  class="color">唱歌</div>
		<p class="color">电视</p>
		<p  class="color">电影</p>
</body>
</html>
```



#### 并集选择器

```html
并集选择器(css选择器分组)是各个选择器通过“逗号”链接而成的，任何形式的选择器(包括标签选择器、class类选择器id选择器等)，都可以作为并集选择器的一部分，如果某些选择器定义的样式完全相同，或部分相同，就可以利用并集选择器为它们定义相同的CSS样式
```

![image](https://www.wanrou.io/html/bj-xzq.png)

#### 记忆技巧

```html
并集选择器 和 的意思，就是说，只要逗号隔开的，所有选择器都会执行后面的样式
```

#### 实例

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		p,div,.yao {    /*指定多个标签来定义为颜色，在em标签中定义：yao,然后调用*/
			color:yellow;
		}
	</style>
</head>
<body>
	

		<p>香蕉</p>
		<p>苹果</p>
		<div>米饭</div>
		<div>面条</div>
		<em class="yao">火腿</em>
		<em>肉</em>
</body>
</html>
```



#### 后代选择器

```bash
后台选择器又称为包含选择器，用来选择元素或元素组的后代，其写法就是把外层标签写在前面，内层标签写在后面，中间用空格分隔，当标签发生嵌套时，内层标签就称为外层标签的后代
```

![image](https://www.wanrou.io/html/hd-xzq.png)

#### 实例

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		.hd ul li {    /*调用类*/
			color:green;
		}
        div ul li {  /* 多个子级标签*/
            color:red;
        }
	</style>
</head>
<body>
	
	<div class="hd">
		<ul>
			<li>w</li>
			<li>w</li>
			<li>w</li>
		</ul>
	</div>
		<ul>
			<li>h</li>
			<li>h</li>
			<li>h</li>
		</ul>
</body>
</html>
```



#### 子元素选择器

```bash
子元素选择器只能选择作为某元素子元素的元素，其写法就是把腹肌标签写在前面，子级标签写在后面，中间跟一个 > 进行连接，注意，符号左右两侧各保留一个空格
```

![image](https://www.wanrou.io/html/zy-xzq.png)

#### 实例

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
			.zy >li   {   /*类zy,指向下级标签，可多级指向，如：.zy > ul > li*/
				color:yellow;
			}
	</style>
</head>
<body>
		<ul class="zy">
			<li>一级菜单</li>
			<ul>
				<li>二级菜单</li>
				<ul>
					<li>三级菜单</li>
				</ul>
			</ul>
		</ul>
</html>
```



#### 题目

```bash
1、链接、登录的颜色为红色，同时主导航栏里面的所有的链接改为蓝色(简单)
2、主导航栏和侧导航栏里面都是14像素并且是微软雅黑(中等)
3、主导航里面的一级菜单链接文字颜色为绿色(难)
```

#### 代码

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		.dl a {
			color:red;
		}
		.zdh ul li a  {
			color: yellow;
		}
		.zdh , .cdh {
			font : 20px  "宋体";
		}
		.zdh > ul > li > a {
			color:green;
		}
	</style>
</head>
<body>
	
		<div class="zdh">
			<ul>
				<li><a href="#">公司首页</a></li>
				<li><a href="#">公司简介</a></li>
				<li><a href="#">公司产品</a></li>
				<li><a href="#">联系我们</a>
				<ul>
					<li><a href="#">公司邮箱</a> </li>
					<li><a href="#">公司电话</a></li>
				</ul>
				</li>
			</ul>
		</div>
	
		<div class="cdh">
			<div class="zch">左侧导航栏</div>
			<div class="dl"><a href="#">登录</a></div>
		</div>
</body>
</html>
```



#### 属性选择器

```bash
实例：
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		a[title] {      /* a标签中带有title的全部颜色设置为红色*/
			color:red;
		}
		input[type=text]{   /*指定input的类型为text都变为红色*/
			color:red;
		}
	</style>
</head>
<body>
	<a href="#" title="百度" >百度</a>
	<a href="#" title="星朗" >新浪</a>
	<a href="#" >头疼</a>
	<input type="text"   value="ww">
	<input type="submit" >
	<input type="reset" >
</body>
</html>
```

#### 属性选择器(通配符)

```bash
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		div[class*=font]{     /*属性值分为： *:包含   ^:开头包含   $:结尾包含*/
			color:red;
		}
	</style>
</head>
<body>
	<div class="font32">w</div>
	<div class="font32">w</div>
	<div class="21font">w</div>
	<div class="22font">//</div>
	<div class="wfontw">zz</div>
	<div class="wfontw">zz</div>
</body>
</html>
```

#### 伪元素选择器(CSS3)

```html
E::first-letter {   #内容第一个字被设置为红色
	color:red;
}
E::first-line {
	color:red;    #内容第一行被设置为红色，仅限第一行
}
E::selection {
	color:red;   #鼠标选择的数据会显示为红色(默认蓝色)
}
#E是指定标签
实例：
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		p::first-letter{
			color:red;
		}
		p::first-line {
			color : yellow;
		}
		p::selection {
			color: green;
		}
	</style>
</head>
<body>
<p>各位网站站长将网站接入YUNDUN前，需要将YUNDUN的高防CDN节点IP段加入白名单，以免YUNDUN安全加速服务被源服务器防火墙（或安全软件）或机房防火墙误判为攻击而进行拦截，影响网站的正常访问。
各位网站站长将网站接入YUNDUN前，需要将YUNDUN的高防CDN节点IP段加入白名单，以免YUNDUN安全加速服务被源服务器防火墙（或安全软件）或机房防火墙误判为攻击而进行拦截，影响网站的正常访问</p>
</body>
</html>
```



#### 在标签内容中前面或后面增加内容

```bash
实例：
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		div::before {       /* before:前面  */
			content: "word";
		}
		div::after {        /* after:后面 */
			content: " word";
		}
	</style>
</head>
<body>
	<div>hello</div>
</body>
</html>
#输出结果为  wordhello word
```



#### CSS书写规范

```bash
空格规范：
[强制] 选择器与 {之间必须包含空格。
示例：
font-size: 12px; 
#属性的:号后面跟值

选择器规范
[强制]当一个rule包含多个selector时，每个选择器声明必须独占一行

实例：
.post,
.page,
.comment {
    line-height: 1.5;
}

[建议]：选择的嵌套层级应不大于3级，位置靠后的限定条件应尽可能精确


[强制]属性定义后必须以分号结尾
实例：
.div {
    margin: 0;
}

```



#### CSS背景(background)

| Background-color                                             | 背景颜色         |
| ------------------------------------------------------------ | ---------------- |
| Background-image                                             | 背景图片地址     |
| Background-repeat                                            | 是否平铺         |
| background-position                                          | 背景位置         |
| background-attachment                                        | 背景固定还是滚动 |
| 背景的合写(复合属性)                                         |                  |
| Background:背景颜色、背景图片地址、背景平铺、背景滚动、背景位置 |                  |

#### 背景图片(image)

