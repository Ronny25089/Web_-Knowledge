[>>>上一篇：js 回调函数](../../lib/JavaScript/js回调函数.md)

## 了解jQuery
---
[>>菜鸟教程__jQuery 教程](https://www.runoob.com/jquery/jquery-tutorial.html)  

jQuery是JavaScript世界中使用最广泛的一个库。  
江湖传言，全世界大约有80~90%的网站直接或间接地使用了jQuery。鉴于它如此流行，又如此好用，所以每一个入门JavaScript的前端工程师都应该了解和学习它。  
jQuery 极大地简化了 JavaScript 编程。

[>>jQuery官方API文档](https://api.jquery.com/)

参照以上文档，可以看到jQuery的所有方法。
jQuery的方法基本上是基于现有的原生JS的方法而产生的，目的是为了将原生JS中复杂的编程方法简化。  
几乎所有的jQuery的方法都可以找到相对应的原生JS的方法。  

也就是说在只使用原生JS进行开发的情况下，几乎可以将大多数的原生JS代码替换成使用jQuery库的写法。

同时jQuery社区还有各种各样丰富的插件库。  
**例如：**jGrid（表格数据的生成），jQuery mobile（一个手机WEB开发的库），jQuery UI（可自定义主题的GUI控件与动画效果）等等...  
[>>jQuery各种插件库](https://plugins.jquery.com/tag/ui/)

### 使用jQuery  
使用jQuery只需要在页面的`<head>`引入jQuery文件即可：  
```
<html>
<head>
    <script src="//code.jquery.com/jquery-1.11.3.min.js"></script>
	...
</head>
<body>
    ...
</body>
</html>
```

### $符号
`$`是著名的jQuery符号。实际上，jQuery把所有功能全部封装在一个全局变量jQuery中，而`$`也是一个合法的变量名，它是变量jQuery的别名：
```
window.jQuery; // jQuery(selector, context)
window.$; // jQuery(selector, context)
$ === jQuery; // true
typeof($); // 'function'
```

### jQuery的选择器
选择器是jQuery的核心。一个选择器写出来类似`$('#id')`  
很多时候使用jQuery，也是因为其选择器的便利性。在下一章节会详细讲解jQuery选择器的运用。

HTML/CSS/JS 在线工具https://c.runoob.com/front-end/61

[>>>下一篇：jQuery 选择器](../../lib/JavaScript/jQuery选择器.md)
