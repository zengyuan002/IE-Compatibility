# 一行代码解决各种IE兼容问题,IE6,IE7,IE8,IE9,IE10

1、百度源代码如下
```
<!Doctype html>
<html xmlns=http://www.w3.org/1999/xhtml xmlns:bd=http://www.baidu.com/2010/xbdml>;
<head>
<meta http-equiv=Content-Type content=“text/html;charset=utf-8″>
<meta http-equiv=X-UA-Compatible content=IE=EmulateIE7>
<title>百度一下，你就知道 </title>
<script>var wpo={start:new Date*1,pid:109,page:‘superpage’}</script>
<meta http-equiv=X-UA-Compatible content=IE=EmulateIE7>

可以打开百度，右键查看源码看下！我们可以看下文件头是否存在这样一行代码！

这句话的意思是强制使用IE7模式来解析网页代码！

在这里送上几种IE使用模式！

<meta http-equiv=“X-UA-Compatible” content=“IE=8″>
```
2. Google Chrome Frame也可以让IE用上Chrome的引擎:
```
<meta http-equiv=“X-UA-Compatible” content=“chrome=1″ />
```
.强制IE8使用IE7模式来解析
```
<meta http-equiv=“X-UA-Compatible” content=“IE=EmulateIE7″><!– IE7 mode –>
//或者
<meta http-equiv=“X-UA-Compatible” content=“IE=7″><!– IE7 mode –>
```
4.强制IE8使用IE6或IE5模式来解析
```
<meta http-equiv=“X-UA-Compatible” content=“IE=6″><!– IE6 mode –>

<meta http-equiv=“X-UA-Compatible” content=“IE=5″><!– IE5 mode –>
```
5.如果一个特定版本的IE支持所要求的兼容性模式多于一种，如：
```
<meta http-equiv=“X-UA-Compatible” content=“IE=5; IE=8″ />
```
二.设定网站服务器以指定预设兼容性模式
```
如果服务器是自己的话，可以在服务器上定义一个自订标头来为它们的网站预设一个特定的文件兼容性模式。这个特定的方法取决于你的网站服务器。

录入，下列的 web.config文件使Microsoft Internet Information Services (IIS)能定义一个自订标头以自动使用IE7 mode来编译所有网页。

另外还有一起其他的解决方案，例如google的

ie7 – js中是一个JavaScript库（解决IE与W3C标准的冲突的JS库），使微软的Internet Explorer的行为像一个Web标准兼容的浏览器，支持更多的W3C标准，支持CSS2、CSS3选择器。它修复了许多的HTML和CSS问题，并使 得透明PNG在IE5、IE6下正确显示。

使IE5,IE6兼容到IE7模式（推荐）

<!–[if lt IE 7]>
<script src=”http://ie7-js.googlecode.com/svn/version/2.0(beta)/IE7.js” type=”text/javascript”></script>
<![endif]–>
使IE5,IE6,IE7兼容到IE8模式

<!–[if lt IE 8]>
<script src=”http://ie7-js.googlecode.com/svn/version/2.0(beta)/IE8.js” type=”text/javascript”></script>
<![endif]–>
使IE5,IE6,IE7,IE8兼容到IE9模式

<!–[if lt IE 9]>
<script src=”http://ie7-js.googlecode.com/svn/version/2.1(beta4)/IE9.js”></script>
<![endif]–>
解决PNG显示问题

只需将透明png图片命名为*-trans.png

需要注意的是：此方法对背景平铺(background-repeat)和背景(background-position)无法起到任何作用,默认会占满整个容器。
```
三、<meta http-equiv=”X-UA-Compatible” content=”IE=edge,chrome=1″ />
创建html5时发现这么一句话，不知其什么意思，百度如下：
这 样写可以达到的效果是如果安装了GCF，则使用GCF来渲染页面，如果没安装GCF，则使用最高版本的IE内核进行渲染。Google Chrome Frame（谷歌内嵌浏览器框架GCF）。这个插件可以让用户的IE浏览器外不变，但用户在浏览网页时，实际上使用的是Google Chrome浏览器内核，而且支持IE6、7、8等多个版本的IE浏览器。
