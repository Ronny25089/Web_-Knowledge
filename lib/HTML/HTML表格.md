[>>>上一篇：HTML标签、元素和属性](../../lib/HTML/HTML标签、元素和属性.md)
## HTML表格
---
`<table>`标签属于常用标签。请先预读以下链接中的文章，再回过头来 展开一些内容。  
[>>HTML 表格](https://www.runoob.com/html/html-tables.html)

通过学习以上的内容，能了解到html的<table>标签可以用来书写出类似于excel的表格内容。
`<table>`除了border属性还有一个重要的属性cellspacing（表单间隙），通过设置cell spacing属性，可以达到**消除/增大**表单间隙。
其次，表单中的内容不止局限于文本内容（TEXT），还可以往里添加标签元素。

### 内容嵌套
往表单`cell`中添加链接标签`<a/>`和图像标题`<img/>`
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

### 带表头的HTML写法
```
<div>
<table >
  <thead>
    <tr>
      <th>head1</th>
      <th>head2</th>
      <th>head3</th>
      <th>head4</th>
      <th>head5</th>
      <th>head6</th>
      <th>head7</th>
    </tr>
  </thead>
  <tbody>
    <tr class="row">
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
  </tbody>
</table>
</div>
```

运行结果： 
<div>
<table >
  <thead>
    <tr>
      <th>head1</th>
      <th>head2</th>
      <th>head3</th>
      <th>head4</th>
      <th>head5</th>
      <th>head6</th>
      <th>head7</th>
    </tr>
  </thead>
  <tbody>
    <tr class="row">
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
  </tbody>
</table>
</div>


同时若想固定表头，或者某一列的时候，需要用到CSS定位元素`position: sticky;`将指定的标签固定在一个相对位置，   
表述位置的时候需要用`top: 0;`意思为 固定在相对于父类标签内边的顶部0位置  
`left: 0;`意思为 固定在相对于父类标签内边的左边0位置  


```
/* 固定第一行 */
thead th {
  position: -webkit-sticky;
  position: sticky;
  /* 相对位置 */
  top: 0;
  /* 将表头提高到1层 */
  z-index: 1;
  background-color: #8ebfd2;
}

/* 固定第一列 */
td:first-child, th:first-child {
  position: -webkit-sticky;
  position: sticky;
  /* 相对位置 */
  left: 0;
  background-color: #fbe375;
}
```

运行实例：
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="css,result" data-user="ronny25089" data-slug-hash="xxRwNbE" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="xxRwNbE">
  <span>See the Pen <a href="https://codepen.io/ronny25089/pen/xxRwNbE">
  xxRwNbE</a> by memo (<a href="https://codepen.io/ronny25089">@ronny25089</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

HTML/CSS/JS 在线工具https://c.runoob.com/front-end/61  
[>>>下一篇：HTML区块](../../lib/HTML/HTML区块.md)
