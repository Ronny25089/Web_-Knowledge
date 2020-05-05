[>>>上一篇：CSS 选择器](../../lib/CSS/CSS选择器.md)

### CSS伪类
---
CSS 伪类用于向某些选择器添加特殊的效果。获得指定状态下的元素。  
属于比较高级的css语法，可以大大提高生产性。在一些需要可读性要求高的项目中，应用的比较少，转而使用更加繁琐，但更通俗易懂的方式。但可以了解以下伪类。

#### 全部伪类和伪元素（按字母顺序）
- :active
- ::after/:after
- ::backdrop (experimental)
- ::before/:before
- :checked
- :default
- :dir (experimental)
- :disabled
- :empty
- :enabled
- :first-child
- ::first-letter/:first-letter
- ::first-line/:first-line
- :first-of-type
- :focus
- :fullscreen (experimental)
- :hover
- :in-range
- :indeterminate
- :invalid
- :lang
- :last-child
- :last-of-type
- :link
- :not
- :nth-child
- :nth-last-child
- :nth-last-of-type
- :nth-of-type
- :only-child
- :only-of-type
- :optional
- :out-of-range
- ::placeholder (experimental)
- :read-only
- :read-write
- :required
- :root
- ::selection
- :scope (experimental)
- :target
- :valid
- :visited

具体了解每个伪类元素，可以转至[>>菜鸟教程_CSS伪类](https://www.runoob.com/css/css-pseudo-classes.html)

因为CSS样式是用来描述HTML标签的，最终是作用在标签上的。
一些具有功能性的标签，比如：`<a/>`，`<button/>`，`<option/>`，`<input type="checkbox"/>`，`<input type="radio"/>`等,他们都可能具有不同的状态。通过伪类，我们给同一个标签，在不同的状态下显示不同的样式。
##### 常用的实例：
- `<a/>`会有以下几种状态，就可以根据不同的状态，给`<a/>`添加以下CSS样式。
>```
a:link {color: #FF0000}     //未访问的链接
a:visited {color: #00FF00}  //已访问的链接
a:hover {color: #FF00FF}    //鼠标移动到链接上
a:active {color: #0000FF}   //选定的链接
```

- `<button/>`
>```
button {color: white;}              //普通状态
button:hove {color: red;}           //鼠标停留状态
button:active {color: blue;}        //active 点击状态
button:focus {color: yellow;}       //focus 取得焦点状态(通过tab键)
button:disabled {background: gray;} //被禁用的状态
```

- `<option/>`
- `<input type="checkbox"/>`
- `<input type="radio"/>`
>```
option:default {color: white}               //未访问的链接
option:checked {color: red}                 //被勾选项目,option(select中的一项)
input[type="checkbox"]checked {color: red}  //被勾选项目,checkbox中的一项
input[type="radio"]:checked {color: red}    //被勾选项目,radio中的一项
```

[>>>上一篇：CSS 值与单位](../../lib/CSS/CSS值与单位.md)
