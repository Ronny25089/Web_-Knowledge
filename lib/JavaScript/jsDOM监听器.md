[>>>上一篇：jsDOM事件](../../lib/JavaScript/jsDOM事件.md)
## jsDOM监听器
---
[>>菜鸟教程__jsDOM监听器监听器](https://www.runoob.com/js/js-htmldom-eventlistener.html)  

上一节讲述到了DOM事件，是通过标签的属性，主动调用的。  
这一节的主要讲述的内容是DOM事件的监听器，通过监听的方式来达到同样，甚至更好的效果。  
#### 作用：
- `addEventListener()` 方法为指定元素指定事件处理程序。

- `addEventListener()` 方法为元素附加事件处理程序而不会覆盖已有的事件处理程序。

#### 优点：
- 能够向一个元素添加多个事件处理程序。  

- 能够向一个元素添加多个相同类型的事件处理程序，例如两个 "click" 事件。
- 能够向任何 DOM 对象添加事件处理程序而非仅仅 HTML 元素，例如 window 对象。
- `addEventListener()` 方法使我们更容易控制事件如何对冒泡作出反应。
- 当使用 `addEventListener()` 方法时，JavaScript 与 HTML 标记是分隔的，已达到更佳的可读性；即使在不控制 HTML 标记时也允许添加事件监听器。
- 能够通过使用 `removeEventListener()` 方法轻松地删除事件监听器。

### 语法
```
element.addEventListener(event, function, useCapture);
```
- 第一个参数是事件的类型（比如 "click" 或 "mousedown"）。
- 第二个参数是当事件发生时我们需要调用的函数。
- 第三个参数是布尔值，指定使用事件冒泡还是事件捕获。此参数是可选的。

※注意：请勿对事件使用 "on" 前缀；请使用 "click" 代替 "onclick"。

一般多如下：
```
<DOM对象>.addEventListener("<事件>", <函数>);
```

可以先看一下下面这个实例

### 用户行为实例:
比如： 当一个按钮被点击后，改变其按钮名称和背景颜色。
```
<!DOCTYPE HTML>
<html>  
<head>  
  <title>Event</title>  
</head>
<body>
  <button id="btn">来点我</button>
</body>
</html>
```
```
document.getElementById("btn").addEventListener("click", clickMe);

function clickMe(){
  document.getElementById("btn").innerText ="点击成功";
  document.getElementById("btn").style.background = 'yellow'
}
```
或者使用**匿名函数**：
```
document.getElementById("btn").addEventListener("click", function(){
  document.getElementById("btn").innerText ="点击成功";
  document.getElementById("btn").style.background = 'yellow'
});
```

<img src="../../img/event01.GIF" width="300" border="1px"/>   


HTML/CSS/JS 在线工具https://c.runoob.com/front-end/61

[>>>下一篇：js匿名函数和闭包](../../lib/JavaScript/js匿名函数和闭包.md)
