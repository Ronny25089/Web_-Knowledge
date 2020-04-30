[>>>上一篇：HTML标签、元素和属性](../../lib/HTML/HTML标签、元素和属性.md)
### HTML 表格
---
&lt;talble&gt;标签属于常用标签。请先预读以下的文章，再回过头来 展开一些内容。

[>>>HTML 表格](https://www.runoob.com/html/html-tables.html)

通过学习以上的内容，能了解到html的<table>标签可以用来书写出类似于excel的表格内容。
<table>除了border属性还有一个重要的属性cellspacing（表单间隙），通过设置cell spacing属性，可以达到消除表单间隙。
其次，表单中的内容不止局限于文本（TEXT），还可以往里添加标签元素。

#### 内容嵌套

```
<table border="1" cellspacing="0">
    <tr>
        <td>教程</td>
        <td>链接</td>
      	<td>图片</td>
    </tr>
    <tr>
        <td>HTML教程</td>
      	<td><a href="https://www.runoob.com/html/html-tables.html">href</a></td>
      	<td><img src="https://img.icons8.com/material-sharp/2x/launch-browser.png"></td>
    </tr>
</table>
```
运行结果：
<table border="1" cellspacing="0">
    <tr>
        <td>教程</td>
        <td>链接</td>
      	<td>图片</td>
    </tr>
    <tr>
        <td>HTML教程</td>
      	<td><a href="https://www.runoob.com/html/html-tables.html">href</a></td>
      	<td><img src="https://img.icons8.com/material-sharp/2x/launch-browser.png"></td>
    </tr>
</table>
