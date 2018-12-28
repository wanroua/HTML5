### css的id选择器

```bash
实例：
<html>
<head>
<style>
#id {
    color:red;
}
</style>
</head>
<body>
<p id="id">a</p>
</body>
</html>
```



#### id选择器和类选择器的区别

```bash
<html>
<head>
<style>
#id {                  //id选择器
    color:red;
}

.color { 			//clss选择器
    color:yellow;
}
</style>
</head>
<body>
<p id="id">a</p>
</body>
</html>

#类选择器：
类选择器可以在多个标签中嵌入
#id选择器
只能在一个标签中嵌入，在多个标签中嵌入会不生效(实际还是生效)
```



#### 通配符选择器

```bash
<html>
<head>
<style>
* {  			// 通配符选择器
    color:red;
}
#asd {
    color:yellow;
}
</style>
</head>
<body>
<h1>abc</h1>
<h2>efg</h2>
<h3 id="asd">sdk</h3>
</body>
</html>
#通配符选择器针对于没有设置类选择器(class)和id选择器(#id)会全部设置为通配符选择器中的配置，但如果标签已经设置了指定的选择器不会影响到
```



#### 伪类选择器

```bash
首先，这也是一个选择器，伪类选择器用于向某些选择器添加特殊的效果。比如给链接添加特殊效果，比如可以选择第1个，第n个元素。
#为了和我们刚才学的类选择器相区别，类选择器是一个点，比如 .demo{} 而我们的伪类用2个点就是冒号，如:  :link{}
```

#### 链接伪类选择器

```bash
:link /*未访问的连接的状态*/
:visited /*已访问的连接的状态*/
:hover   /*鼠标移动到连接上的状态*/
:active  /*选定的连接，选定后没点击的状态*/
#注意写的时候，他们的顺序尽量不要颠倒，按照lvha的顺序，love hate记忆法或者lv包包 非常hao，顺序不能颠倒，记忆法：l v  h a
实例：
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>
	</title>
	<style type="text/css">
		a:link{   /*未访问前显示状态*/
			color: yellow;
			font-size: 100px;
			font-weight: bold;
		}
		a:visited{   /*访问后的状态*/
			color: red;
			font-size: 100px;
			font-weight: bold;
		} 
		a:hover{   /*鼠标移动上去后的状态*/
			color: blue;
			font-size: 100px;
			font-weight: bold;
		}
		a:active{   /*选定的连接*/
			color: green;
			font-size: 100px;
			font-weight: bold;
		}

	</style>
</head>
<body>
	<a href="#">百度</a>
	<a href="#">谷歌</a>
</body>
</html>
#一般只用到link和hover状态
```



#### 结构(位置)伪类选择器(CSS3)

```bash
：first-child:选取属于其父元素的首个子元素的指定选择器
:last-child:选取属于其父元素的最后一个子元素的指定选择器
:nth-child(n):匹配属于其父元素的第N个子元素，不论元素的类型
:nth-last-child(n):选择器匹配属于其元素的第N个子元素的每个元素，不论元素的类型，从最后一个子元素开始计数，n可以是数字、关键词或公式

实例：
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style type="text/css">
		li:first-child{ /*第一个*/
			font-size: 100px;
		}
		li:last-child{  /*last,最后一个*/
			color: red;
		}
		li:nth-child(3){  /*指定第几个结构体*/
			font-weight: bold;
			color: yellow;
		}
	</style>
</head>
<body>
	<ol>
		<li>a</li>
		<li>B</li>
		<li>C</li>
		<li>d</li>
		<li>e</li>
	</ol>
	
</body>
</html>

#实例，所有的全部为红色
li:nth-child(n){
    color:red;
}
#实例，偶数行，even:偶数，odd：奇数，或者写为2:2的平方，为偶数。奇数：2+1
li:nth-child(even) {
    color:red;
}
```

#### 目标伪类选择器

```bash
:target目标伪类选择器，选择器可用于选取当前活动的目标元素
实例：
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style type="text/css">
		li:nth-child(n) {
			color:pink;
		}
		
		:target{
			color:red;
		}
		.jl {
			font-weight: bold;
			font-size: 100px;
		}
	</style>
</head>
<body>
	<ul>
		<li class="jl">a</li>
		<li>B</li>
		<li>C</li>
		<li>d</li>
		<li>e</li>
	</ul>
	<a href="#jl">jl</a>
	<a href="#sq">sq</a>
	
	<h1 id="jl">演艺经历编辑</h1>
	<p >港剧时期
1994年，古天乐正式进入TVB，在《餐餐有宋家》《啊sir早晨》《婚姻物语》
古天乐在1995年《神雕侠侣》中饰演杨过
古天乐在1995年《神雕侠侣》中饰演杨过(18张)
 等电视里跑龙套，其中，由郑伊健、陈松伶主演的《婚姻物语》是他出演的第一部电视作品。
1995年7月，古天乐签约华星唱片公司；同年，与李若彤主演的金庸武侠剧《神雕侠侣》播出，这是古天乐首次担任第一男主角，凭借剧中狂放深情亦正亦邪的杨过广受关注 [19]  。1996年2月，在郑少秋、罗嘉良主演的时装剧《天地男儿》中饰演文静而柔弱眉目俊朗又用情专一的叶承康 [20]  。
1997年7月，主演改编自古龙的古装武侠剧《圆月弯刀》，古天乐饰演气质高贵而冷漠、个性亦正亦邪的丁鹏 [21]  ；11月，主演描写美食的喜剧《美味天王》，出演大厨乔柏高 [22]  。</p></br>
<h1 id="sq">电影时期</h1>
<p>1994年，古天乐在电影《男儿当入樽》里跑龙套，这是他出演的首部电影。
部落格照片
部落格照片(40张)
 1996年，古天乐在警匪片《旺角的天空2之男烧衣》中出演一个古惑仔。
2000年8月，搭档朱茵、张家辉主演的赌片《中华赌侠》上映，饰演一手飞牌绝技名震江湖的香港赌王“阿酷” [31]  。
2001年，古天乐与中国星电影公司签定三年电影合约，离开TVB正式加入电影圈；同年10月，与刘青云、梁咏琪、刘嘉玲主演的喜剧片《绝世好Bra》上映。
2002年11月16日，古天乐在广州举行一千多名歌迷参加的“入型入格酷MENSHOW”音乐晚会 [32]  。9月，连同张柏芝主演的古装电影《河东狮吼》上映，古天乐在片中饰演风流潇洒、文质彬彬的诗人陈季常 [33]  。
2003年1月，与郑秀文、李冰冰主演杜琪峰的电影《百年好合》，饰演花花公子洪飞虎；7月，与郑秀文、刘青云合作的时装喜剧片《恋上你的床》上映 [34]  ；11月，搭档张柏芝、刘青云主演《忘不了》，饰演阿文一角。同年，与大国文化集团Music Nation唱片公司（大国文化唱片公司）签定两年歌手合约 [35]  ；5月30日，推出加盟Music Nation后首张个人专辑《Mr. Cool》（酷先生），订单即达金唱片销量 [36]  ；在CCTV—MTV音乐盛典中，同名单曲《Mr Cool》获得2003年度港台地区最受欢迎歌曲奖 [37]  。
2004年4月，主演喜剧片《</p>

</body>
</html>
```



#### CSS外观属性

```bash
color:文本颜色
color属性用于定义文本的颜色，其取值方式有如下3种
1、预定义的颜色值，如red,greeen,blue等
2、十六进制，如#FF0000，#FF6600,#29D794等，实际工作中，十六进制是最常用的定义颜色的方式
3、RGB代码，如红色可以表示rgb(255,0,0)或rgb(100%,0%,0%)
需要注意的是，如果使用RGB代码的百分比颜色值，取值为0时也不能省略百分号，必须写为0%
```



#### line-height：行间距

```bash
ine-height属性用于设置行间距，就是行与行之间的距离，即字符的垂直间距，一般称为行高。lin-height常用的属性值单位有三种，分别为像素px,相对值em和百分比%,实际工作中使用最多的是像素px
```

#### text-align:水平对齐方式

```bash
text-align属性用于设置文本内容的水平对齐，相当于html中的align对齐属性，其可用属性值如下：
left:左对齐
right:右对齐
center:居中对齐
```

#### text-indent:首行缩进

```bash
text-indent属性用于设置首行文本的缩进，其属性值可为不同单位的数组、em字符宽度的倍数、或相对于游览器窗口的百分比%,允许使用

实例：
<style>
p{
    text-indent: 2em; 
    }
</style>
<p>a</p>
```



#### letter-spacing:字间距

```bash
letter-spacing属性用于定义字间距，所谓字间距就是字符与字符之间的空白，其属性值可为不同的单位的数值，允许使用负值，默认为normal
```

#### word-spacing:单词间距

```bash
word-spacing属性用于定义英文单词之间的间距，对中文字符无效，和letter-spacing一样，其属性值可为不通单位的数值，允许使用负值，默认为normal

word-spacing和letter-spacing均可对英文进行设置。不同的是letter-spacing定义的为字母之间的间距，而word-spacing定义的为英文单词之间的间距
```



#### word-break：自动换行

