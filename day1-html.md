 ### `标签`

#### `sublime插件`

```bash
View In Browser #右键直接游览器打开
ChineseLocalizations #中文，汉化
ConvertToUTF8 #自动把文件编码方式转换为UTF-8
Emmet  #能快速编写HTML、CSS文件
SublimeCodeintel #代码提示插件
SidebarEnhancements #侧边栏插件，让侧边栏功能更丰富
markdownEditing #markdown,ctrl+b
```





```bash
<!DOCTYPE html>   :文档声明#这是Html5的声明，html比这复杂点
<html>			  :表示文档开始
<head>			  :head标签存放文档的基本信息，不可见元素
<meta   charset="uft-8"> : 声明字符编码
#utf-8：是目前最常用的字符集编码方式，常用的字符集编码方式还有gbk和gb2312
#gb2312简单中文，包括6763
#BIG5：繁体中文港澳台等用
#GBK：包含全部中文字符，是GB2312的扩展，加入对繁体字的支持，兼容GB2312
#UTF-8:则包含全世界所有国家需要用到的字符 
<title></titile>  :声明文档标题
</head>           : html标签都是有开始有结束
<body>			  : 标签存放文档可见内容
</html>			  :表示文档结束
<!-- ab -->		  :注释	
#meta都写在head头部
<meta http-equiv="X-UA-Compatible" content="IE=edge"> #支持ie
<meta name="viewport" content="device-width, inital-scale=1.0"> #宽度等于设备的宽度，手机访问时等于手机的宽度，1：不缩放，2：缩放  小于1：缩小

<h1> :1级标题，有1-6，共6级，每级字体一次变小
<p>  :段落标签
<hr /> :水平线标签
<br /> :换行
<a href="url" target="_self/blank"> ：超链接，target:默认是_self,在当前页面跳转，blank:新的窗口
<img src="图片地址"  alt="文字类容(当图片无法加载或者网络出现问题时显示的文字内容)"  width="宽度" height="高度">
<ul><li></li></ul> :ul：无序列表，li:填写内容(li中可嵌套)
<ol><li></li></ol> :ol:有序列表，前面有数字(li中可嵌套)
<em></em> :斜体字
<strong></strong>: 高亮黑体
<strike></strike> :删除线
<label></label>: 点击时会自动到当前输入框 
<input text="email" placeholde="这是虚拟提示">  #placeholde：虚拟提示
<textarea></textarea> :大方框，可以自定义拉大

<select>
	<option>1</option>
	<option>2</option>
	<option>3</option>
</select>
#下拉框，1、2、3是值


<input type="radio" name="color"/> 红色
<input type="radio"  name="color"/> 蓝色
#radio，按钮，需要设置相同的name值，不然是多选

<input type="checkbox" name="dog"/> 狗
<input type="checkbox" name="cat"/> 猫
#checkbox:多选框


<a name="top"/>
<a href="#top">
#定义name为top，下面的<a href="#top">点击会跳到最上面
```



#### `文本格式化标签`

```bash
<b> </b> 、<strong></strong>:文本以粗体方式显示(XHTML推荐使用strong)
<i></i>、<em></em>:文字以斜体方式显示(XHTML推荐使用em)
<s></s>、<del></del>:文字以加删除线方式显示(XHTML推荐使用del)
<u></u>、<ins></ins>:文字以加下划线方式显示(XHTML不赞成使用u)
```



### `<img /> :属性`

| 属性   | 属性值                       | 描述                     |
| ------ | ---------------------------- | ------------------------ |
| src    | URL                          | 图像路径                 |
| alt    | 文本                         | 图像不能显示时的替换文本 |
| title  | 文本                         | 鼠标悬停时显示的内容     |
| width  | 像素(XHTML不支持%页面百分比) | 设置图像的宽度           |
| height | 像素(XHTML不支持%页面百分比) | 设置图形的高度           |
| border | 数字                         | 设置图形边框的宽度       |



#### `链接标签`

```bash
在html中创建超链接非常简单，只需要用标签环绕需要被链接的对象即可，其基本语法格式如下：
<a href="跳转目标" target="目标窗口的弹出方式">文本或图像</a>

1、href:用于指定链接目标的url地址，当为标签应用href属性时，它就具有了超链接的功能
2、target:用于指定链接页面的打开方式，其取值有_self_和_blank两种，其中_seif为默认值，_blank为在新窗口中打开方式。

注意：
1、外部链接，需要添加http://www.baidu.com
2、内部链接，直接连接内部页面名称即可，比如<a href="index.html">首页</a>
3、如果当时没有确定链接目标时，通常将该链接标签的href属性值定义为"#(即href="#")"，表示该链接为一个空连接
4、不仅可以创建文本超链接，在网页中各种网页元素，如图像、表格、音频、视频等都可以添加超链接

```



#### `锚点定位(难点)`

```bash
1、通过创建锚点链接，用户能够快读定位到目标内容，创建锚点链接分为两步：
2、使用"<a href="#id名">"链接文本</a>“创建链接文本
3、使用响应的id名标注跳转目标的位置 

实例：
<a href="#jl"><p>经历</p></a>
<a href="pl"><p>评论</p></a>


<p id="jl">某某某经历</p>
<p id="pl">某某某经历</p>
```



#### `base标签`

```bash
主要用于超链接批量设置为：如：_self(默认。当前页面)和_blank(新窗口)
设置如下：需在head标签中
<head>
	<base target="_blank">
</head>
```



#### `特殊字符标签的理解`

| 特殊字符 | 描述     | 字符的代码 |
| -------- | -------- | ---------- |
|          | 空格符   | & nbsp;    |
| <        | 小于号   | &lt;       |
| >        | 大于号   | &gt;       |
| &        | 和号     | &amp       |
| ©        | 版权     | &cpoy;     |
| ®        | 注册商标 | & reg;     |
| ℃        | 摄氏度   | & deg;     |
| ±        | 正负号   | & plusmn;  |
| &times;  | 乘号     | & times;   |
| &divide; | 除号     | & divide;  |
| &sup2;   | 平方2    | & sup2;    |
| &sup3;   | 平方3    | & sup3;    |



#### `注释标签`

```bash
在html中还有一种特殊的标签----注释标签，如果需要在HTML文档中添加一些便于阅读和理解但又不需要叙事在页面中的注释文字，就需要使用注释标签，其基本语法格式如下：
<!--  内容 -->

ctrl +  / 单行注释  shift +  / 多行注释
```



#### `无序列表ul(重点)和有序列表ol`

```bash
无序列表的各个列表之间没有顺序级别之分，是并列的，其基本语法格式如下：
<ul>
	<li>电话</li>
	<li>电脑</li>
	<li>手机</li>
</ul>

有序列表：
<ol>
	<li>电话</li>
	<li>电脑</li>
	<li>手机</li>
</ol>

#需注意：
1、<ul></ul>中只能嵌套<li></li>，之间在<ul></ul>标签中输入其他标签或者文字的做法是不被允许的。
2、<li>与</li>之间相当于一个容器，可以容纳所有元素
3、无序列表会带有自己样式属性，放下那个样式，一会让css来
```



#### `自定义列表(理解)`

```bash
定义列表常用语对术语或名词进行解释和描述，定义列表的列表项前没有任何项目符号，其基本语法如下：
<dl>
	<dt>名词1</dt> #最前面
	<dd>名词2</dd> #在dt后面排列  
	<dd>名词3</dd>
</dl>
```



#### `创建表格`

```bash
在html网页中，要想创建表哥，就需要使用表格相关的标签。创建表格的基本语法格式如下：
<table>
	<tr>
		<td><td>
		<td><td>
		<td><td>
	</tr>
</table>
#在上面的语法中包含三对HTML标签，分别为 table</table、tr</tr、td</td，他们是创建表格的基本标签，缺一不可，下面对他们进行具体地解释

1.table用于定义一个表格。

2.tr 用于定义表格中的一行，必须嵌套在 table标签中，在 table中包含几对 tr，就有几行表格。

3.td /td：用于定义表格中的单元格，必须嵌套在<tr></tr>标签中，一对 <tr> </tr>中包含几对<td></td>，就表示该行中有多少列（或多少个单元格）。

<table>
			
			<tr>
				<td>你好</td>
				<td>我好</td>
				<td>他好</td>
			</tr>
				<tr>
				<td>你好</td>
				<td>我好</td>
				<td>他好</td>
			</tr>
		</table>
注意：
1. <tr></tr>中只能嵌套<td></td>
2. <td></td>标签，他就像一个容器，可以容纳所有的元素
```



#### `表格的属性`

| 属性名      | 含义                                                       | 常用属性值          |
| ----------- | ---------------------------------------------------------- | ------------------- |
| border      | 设置表格的边框(默认border="0"无边框)                       | 像素值              |
| cellspacing | 设置单元格与单元格边框之间的空白间距(方框之间距离)         | 像素值(默认为2像素) |
| cellpadding | 设置单元格内容与单元格边框之间的空白间距（字体与边框距离） | 像素值(默认为1像素) |
| widht       | 设置表格的宽度                                             | 像素值              |
| Height      | 设置表格的高度                                             | 像素值              |
| align       | 设置表格在网页中的水平对齐方式                             | Left、center、right |



#### `表头标签`

```bash
表头一般位于表格的第一行或第一列，其文本加粗居中，如下图所示，即为设置了表头表格。设置表头非常简单，只需要表头标记<th></th>替代相应的单元格标记<td></td>即可
实例：
<table>
<thead> #头部
	<tr>
	<th>姓名</th>
	<th>性别</th>
	<th>年纪</th>
	</tr>
	#th：只需在表格开头写即可,字体会加粗居中
<thead>
<tbody> #内容
	<tr>
	<td>one</td>
	<td>man</td>
	<td>23</td>
	</tr>
	
	<tr>
	<td>two</td>
	<td>man</td>
	<td>22</td>
	</tr>
</tbody>
</table>
```



#### `表格标题`

```bash
表格的标题，caption
定义和用法：
caption元素定义表格标题：
<table>
	<caption>我是表格标题</caption>
</table>
#注意：caption标签必须随table标签之后，只能对每个表格定义一个标题，通常这个标题会被居中与表格之上
```





#### `合并单元格`

```bash
跨行合并：rowspan，跨列合并：colspan 
#注意:合并下面的表格需要删除当前对应的行数据
```





#### `Input控件`

```bash
在上面的语法中，<input />标签为单标签，type属性为其最基本的属性，其取值有多种，用于指定不同的控件类型。除了type属性之外，<input />标签还可以定义很多其他的属性，其常用属性如下表所示:

属性			属性值			描述
type		 text		    单行文本输入框
			 password		密码输入框
			 radio			单选按钮
			 checkbox		复选框
			 button			普通按钮
			 submit			提交按钮
			 reset			重置按钮
			 image			图像形式的按钮
			 file			文件域
name		由用户自定义		控件名称
value		由用户自定义		input控件中的默认文本值
size		正整数			  input控件中的默认文本值
checked	    checked			定义选择控件默认被选中的项
maxlength	正整数			  控件允许输入的最多字符数
```

