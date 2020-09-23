# CSS-2
## Emmet语法
### 快速生成HTML结构语法
1. **生成标签**直接输入标签名 按tab即可 比如div然后tab键，就可以生成```<div></div>```
2. 如果想要生成多个相同的标签，加上*就可以了，比如div*3就可以快速生成3个div
3. 如果有父子关系标签，可以用>比如ul>li就可以
4. 如果有兄弟关系的标签，就用+比如div+p
5. 如果生成带有类名或者id名字的，直接写.demo或者#two tab键就可以，默认生成```<div class="demo">```或```<div id="two">```，如果希望是别的标签可以写成p.demo,p#two,以及ul>li#two.
6. 如果生成的div类名是有顺序的，可以用 自增符号$
7. 如果想要标签内部写内容可以用div{abcdef} tab生成
### 快速生成CSS样式语法
CSS基本采取简写形式即可
1. 比如tac=text-align: center;、w=width、h=height、w100=width: 100px;
### 快速格式化代码
1. 右键格式化文档
2. 想保存时就可以自动格式化，则：1.文件-首选项-设置-a.搜索format 
b.文本编辑器-勾选(editorOnType 和 editorOnSave)
## CSS复合选择器
复合选择器建立在上个CSS-1中色调基础选择器之上，对基本选择器进行组合形成的。
### 后代选择器（重要）
后代选择器又称为包含选择器，可以选择父元素里面的子元素。其写法就是把外层标签写在前面，内层标签写在后面，中间用空格分隔。当标签发生嵌套时，内层标签就成为外层标签的后代。
```html
ol li{
    color: pink;
}
有相同的ul可以
.nav li a {

}
元素1 元素2 {样式声明}
```
* 元素1 和元素2中间用<font color="yellow">空格</font>隔开
* 元素1是父级，元素2是子级 ，最终选择的是元素2
* 元素2可以是儿子，也可以是孙子等等，只要是元素1的后代即可
* 元素1和元素2可以是任意基础选择器
### 子选择器（重要）、
子元素选择器（子选择器）只能选择作为某元素的最近一级子元素。简单理解就是选亲儿子元素。（如果是后代选择器他会把同名的子子孙孙都改变）
```html
元素1>元素2 {样式声明}
选择元素1里面的所有直接后代（子元素）元素2
div>p{
    color: pink;
}
```
### 并集选择器（重要）
并集选择器可以选择多组标签，同时为他们定义相同的样式。通常用于集体声明。并集选择器是通过英文（，）连接而成，任何形式的选择器都可以作为并集选择器的一部分
```
div,
p,
.pig li {
	color: pink;
}
/*约定的语法，冰机选择器一般竖着写*/
```
### 伪类选择器
* 伪类选择器用于向某些选择器添加特殊效果，比如给链接添加特殊小股票，或选择第1个，第n个元素。
* 伪类选择器书写最大的特点是用冒号（:）表示，比如:hover,:first-child.
* 伪类选择器很多，比如有链接伪类、结构伪类等。
#### 链接伪类选择器
| 形式    | 作用 |
| ------- | ---- |
| a:link |  选择所有未被访问的链接    |
| a:visited | 选择所有已被访问的链接 |
| <font color="yellow">a:hover</font> | 选择鼠标指针位于其上的链接 |
| a:active | 选择活动链接（鼠标按下未弹起的链接） |
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>利用选择器画三个盒子</title>
    <style>
    a:link {
    	color: #333;
    	text-decoration:none;
	}
	a:visited {
    	color: orange;
	}
	a:hover {
    	color: blue;
	}
	a:active  {
    	color: green;
	}
    </style>
</head>
<body>
   <a href="#">小猪佩奇</a>
</body>
</html>
```
<font color="yellow">注意：</font>
1. 为了确保生效，请按照<font color="red">LVHA</font>的顺序进行声明：:link、:visited、:hover、:active。
2. 记忆法：love hate 或者lv包包hao
3. 因为a链接在浏览器中具有默认样式，所以我们在实际共奏中需要给链接单独制定样式。
#### focus伪类选择器
**:focus伪类选择器**用于获得焦点的表单元素
焦点就是光标，一般情况<input>类表单才能获取，因此这个选择器也主要针对于表单元素来说。
```html
input:focus {
	background-color:yellow;
}
<input type="text"><input type="text"><input type="text">
```
例如上面有有三个输入框，focus的效果就是，光标点到哪个就哪个变颜色。
## CSS的元素显示模式（重点）
元素的显示模式就是元素（标签）以什么方式进行显示，比如```<div>```自己占一行，比如一行可以放多个```<span>```
HTML元素一般分为块元素和行元素两种类型
### 块元素
常见的块元素有```<h1> <h6> <p> <div> <ul> <li>```等，其中```<div>```标签是最典型的块元素。
**块元素的特点：**
1. 比较霸道，自己独占一行
2. 高度，宽度、外边距以及内边距又可以控制
3. 宽度默认是荣威（父级宽度）的100%
4. 是一个容器及盒子，里面可以放行内或块级元素
<font color="yellow">注意：</font>
* 文字类的元素内不能使用块级元素
* ==```<p>```标签主要用于存放文字，因此其内不能放块级元素，特别是不能放```<div>```==
* 同理，```<h1>~<h6>```等都是文字块级标签，里面也不能放其他块级元素。
### 行内元素
```<span>```是最典型的行内元素，也有的地方成为内联元素
**行内元素的特点**
1. 相邻行内元素在一行上，一行可以显示多个。
2. 高、宽直接设置是无效的。
3. 默认宽度就是它本身内容的宽度。
4. 行内元素只能容纳文本或其他行内元素，不允许放块元素。
<font color="yellow">注意：</font>
* 链接里面不能再放链接
* 特视情况链接`<a>`里面可以放块级元素，但是给`<a>`转换一下模式最安全
### 行内块元素
在行内元素中有几个特殊的标签——```<img/>、<input/>、<td>```，它们同时具有块元素和行内元素的特点。
有些资料称它们为行内块元素。
行内块元素有以下的特点：

1. 和相邻行内元素（行内块）在一行上，但是之间会有空白间隙，一行可以显示多个（**行内元素特点**）
2. 默认宽度就是它本身内容的宽度（**行内元素特点**）
3. 高度、行高、外边距以及内边距都可以控制（**块级元素特点**）
### 元素显示模式转换
特殊情况下，我们需要元素模式转换，简单理解：一个模式的元素需要另外一种模式的特性，比如想要增加链接<a>的触发范围。
* 转化为块元素：display:block
* 转化为行内块元素：display:inline
* 转化为行内块元素：display:inline-block
### 小技巧 单行文字垂直居中
CSS没有提供文字==垂直居中==的代码，这里使用一个小技巧。
* 解决方案：让文字的行高等于盒子的高度 就可以让文字在当前盒子内垂直居中
* 垂直居中的原理：行高=上空隙+文字本身高度+下空隙
## CSS的背景
### 背景颜色
backgroud-color：颜色值；
* transparent:背景颜色透明（默认就是这个）
### 背景图片
background-image属性描述了元素的背景图像。实际开发常见于logo或者一些装饰性的小图片或者是超大的背景图片，优点是非常便于控制位置。（精灵图也是一种运用场景）
background-image: none/url(url);
url(images/logo.jpg)
### 背景平铺
如果需要在HTML页面上对图像进行平铺：
* 背景图片默认是平铺的，即：background-repeat：repeat；
* 还有：background-repeat：repeat-x、background-repeat:repeat-y;
* 不平铺：background-repeat：no-repeat；
==注：==背景元素既可以添加背景颜色也可以添加背景图片，但是背景图片会盖住背景颜色
### 背景图片位置
利用background-position属性可以改变图片在背景中的位置。
background-position：x，y；
参数代表的意思是：x坐标和y坐标。可以使用方位名词或者精确单位。

|参数值|说明|
|---|---|
|length|百分数 由浮点数字和单位标识符组成的长度值|
|position|top center bottom left center right 方位名词|
eg.background-position：center right；=background-position：right，center；表示是一样的因为right一定是水平方向。
1. 参数是方位名词
* 如果指定的两个值都是方位名词，则两个值前后顺序无关，比如left top和top left效果一致
* 如果指定了一个方位名词，另一个忽略值，则第二个默认居中对齐
2. 参数是精确单位
* 如果参数值是精确坐标，那么第一个肯定是x坐标，第二个一定是y坐标
* 如果至指定一个数值，那么数值一定是x坐标，另一个默认垂直居中
3. 参数是混合单位
* 入火指定的两个值是精确单位和方位名词呼和使用，则第一个是x坐标、第二个值是y坐标。
### 背景图像固定（背景附着）
background-attachment属性设置背景图像是否固定或者随着页面的其余部分滚动。
background-attachment后期可以制作视差滚动的效果。
```background-attachment:scroll | fixed```
* fixed 背景固定
* scroll 背景图像是随着对象内容滚动（默认也是这样）
### **背景复合写法**
可以将这些属性合并简写在同一个属性background中。用空格隔开
```background: black url(images/bacground.jpg) no-repeat fixed top```
### 背景色半透明、
CSS3为我们提供了半透明的效果。
```background：rgba(0,0,0,0.3);```
* rgb: 就是红绿蓝
* a是alpha透明度，取值范围在0~1之间。
* 我们习惯吧0.3的0省略掉，写为background：rgba(0,0,0,.3)
* 注意：背景半透明是指盒子背景半透明，盒子里面的内容不受影响。
* CSS3新增属性，是IE9+版本浏览器才支持的。
* 但是现在实际开发，我们不太关注兼容性写法了，可以放心使用。
