# HTML
  是一种文本语言带有特殊标签
## HTML骨架格式
```html
<html> #根标签 #<>标签 标记
  <head> #头标签
     <title>我的第一个网页</title> #标题标签（网页标题）
  </head>
  <body>
  这是我的第一个页面！！
  </body> #主体标签
</html>
```
## HTML标签分类
1. 双标签
```html
<body>#标签开始
</body>#标签结束 /关闭符号
```
2. 单标签
```html
<br /> 、<hr />、<img />、<base />、<input />#单标签 数量非常少
```


## HTML标签关系

1. 嵌套关系
```HTML
<head> #头标签
    <title>我的第一个网页</title> #标题标签（网页标题）
</head>
```
2. 并列关系
```html
<head> #头标签
    <title>我的第一个网页</title> #标题标签（网页标题）</head>
<body>
这是我的第一个页面！！
</body> #主体标签
```
##### Sublime快速生成介绍
```html
<!DOCTYPE html>
<html lang='en'>
<head>
	<meta charset="UTF-8">
	<title></title>
</head>
<body>
</body>
</html>
```

* **!**或者**html:5**或**html+Tab**快速生成框架
* 输入html+Tab键 #如果不成功需要ctrl+shift+p install package 输入emmet选择下载==但是我还没有成功==
* **```<!DOCTYPE html>```**#告诉我们这个是哪一个版本的html，我们目前使用的是HTML5的版本

* UTF-8目前最常用的字符集编码方式，常用的编码方式还有GBK和GB2312。

  * GB2312 简体中文 包含6763个汉字

  	* BIG5 繁体中文 港澳台等用
  	* GBK 包含全部中文字符 是GB2312的扩展，加入繁体字的支持，兼容GB2312
  	* UTF-8 则包含全世界所有国家需要用到的字符
## HTML标签属性
```html
1.<标签名 属性1='属性1' 属性2='属性2'...>内容</标签名>
2.<br/>#这个是表示强制换行break
3.<hr width='500'color="red"/>如下：
```
<hr width='666' color="red"/>
```html
4.段落标签：<p>我是一个段落标签</p>段落标签文字之间分的比较开br较小
```
## HTML图像标签
1. 基本图像插入方式
```html
<img width='300'src="D:\学习\Markdown笔记\pictures\sb.png"/>如下：
```
<img  width='300' src="D:\学习\Markdown笔记\pictures\sb.png"/>

2. 带有alt的图像
```html
<img src="D:\学习\Markdown笔记\pictures\sb1.png"/>如下：
```
<img  src="D:\学习\Markdown笔记\pictures\sb1.png"/>

我如果对应文件夹里面没有这张图片，它就裂开了
此时此刻，我们可以用到提示文本，替换该图片防止出现裂开体验感不好的情况。

```html
<img src="D:\学习\Markdown笔记\pictures\sb1.png" alt="这是我的一个小logo"/>如下：
```
<img src="D:\学习\Markdown笔记\pictures\sb1.png" alt="这是我的一个小logo"/>

3.带有title的图像

```html
<img width='300'src="D:\学习\Markdown笔记\pictures\sb.png" title="wlq的logo" alt="这是我的一个小logo"/>如下：
```
<img width='300' src="D:\学习\Markdown笔记\pictures\sb.png" title="wlq的logo" />

可以尝试一下将您的鼠标移过这张图片，你会神奇的发现它有文字讲述。pps.上一张图片就没有哦

4.带有宽或者高的图像
```html
<img width/heigh='300'src="D:\学习\Markdown笔记\pictures\sb.png" title="wlq的logo" alt="这是我的一个小logo"/>  ##emmmm其实在上面嫌太丑就已经改了宽度，一般情况下宽和高就改一个，因为都改要考虑比例问题。
```
5.带有边框的图像**border**

```html
<img width='300'src="D:\学习\Markdown笔记\pictures\sb.png" title="wlq的logo" boder='10' alt="这是我的一个小logo"/>如下：
```
<img width='300' src="D:\学习\Markdown笔记\pictures\sb.png" title="wlq的logo" border="10" alt="这是我的一个小logo"/>
可能因为我的是透明png所以没有边框我来换一张。
<img width='100' src="D:\学习\Markdown笔记\pictures\touxiang.jpg" border="10"/>
尝试失败但是在网页中用此方法打开是正确的，如下：
<img width='100' src="D:\学习\Markdown笔记\pictures\border.png" border="10"/>

看来不是png透明的问题。

## HTML链接标签（重点）
单词缩写：anchor的缩写。基本解释锚，铁锚的。
HTML中创建超链接，标签环绕被链接的对象
```html
<a href="跳转目标" target="目标窗口的弹出方式">文本或图像</a>
```
*  href：用于指定链接目标url地址，当为标签应用href属性时，它具有了超链接的功能。Hypertext Reference的缩写。意思是超文本引用
* target：用于指定链接页面的打开方式，其取值有self和blank两种，其中self为默认值，**blank为在新窗口中打开方式**。
1. 外部链接 需要添加http:// 协议
<a href="http://www.baidu.com">百度</a>
2. 内部链接（本地链接）
<a href="htmldemo.html">demo</a>
3. 如果当没有确定连接目标时，通常将链接标签的href属性值定义为“#”（即href="#"）,表示该链接暂时为一个空链接。
4. 不仅可以创建文本超链接，在网页中各种网页元素，如图像、表格、音频、视频等都可以添加超链接。

## HTML锚点定位（难点）
```html
<a href="#text" id="mulu" >文本或图像</a>
<h3 id="text" href="#mulu">文本</h3>
```
这两条语句时间了定位跳转并可以返回到目录

## HTML的base标签

```html
<!DOCTYPE html>
<html lang='en'>
<head>
	<meta charset="UTF-8">
    <base target="_blank">这个可以使网页中所有链接都在新窗口打开，如果有需要在当前网页打开的则在该链接后单独设置target为self即可。
	<title></title>
</head>
<body>
</body>
</html>
```

## HTML的特殊字符

<img width='500' src="D:\学习\Markdown笔记\pictures\特殊字符.png" border="10"/>

## HTML注释标签

用<!--吧啦吧啦的-->表示

## 路径（难点、重点）
* 相对路径

1. 图像文件和HTML文件位于同一文件夹：只需输入图像文件名称即可，即如
```html
<img src="logo.gif">
```
2. 图像文件位于HTML文件位于下一级文件夹，之间用“/”隔开
```html
<img src="images/logo.gif">#它的下一级
```
3. 图像文件位于HTML文件位于上一级文件夹，之间加入“../隔一级一个”
```html
<img src="../logo.gif">#它的下一级
```
* 绝对路径
 类似这种D:\学习\Markdown笔记\pictures\sb.png(不提倡因为换台电脑就不行了)，但是应该用网络的完整地址例如：

 https://i0.hdslb.com/bfs/sycp/creative_img/202008/a0603b9d65781241f78c4cea82827b8f.jpg

## 列表标签
列表最大的特点：使网页整洁整齐有序
#### 无序列表（**重点**）
```html
<ul>  #用其包裹各列，<ul>标签里只能放<li>里标签（随兼容但不提倡）
  <li></li> #前面默认生成小点，但是可以边方框这与css有关
  <li></li>
  ...
<ul/>
```
#### 有序列表（了解）
```html
<ol>  #用其包裹各列，<ol>标签里只能放<li>里标签（随兼容但不提倡）
  <li></li> #根据<li>顺序默认排序，但是可以边方框这与css有关
  <li></li>
  ...
<ol/>
```
#### 自定义列表
```html
<dl> 
  <dt></dt>
  <dd></dd> #多个<dd>对<dt>来解释说明
  <dd></dd> #最好一个<dt>一组<dd>
  <dd></dd>
  ...
<ol/>
```
## 表格table
```html
<table width="500" height="300" border="1"> 
  <tr><!--是行-->
  <td>姓名</td> 
  <td>性别</td> 
  <td>年龄</td>
  </tr>
  <tr><!--是行-->
  <td>姓名</td> 
  <td>性别</td> 
  <td>年龄</td>
  </tr>
  <tr><!--是行-->
  <td>姓名</td> 
  <td>性别</td> 
  <td>年龄</td>
  </tr>
  ...
</table>
```
<table width="200" height="200" border="1" align="left"> 
  <tr><!--是行-->
  	<td>姓名</td> 
  	<td>性别</td> 
  	<td>年龄</td>
  </tr>
  <tr><!--是行-->
  	<td>姓名</td> 
  	<td>性别</td> 
  	<td>年龄</td>
  </tr>
  <tr><!--是行-->
  	<td>姓名</td> 
  	<td>性别</td> 
  	<td>年龄</td>
  </tr>
</table>
#### 表格属性
<img width='500' src="D:/学习/Markdown笔记/pictures/表格属性.png"/>
#### 表头标签
```html
<table width="200" height="200" border="1" align="left"> 
  <tr><!--是行-->
  	<th>姓名</th> 
  	<th>性别</th> 
  	<th>年龄</th>
  </tr>
  <tr><!--是行-->
  	<td>姓名</td> 
  	<td>性别</td> 
  	<td>年龄</td>
  </tr>
  <tr><!--是行-->
  	<td>姓名</td> 
  	<td>性别</td> 
  	<td>年龄</td>
  </tr>
</table>
```
<table width="200" height="200" border="1" align="left"> 
  <tr><!--是行-->
  	<th>姓名</th> 
  	<th>性别</th> 
  	<th>年龄</th>
  </tr>
  <tr><!--是行-->
  	<td>姓名</td> 
  	<td>性别</td> 
  	<td>年龄</td>
  </tr>
  <tr><!--是行-->
  	<td>姓名</td> 
  	<td>性别</td> 
  	<td>年龄</td>
  </tr>
</table>
#### 表格结构
```html
<table width="200" height="200" border="1" align="left"> 
  <thead>
 	 <tr><!--是行-->
  		<th>姓名</th> 
  		<th>性别</th> 
  		<th>年龄</th>
 	 </tr>
  </thead>
  <tbody>
 	 <tr><!--是行-->
        <td>姓名</td> 
  		<td>性别</td> 
  		<td>年龄</td>
  	</tr>
  	<tr><!--是行-->
        <td>姓名</td> 
  		<td>性别</td> 
  		<td>年龄</td>
 	 </tr>
  </tbody>
</table>
```
<table width="200" height="200" border="1" align="left"> 
  <thead>
 	 <tr><!--是行-->
  		<th>姓名</th> 
  		<th>性别</th> 
  		<th>年龄</th>
 	 </tr>
  </thead>
  <tbody>
 	 <tr><!--是行-->
        <td>姓名</td> 
  		<td>性别</td> 
  		<td>年龄</td>
  	</tr>
  	<tr><!--是行-->
        <td>姓名</td> 
  		<td>性别</td> 
  		<td>年龄</td>
 	 </tr>
  </tbody>
</table>
#### 表格标题标签
```html
<table width="200" height="200" border="1" align="left"> 
  <caption>人员名称</caption>
  <thead>
 	 <tr><!--是行-->
  		<th>姓名</th> 
  		<th>性别</th> 
  		<th>年龄</th>
 	 </tr>
  </thead>
  <tbody>
 	 <tr><!--是行-->
        <td>姓名</td> 
  		<td>性别</td> 
  		<td>年龄</td>
  	</tr>
  	<tr><!--是行-->
        <td>姓名</td> 
  		<td>性别</td> 
  		<td>年龄</td>
 	 </tr>
  </tbody>
</table>
```
<table width="200" height="200" border="1" align="left"> 
  <caption>人员名称</caption>
  <thead>
 	 <tr><!--是行-->
  		<th>姓名</th> 
  		<th>性别</th> 
  		<th>年龄</th>
 	 </tr>
  </thead>
  <tbody>
 	 <tr><!--是行-->
        <td>姓名</td> 
  		<td>性别</td> 
  		<td>年龄</td>
  	</tr>
  	<tr><!--是行-->
        <td>姓名</td> 
  		<td>性别</td> 
  		<td>年龄</td>
 	 </tr>
  </tbody>
</table>
#### 合并单元格（**难点**）

合并顺序：向上后下，先左后右；删除个数：要合并的单元格数-1

1. 跨行合并 
* 添加rowspan="合的行数"
* 删除对应合的行（跨<tr>块删）
<table width="200" height="200" border="1" align="left"> 
  <caption>人员名称</caption>
  <thead>
 	 <tr><!--是行-->
  		<th>姓名</th> 
  		<th>性别</th> 
  		<th>年龄</th>
 	 </tr>
  </thead>
  <tbody>
 	 <tr><!--是行-->
        <td>姓名</td> 
  		<td>性别</td> 
  		<td rowspan="2" >年龄</td>
  	</tr>
  	<tr><!--是行-->
        <td>姓名</td> 
  		<td>性别</td> 
 	 </tr>
  </tbody>
</table>
2. 跨列合并
* 添加colspan="合的列数"
* 删除对应合的列（不跨<tr>块删）
<table width="200" height="200" border="1" align="left"> 
  <caption>人员名称</caption>
  <thead>
 	 <tr><!--是行-->
  		<th>姓名</th> 
  		<th>性别</th> 
  		<th>年龄</th>
 	 </tr>
  </thead>
  <tbody>
 	 <tr><!--是行-->
        <td>姓名</td> 
  		<td colspan="2" >年龄</td>
  	</tr>
  	<tr><!--是行-->
        <td>姓名</td> 
  		<td>性别</td>
        <td>年龄</td>
 	 </tr>
  </tbody>
</table>
## 表单控件
<img width='500' src="D:/学习/Markdown笔记/pictures/INPUT控件.png"/>
#### 文本框密码框
```html
用户名：<input type="text" /><br />
密码：<input type="password" /><br />
```
#### 单选框复选框
```html
* 单选框
性别：<input type="radio" name="sex"/>女<input type="radio" name="sex"/>男<br />
<!--如果是单选我们用一组相同的name值来实现-->
* 复选框
爱好：<input type="checkbook" name="hobby" />足球<input type="radio" name="hobby" />篮球<br />
<!--复选框可以同时选多个-->
```
==注==：CTRL+/快速注释

#### 默认选中表单中选项
```html
性别：<input type="radio" name="sex" checked="checked" />女<input type="radio" name="sex"/>男<br />
爱好：<input type="checkbox" name="hobby" />足球<input type="checkbox" name="hobby" />篮球<input type="checkbox" name="hobby" />乒乓球<br />
```
#### INPUT按钮组
```html
搜索：<input type="button" value="搜索啥"/> <br/>
<input type="submit" value="提交表单"/> 
<input type="reset" value="重置表单"/> <br/>
<input type="image" src="D:/学习/Markdown笔记/pictures/touxiang.jpg"/> <br/>
上传文件：
<input type="file" /> <br/>
```
#### 最多字符数和文本值
```html
用户名：<input type="text" value="用户名" /><br />
密码：<input type="password" maxlength="6" /><br />
```
#### label标签
1. 用label直接包裹input
2. label里有多个表单，向定位到某个 可以通过for id的格式来进行
```html
<label> 输入账号：<input type="text" /><br />
<!--用label直接包裹input，点击文字光标会进入文本框，用户体验感好-->
<label for="two"> 输入账号：<input type="text" /> <input type="text" id="two" /><br />
```
#### textarea控件（文本域）
```htm
留言板：
<textarea>请输入留言</textarea>l
<!--这里面的文字到框的边界可以自动换行，但是文本框不能实现自动换行-->
```
#### 下拉菜单
1. ```<select> 里还少包含一个<option></option>```
2. 缺省表单显示第一个，可以用selected改为后面的显示
```html
籍贯：
<select>
	<option>点击选择你的籍贯</option>
	<!--原本默认第一个，但是可以用selected修改，如星星-->
	<option>北京</option>
	<option>上海</option>
	<option>广州</option>
	<option selected="selected">星星</option>
</select>
```
#### 表单域
* action后台提交表单的地方
* method
* name
```html
<form action="XXX.php" method="post/get" name="userMessage">
</form>
```
## HTML5新标签和特性
和之前的版本的HTML不一样的框架
#### 常用新标签
标签字典：http://w3school.com
1. ```<nav></nav>```定义导航栏
2. ```<footer></footer>```定义网页页脚
3. ```<article></article>```定义文章
4. ```<section></section>```定义区域
5. ```<aside></aside>```定义侧边块
##### datalist标签
```html
<input type="text" value="输入明星" list="star"/>
<!--input 里面用list-->
<!--datalist 里面用id来实现input链接-->
<datalist id="star">
	<option>刘德华</option>
	<option>刘若英</option>
	<option>郭富城</option>
	<option>周杰伦</option>
</datalist>
```
##### fieldset标签
<fieldset>
	<legend>用户登录</legend>#标题
	用户名：<input type="text" /><br/>
	密码：<input type="password"/>
</fieldset>
## HTML5新增input表单
#### 交互输入框、时间
```html
<fieldset>
	<legend>HTML5新增的input type类型  那些表单</legend>
	邮箱：<input type="email" /><!--aa@aa.com--><br/>
	手机：<input type="tel" /><!--手机号格式 数字--><br/>
	数字：<input type="number" /><!--只能是 数字--><br/>
	网址：<input type="url" /><!--只能是 网址--><br/>
	搜索：<input type="search" /><!--搜索框，后面多一个全删的--><br/>
	区域：<input type="range" /><!--它是个区域的 滑块--><br/>
	颜色：<input type="color" /><!--获得颜色--><br/>
	<hr />
	时间：<input type="time" /><!--小时 分钟--><br/>
	年月日：<input type="date" /><!--获得年月日--><br/>
	月份：<input type="month" /><!--获得年月--><br/>
	星期：<input type="week" /><!--获得周--><br/>
	<input type="submit"/>
</fieldset>
```
#### 常用新属性
<img width='500' src="D:/学习/Markdown笔记/pictures/新属性.png"/>
1. 占位符（**placeholder**）
```html
用户名：<input type="text" placeholder="请输入用户名" /><br />
<!--和value不同，value的值真实存在，再输入需要删除，而占位符不用只起提示作用（灰色的）-->
```
2. 自动获得焦点（光标）(**autofocus**)
进网页光标会直接在搜索框内
```html
用户名：<input type="text" placeholder="请输入用户名"  autofocus /><br />
<!--直接写autofocus或者写autofocus="autofocus"都可-->
```
3. 多文件上传(**multiple**)
```html
上传文件：
<input type="file" multiple /> <br/>
<!--直接写multiple或者写multiple="multiple"都可-->
```
4. 输入时自动记录(**autocomplete**)
* 记录之前录入过内容，如输入过1234，当下次输入1时会提示1234
* autocomplete 首先需要提交按钮
* 这个表单必须给它名字
* 写autocomplete其实其缺省值为autocomplete="on",还可以写为autocomplete="off"即更加安全，不会显示
5. 不能为空的必填项（**required**）
6. 使元素获得焦点（**accesskey**）
* 即快捷键alt+字母，光标自动聚焦搜索框
```html
<form action="">
姓名：<input type="text" autocomplete name="username"/>
<input type="submit">
昵称：<input type="text" required accesskey="s"/>
</form>
```
## 多媒体标签
* embed标签定义嵌入的内容
* audio：播放音频
* video：播放视频
1.多媒体embed
embed可以用来插入各种各样多媒体，格式可以是Midi、Wav、AIFF、AU、MP3等等。url为音频或者视频文件及其路径，可以是相对路径或绝对路径。
2. HTML5的音频播放audio
* autoplay 自动播放
* controls 是否显示默认播放控件
* loop循环播放 loop=2就是循环播放两次 写loop或者loop="-1"就是无限循环
```html
<audio src="sound.mp3" autoplay="autoplay" controls loop="2"/></audio>
```
* 为了浏览器兼容，我们可以同时做
```html
<audio src="sound.mp3" autoplay controls />
    <source src="bgsound.mp3"/>
    <source src="bgsound.ogg"/>
    <source src="bgsound.Wav"/>
    <!--其实这三个就基本全部兼容了，但是你只有一种或两种格式的情况下你可以写下面这句话hhh-->
    您的浏览器不支持播放声音
</audio>
```
3. HTML5的音频播放audio
* autoplay 自动播放
* controls 是否显示默认播放控件
* loop循环播放 loop=2就是循环播放两次 写loop或者loop="-1"就是无限循环
* width 设置播放窗口高度
* height设置播放窗口的高度
* 兼容性格式同audio
```html
<video src="sound.mp3" autoplay controls width="800"></video>
```
