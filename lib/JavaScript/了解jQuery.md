[>>>上一篇：js 回调函数](../../lib/JavaScript/js回调函数.md)

## 了解jQuery
---
[>>菜鸟教程__jQuery 教程](https://www.runoob.com/jquery/jquery-tutorial.html)  

jQuery是JavaScript世界中使用最广泛的一个库。  
江湖传言，全世界大约有80~90%的网站直接或间接地使用了jQuery。鉴于它如此流行，又如此好用，所以每一个入门JavaScript的前端工程师都应该了解和学习它。  
Query 极大地简化了 JavaScript 编程。

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



HTML/CSS/JS 在线工具https://c.runoob.com/front-end/61

[>>>下一篇：jQuery 选择器](../../lib/JavaScript/jQuery选择器.md)
