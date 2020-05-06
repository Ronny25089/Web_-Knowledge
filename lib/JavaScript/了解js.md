[>>>上一篇：CSS 问题分析思路](../../lib/CSS/CSS问题分析思路.md)

## 了解js
---
JavaScript 是 Web 的编程语言。
所有现代的 HTML 页面都使用 JavaScript。

具体的JS语法等方面的问题，请详细查看[>>菜鸟_JS教程](https://www.runoob.com/js/js-tutorial.html)，接下来介绍JavaScript 如何与 HTML 和 CSS 一起工作。

之前通过【[>>关于前端](../../关于前端.md)】这一章节的了解，可以得知在WEB前端中，js是可以通过代码的编写，来控制html和css的，而达到一种动态的效果的。  
js是运行在客户端上的编程语言，与后端语言本质上是一样的，只是适用的场景不同而已。  
js由浏览器负责解释执行，js的使用可以减轻服务器的压力，比如使用js检测输入数据格式、局部数据刷新等等。

### 书写JS
- **内嵌HTML中**  
  JS内容也可以写在html文本中,通过`<script>`标签来实现。  
  ```
    //可以通过底部的在线工具，尝试一下下面的实例：
    <script>
    function displayDate(){
    	document.getElementById("demo").innerHTML=Date();
    }
    </script>
    <h1 onclick="displayDate()">显示日期</h1>
    今天是：<span id="demo">几年几月几日</span>
  ```  
  通过点击`显示日期`能显示当前日期  
  <img src="../../img/js_tutorial01.GIF" width="350" border="1px"/>  

  - 优点：直接，简单  
  - 缺点：不方便复用和维护,不符合结构行为分离规范  

- **独立js文件**  
    为了规范书写JS内容文本，我们更多地是利用XXX.js文档。让**html文件** 和**js文件**产生关联,通过`<script>`标签的 `src` 属性 链接到js文件。
    ```
    <script src="XXX.js"></script>
    ```
    和css文件一样，要做到分离。只通过关联标签，将三方联系在一起。这样书写的html，css，js可以达到解耦的状态。使彼此之间的联系没有那么紧密，更不容易因为一方的维护而影响其他的区域。同时也能达到统一修改css样式和js行为的目的，便于维护。  
    - 优点：
      1. 结构 行为 完全分离
      1. 方便修改维护
      1. 可复用性强   

### 书写格式  
  依据js语法，如下：  
  - 声明变量
  - 声明函数
  - 函数内部执行内容
  - etc...

```
var 变量名 = 值;
例：
//声明一个数值类型
var num = 1;
//声明一个字符串
var str = "字符串";
//声明一个boolean
var flag = true;
//声明一个数组
var arr = [1,2,3,4];
//声明一个object
var obj = {
  id = 00001,
  userCd = "test001",
  userName = "testUser",
  pwd = "1234567"
}
//声明一个函数，但此函数只有在var语句声明之后才能被调用
var XXX = funtion () {
  //TODO...
};

//function声明方式,函数可以在function声明之前被调用
function XXX() {
  //TODO...
};
```
  即js中万物皆是对象，连函数都不放过。因为函数也是对象，所以在JS中函数也可以被当作参数用来传递使用。

HTML/CSS/JS 在线工具https://c.runoob.com/front-end/61

[>>>下一篇：js变量和函数](../../lib/JavaScript/js变量和函数.md)
