[>>>上一篇：关于前端](../../lib/关于前端.md)

### 理解HTML
---

HTML是一种用于创建网页的标准标记语言。
超文本标记语言（英语：HyperText Markup Language，简称：HTML）是一种用于创建网页的标准标记语言。
您可以使用 HTML 来建立自己的 WEB 站点，HTML 运行在浏览器上，由浏览器来解析。

[>>菜鸟_HTML教程](https://www.runoob.com/html/html-tutorial.html)

#### HTML文档的后缀名
- html
- htm

HTML文档的打开方式可以通过双击，浏览器打开查看效果。  
※在上线的程序当中，HTML文档多是服务器通过[相对路径/绝对路径](https://www.jianshu.com/p/8baf85dc7d42)来调用（呼叫），默认打开主页一般设置为index.html。

#### HTML标签书写格式
- <标签名>...</标签名>
- &lt;html&gt;...&lt;/html&gt;
- &lt;a/&gt;

html中处处可见的尖括号<>，这被称为标签，绝大多数的标签都是成对出现的：分为起始标签和结束标签，夹在两个标签中的内容被称为元素。HTML文本内容是由多个HTML标签组成的。

[>>HTML 标签列表](https://www.runoob.com/tags/html-reference.html)  
[>>HTML 实例](https://www.runoob.com/html/html-examples.html)


#### 基本结构
下面是组成一个HTML文本的基本结构。
- html
    - head
        - title:我的网页
    - body
        - <内容/>

**<内容/>**里头书写我们所要构建的网页内容。
通过学习HTML标签，可以自行组装**标签**和**元素**，构建出自己的网页。
可以将以上的概念，书写成html文本格式。
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>我的网页</title>
  </head>
  <body>
      ....
  </body>
</html>
```

HTML/CSS/JS 在线工具https://c.runoob.com/front-end/61

[>>>下一篇：HTML标签、元素和属性](../../lib/HTML/HTML标签、元素和属性.md)
