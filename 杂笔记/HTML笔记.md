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
<br /> #单标签 数量非常少
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

* ！或者html：5或html+Tab快速生成框架

* ```<!DOCTYPE html>```#告诉我们这个是哪一个版本的html，我们目前使用的是HTML5的版本

* UTF-目前最常用的字符集编码方式，常用的编码方式还有gbk和gb2312。

  * GB2312 简体中文 包含6763个汉字

  	* BIG5 繁体中文 港澳台等用
  	* GBK 包含全部中文字符 是GB2312的扩展，加入繁体字的支持，兼容GB2312
  	* UTF-8 则包含全世界所有国家需要用到的字符

