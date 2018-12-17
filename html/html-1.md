 ### `标签`

```bash
<!DOCTYPE html>   :文档声明#这是Html5的声明，html比这复杂点
<html>			  :表示文档开始
<head>			  :head标签存放文档的基本信息，不可见元素
<meta   charset="uft-8"> : 声明字符编码
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
<a href="url" target="_self/blank"> ：超链接，target:默认是_self,在当前页面跳转，blank:新的窗口
<img src="图片地址"  alt="文字类容(当图片无法加载或者网络出现问题时显示的文字内容)"  width="宽度" height="高度">
<ul><li></li></ul> :ul：无序列表，li:填写内容(li中可嵌套)
<ol><li></li></ol> :ol:有序列表，前面有数字(li中可嵌套)

<table> :表格
<tr> :里面写内容需加别的标签
<td> :标准单元，包含数据
<th> :表头单元，包含头部信息
#注意，若td和th数据不对称会显示空白。(th和td都是在tr标签里面)
<caption> :表单标题，默认居中
<table border="1"> :border="1"边线
如：
__________________________________
<table  border="1">
		<tr>
			<td>a</td>
			<td>b</td>
			<td>c</td>
		</tr>
		<tr>
			<th>w</th>
			<th>z</th>
		
		</tr>
	</table>
__________________________________

```

### `表单的使用`

```bash
<table  border="1"> #border:以表格的方式显示
	<caption>表单标题</caption>  #caption:表单标题，会居中
	<tr>
		<td  colspan="2">1</td>
		<td>2</td>  // colspan，横向合并，需删除这一行
		<td>3</td>
	</tr>
	
	<tr>
		<td  rowspan="2">4</td>  
		<td>5</td>
		<td>6</td>
	</tr>
	
	<tr>
		<td>7</td>   //rowspen:纵向合并，需删除此行
		<td>8</td>  
		<td>9</td>
	</tr>
</table>

#table是表单格式，tr:里面是表单内容，td：标准单元，包含数据   th:表头表单，会高亮显示

```

### `form标签`

```bash
简单格式：
<form>
	<label  for="userName"  >用户名</label>
	#for：表示关联某个ID的值，当点击用户名时光标会自动跳到方框中
	#label：会在最前面显示字符串用户名
	<input id="userName" type="text"  name="username"   placeholder="用户名"  value="">
	#id:设置个唯一的id为userName
	#type:类型是文本类型，有多种类。
    #name:中的值会跟后端服务器交互
	#placeholder="用户名"：会在文本框显示用户名字符串，虚拟显示，光标点上去消失
	#value：文本框中默认的值，真是显示，需要删除
	
</form>



类型：
<form>
		<label for="userName">用户名</label>
		
		<input id="userName" type="text" name="username" placeholder="用户名" value="">
		<br>
		<label for="password">密码</label>
		<input type="password" name="password" value="">
		<br>
		<input type="radio" name="sex" value="">男
		<input type="radio" name="sex" value="">女
		<br>
		<input type="checkbox"  name="coclor"  value="">红
		<input type="checkbox"  name="coclor"  value="">蓝
		<input type="checkbox"  name="coclor"  value="">黄
		<input type="checkbox"  name="coclor"  value="">黑
		<br>
		<input type="button" name="" value="提交">
	</form>
#type:
#password:密码
#radio:单选项，需name值相同，不然都可以选择
#checkbox:多选项
#button:提交按钮
```

### `下拉列表`

```bash
<select>
    <option  value=""></option> #默认空  
    <option value="1">上海</option> #value:默认数字排序
	<option selected value="2">北京</option>  #默认显示北京
	<option value="3">广东</option>
</select>
```

### `提交按钮`

```bash
form表单中：
<form>
	<input type="text" name="name"  value="">
    <button type="button">按钮</button>
	<button type="submit">提交</button>
	<button type="reset">重置</button>
	#重置会重置输入框中内容
</form>

在input中
<input type="button" name="" value="按钮">
<input type="submit" name=""  value="提交">
<input type="reset" name=""  value="重置">


```

