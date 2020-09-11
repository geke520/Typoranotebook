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
<br /> 、<hr />、<img />、<base />#单标签 数量非常少
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

* **```<!DOCTYPE html>```**#告诉我们这个是哪一个版本的html，我们目前使用的是HTML5的版本

* UTF-8目前最常用的字符集编码方式，常用的编码方式还有GBK和GB2312。

  * GB2312 简体中文 包含6763个汉字

  	* BIG5 繁体中文 港澳台等用
  	* GBK 包含全部中文字符 是GB2312的扩展，加入繁体字的支持，兼容GB2312
  	* UTF-8 则包含全世界所有国家需要用到的字符
## HTML标签属性
```html
<标签名 属性1='属性1' 属性2='属性2'...>内容</标签名>
<br/>#这个是表示一行
<hr width='500'color="red"/>如下：
```
<hr width='666' color="red"/>
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
 类似这种D:\学习\Markdown笔记\pictures\sb.png(不提倡因为换台电脑就不行了)，但是应该用网络的完整地址例如：https://i0.hdslb.com/bfs/sycp/creative_img/202008/a0603b9d65781241f78c4cea82827b8f.jpg









