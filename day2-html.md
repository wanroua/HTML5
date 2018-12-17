### HTML5

```bash
<header>:语义：定义页面的头部，页眉</header>
<nav>:语义：定义导航栏 </nav>
<footer>:语义:定义页面底部  页脚</footer>
<article>:语义：定义文章</article>
<aside>:语义：定义其所处内容之外的内容  侧边</aside>
```

### datalist智能下拉列表

```bash
<input type-"text" value="请输入名字" list="string" />
<datalsit  id="string">
<option>yyc</option>
<option>swr</option>
<option>yxp</option>
<option>wzc</option>
<option>sj</option>
</datalsit>
效果如下图：
```

![image](https://www.wanrou.io/html/datalist.gif)

#### fieldset 元素可将表单内的相关元素分组，打包，legend搭配使用

```bash
<fieldset>
	<legend>用户登录</legend>
	用户名：<input type="text">
	密  码：<input type="text">
</fieldset>
效果如下图：
```

![image](https://www.wanrou.io/html/fieldset.gif)





#### input-new

| 类型     | 使用实例                | 含义               |
| -------- | ----------------------- | ------------------ |
| email    | <input type="email">    | 邮箱格式           |
| tel      | <input type="tel">      | 输入手机号码格式   |
| url      | <input type="url">      | 输入url格式        |
| number   | <input type="number">   | 输入数字格式       |
| search   | <input type="search">   | 搜索框(体现语义化) |
| range    | <input type="range">    | 自由拖动滑块       |
| time     | <input type="time">     | 小时分钟           |
| date     | <input type="date">     | 年月日             |
| datetime | <input type="datetime"> | 时间               |
| month    | <input type="month">    | 月年               |
| Week     | <input type="week">     | 星期 年            |



```bash
<form action="">
	邮箱： <input type="email" />  </br>  <!-- 邮箱 -->
	手机： <input type="tel" />  </br>  <!--手机，只允许输入数字 -->
	数字： <input type="number" />  </br>  <!-- 纯数字，只允许输入数字 -->
	url： <input type="url" />  </br>  <!-- 只允许输入http://www 开头的 -->
	搜索： <input type="search" />  </br>  <!-- 搜索 -->
	区域： <input type="range" />  </br>  <!-- 区域 -->
	<input type="submit" />  <!-- 提交 -->
</form>
效果如下图：
```

  ![image](http://www.wanrou.io/html/input-new.gif)





#### HTML5新增属性

| 属性         | 用法                                                  | 含义                                                         |
| ------------ | ----------------------------------------------------- | ------------------------------------------------------------ |
| placeholder  | <input type="text" placeholder="请输入用户名">        | 占位符，当用户输入的时候，里面的文字消失，删除所有文字，自动返回 |
| autofocus    | <inpt type="text" autofocus> \| autofocus="autofocus" | 规定当页面加载时input元素应该自动获得焦点                    |
| multiple     | <input type="file" multiple>                          | 多文件上传                                                   |
| autocomplete | <input type="text" autocomplete="off">                | 规定表单是否应该启用自动完成功能，有2个值，一个是On一个是off，on代表记录已经输入的值: 名字：<input type="text"  name="userName" autocomplete / ><br/>			<input type="submit"> |
| required     | <input type="text" required>                          | 必填项                                                       |
| Accesskey    | <input type="text" accesskey="s">                     | 规定激活(使元素获得焦点)元素的快捷键，采用alt + 字母的格式   |



#### 综合之前所学习的实例

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	<form action="">
		<fieldset>
			<legend>学生档案</legend>
			姓名:<input type="text" placeholder="请输入姓名" /> </br>
			手机:<input type="tal" plcaceholder="请输入手机号" /></br>
			邮箱:<input type="email" placeholder="xxx@qq.com" /></br>
			所属学院:<input type="text" placeholder="请输入所属学院" list="xy" /></br> 
			<datalist id="xy">
				<option>Linux</option>
				<option>Java</option>
				<option>Html</option>
			</datalist>
			出生日期: <input type="date" /> </br>
			成绩: <input type="number" placeholder="请输入考试成绩" /></br>
			毕业时间:<input type="date" />  
			<input type="submit" /> <input type="reset" value="重置">
		</fieldset>

	</form>
</body>
</html>
```



#### 多媒体标签

```bash
embed:标签定义嵌入的内容
audio:播放音频
video:播放视频

多媒体embed(会使用)
embed可以用来插入多种多媒体，格式可以是Midi、Wav、AIFF、AU、MP3等等。url为音频或视频文件及路径，可以是相对路径或者绝对路径。
因为兼容性问题，我们这里只讲解插入网络视频，后面H5会讲解audio和video多媒体
<embed src="//player.video.iqiyi.com/4a24e6f756dc161a9635a10bd609b93c/0/0/v_19rqsj1vvc.swf-albumId=1701248500-tvId=1701248500-isPurchase=0-cnId=undefined" allowFullScreen="true" quality="high" width="480" height="350" align="middle" allowScriptAccess="always" type="application/x-shockwave-flash"></embed>

<iframe src="http://open.iqiyi.com/developer/player_js/coopPlayerIndex.html?vid=4a24e6f756dc161a9635a10bd609b93c&tvId=1701248500&accessToken=2.f22860a2479ad60d8da7697274de9346&appKey=3955c3425820435e86d0f4cdfe56f5e7&appId=1368&height=100%&width=100%" frameborder="0" allowfullscreen="true" width="100%" height="100%"></iframe>
```



#### 多媒体标签 audio

```bash
HTML5通过<audio>标签来解决音频播放的问题
使用相当简单，如下图所示：
<audio src="./sz.mp3"></audio>

并且可以通过附加属性可以更友好控制音频的播放，如：
autoplay ：自动播放
controls ：是否显不默认播放控件
loop :循环播放，如：loop="2" ,循环播放2次，若是：-1 则无限播放

下图解决方案：
<audio controls  autoplay>
<source src="/1.mp3" />
<source src="2.ogg" />
您的游览器不支持播放
</audio>
```

![image](https://www.wanrou.io/html/audio.png)



####  多媒体标签video

```html
HTML5通过<audio>标签来解决音频播放问题
同样音频播放一样，<video>使用也相当简单，如下图
    <video src="/1.mp4"  controls="controls"> </video>
同样，通过附加属性可以更友好的控制视频的播放
autopaly : 自动播放
controls : 是否显示控件
loop     :循环播放
width    : 设置播放窗口的宽度
heigth   : 设置播放窗口的高度

下图解决方案：
<video controls  autoplay>
<source src="/1.mp3" />
<source src="2.ogg" />
    您的游览器不支持播放
</video>
```

![image](https://www.wanrou.io/html/video.png)

