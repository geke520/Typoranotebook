# CSS-1
CSS(Casscading Style Sheets),CSS通常称为CSS样式表或层叠样式表（级联样式表），主要用于设置HTML页面中文本内容（字体、大小、对齐方式等）、通篇的外形（宽高、边框样式、边距等）以及版面的布局等外观显示样式。
### CSS简介
#### CSS语法规范
1. 属性和属性值之间需要用冒号隔开
2. 每个属性结尾一定要有分号
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>体验CSS语法规范</title>
    <style>
        /* 选择器{样式}*/
        /* 给谁改样式{改什么样式}*/
        p {
            color: red;  
            /* 一定要有分号分隔 */
            font-size: 12px;
        }
    </style>
</head>
<body>
   <p>有点意思</p>
</body>
</html>
```
#### CSS代码风格
1. 建议用展开式书写风格，清晰一行一个属性
2. 虽然兼容大小写，但是建议小写
3. 属性名冒号后要留一个空格
4. 选择器（标签）后和大括号之间留一个空格
### CSS基础选择器
#### 选择器分类
分为基础选择器和复合选择器两大类
##### 标签选择器
选同一类所有标签，所以不能差异化

##### **类**选择器
1. 可以单独选一个，或某几个
2. 样式点定义（后面的类名，自起但是不能是原定义名称如div） 结构类调用
3. 类名可以长一点color-box
4. 有一个命名规则
[在这里](https://blog.csdn.net/wang414300980/article/details/79758008)
```html
.red{ 
   color: red;
}
<div class="red">我要变红色</div>
```
###### 用div画盒子
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>利用选择器画三个盒子</title>
    <style>
        .red {
            width: 100px;
            height:100px;
            background-color: red;  
        }
        .green {
            width: 100px;
            height:100px;
            background-color: green;  
        }
    </style>
</head>
<body>
   <div class="red">红色</div>
   <div class="green">绿色</div>
   <div class="red">红色</div>
</body>
</html>
```
###### 多类名的使用方式
```html
       .box {
            width: 100px;
            height:100px;
        }
       .red{ 
            color: red;
        }
       .green {
            background-color: green;  
        }
    </style>
</head>
<body>
   <div class="red box">红色</div>
   <div class="green box">绿色</div>
   <div class="red box">红色</div>
</body>
```
##### id选择器
* 样式#号定义，结构id调用，只能调用一次，别人切勿调用
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>id选择器</title>
    <style>
        # pink{
            color="pink";
        }
    </style>
</head>
<body>
   <div id="pink">红色</div>
</body>
</html>
```
* **id选择器和类选择器的区别**
1. 类选择器（class）好比人的名字，一个人，可以有多个名字。同时一个名字可以被多个人使用
2. id选择器好比人的身份证号码，全中国唯一的，不得重复。
3. id选择器和类选择器最大的不同在于使用次数上。
4. 类选择器在修改样式中用的多，id选择器一般用于页面唯一性的元素，经常和JavaScriot搭配使用。
##### 通配符选择器
* 在CSS中，通配符选择器使用"*"定义，它表示选取页面中所有元素（标签）。
语法:
```
* {
    属性1：属性值1；
    ···
}
```
* 通配符选择器不需要调用，自动就给所有的元素使用样式。

### CSS字体属性
#### 字体系列
1. 可以同时写多个字体，各个字体之间必须使用英文状态下的逗号隔开
2. 一般情况下，如果有空格的多个单词组成的字体，加引号(单引号双引号均可)（就是看你电脑上装了没有）
3. 尽量使用系统默认的字体
4. 最常见的几个字体：body{font-family:'Microsoft YaHei',tahoma,'Hiraino Sans GB'}
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>id选择器</title>
    <style>
        h2 {
            font-family='Microsoft YaHei',;
        }
        h2 {
            font-family="微软雅黑";
        }
    </style>
</head>
<body>
   <h2>啦啦</h2>
   <p>天上飘来啦啦</p>
</body>
</html>
```
#### 字体大小
CSS使用font-size属性定义字体大小
```
p {
    font-size： 20px；
}
```
* px（像素）大小是我们网页的最常用的单位
* 不同浏览器可能默认显示的字号大小不一致，我们尽量给一个明确值大小，不要默认大小
* 可以给body制定整个页面文字的大小(标题比较特殊，任需要单独拎出来设置大小)
#### 字体加粗
1. ```<b></b>```
2. ```<strong></strong>```
3. 
```html
.bold {
	font-weight: bold;/*等价于font-weight=700注意这里不加单位，实际开发中用数字比较多400就是原字体或normal*/
}
<p class="bold">
```
#### 字体样式
斜体：
1. ```<em></em>或者<i></i>```
但是这个方法我们可以让它正过来
em {
	font-style=normal;
}
2. 
```html
p{
	font-style:italic;
}
```
#### 字体复合属性
* font：font-style font-weight font-size/line-height font-famliy
* 不可以颠倒顺序
* 各个属性之间空格隔开
* 但是 必须有文字大小font-size和字体font-family
### CSS文本属性
#### 文本颜色
1. 预定义的颜色值red，green等
2. 十六进制#ff0000
3. RGB代码，红绿蓝rgb（255,0,0）
```
div{
color: red;
/*color : #ff0000; #加留个十六进制数，简洁方式，选中#和这串数字然后双击可以出现选色器*/
/*color: rgb(255,0,0)红绿蓝的提取 */
}
```
#### 对齐文本
text-align属性用于设置元素内文本内容==水平对齐方式==
1.left(左对齐）默认
2.right右对齐
3.center居中
```
div {
	text-align: center;
}
```
#### 装饰文本
text-decoration属性规定添加文本的修饰。可以给文本添加下划线、删除线、上划线等。
1. none默认。没有和装饰线（最常用）
2. underline下划线。链接a自带下划线（常用）
3. overline上划线。（几乎不用）
4. line-through删除线（不常用）
```
div{
	text-decoration: underline;
}
取消下划线：
（因为a都带有）
a {
	text-decoration: none;
	color: #333;
}
```
#### 文本缩进
text-indent文本缩进只能缩进第一行
div {
	text-indent: 20px;/*indent译为缩进*/
}
段落可以缩进一个指定的数值，也可以是负值。
**相对缩进单位**
em是一个相对单位，就是当前元素（font-size）1个文字的大小，如果当前元素没有设置大小，则会按照父元素的1个文字大小。
p {
	text-indent: 2em;
}
#### 行间距
line-height属性用于设置行间的距离（行高）上间距、文字高度和下间距。可以控制文字与行之间的距离。
```
div {
	line-height: 26px;
}
```
### CSS的引入方式
#### 三种样式表
按照CSS样式的书写位置（或者引入的方式），CSS样式表可以分为三大类：
1. 行内样式表（行内式）
2. 内部样式表（嵌入式）
3. 外部样式表（链接式）
#### 内部样式表
1.内部样式表示写到html页面内部，是将CSS代码抽取出来全部放在```<style>```标签内
* ``` <style>```标签理论上可以放在HTML文档的任何地方，但一般会放在文档的```<head>```标签中
* 通过此种方式，可以方便控制当前整个页面中的元素样式位置
* 代码结构清晰，但是并没有实现结构与样式完全分离（还放在HTML页面里）
#### 行内样式表
行内样式表（内联样式表）是在元素标签内部的style属性中设定CSS样式。适合于修改简单样式。
```<div style="color: red; font-size: 12px;">青春不常在  抓紧谈恋爱</div>```
* style其实就是标签的属性
* 在双引号中间，写法要符合CSS规范
* 可以控制当前的标签设置样式
* 由于书写繁琐，并且没有体现结构与样式相分离的思想，所以不推荐大量使用，只有对当前元素添加简单样式的时候，可以考虑使用。
#### 外部样式表
实际开发都是外部样式表，适用于样式比较多的情况。核心是：样式单独写到CSS文件中，之后吧CSS文件引入到HTML页面中使用。
引入外部样式表分为两步：
1. 信件一个后缀名为.css的文件样式文件，把所有css代码都放入此文件中。

2. 在HTML页面中，使用```<link>```标签引入这个文件
    ```<link rel="stylesheet" href="css文件路径">```
### Chrome 调试工具
* ctrl+0可以复原浏览器大小
* 点击元素，发现右侧没有仰视引入，极有可能是类名或者样式引入错误
* 如果有样式，但样式前面有黄色叹号提示，则是样式属性书写错误

