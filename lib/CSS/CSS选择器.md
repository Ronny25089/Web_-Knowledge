[>>>上一篇：了解 CSS](../../lib/CSS/了解CSS.md)

## CSS选择器
---
CSS选择器用于选择你想要的元素的样式的模式。  
[>>CSS选择器](https://www.runoob.com/cssref/css-selectors.html)

### 1.基本选择器  

| 选择器 | 含义 |  
| ---- | ---- |
| * | 通用元素选择器，匹配任何元素 |
| E	| 标签选择器，匹配所有使用E标签的元素 |
| .info |	class选择器，匹配所有class属性中包含info的元素 |
| #footer |	id选择器，匹配所有id属性等于footer的元素 |

#### 实例：
```
* { margin:0; padding:0; }

p { font-size:2em; }

.info { background:#ff0; }

p.info { background:#ff0; }

p.info.error { color:#900; font-weight:bold; }

#info { background:#ff0; }

p#info { background:#ff0; }
```

### 2.多元素的组合选择器
| 选择器	| 含义 |
| ---- | ---- |
| E,F	| 多元素选择器，同时匹配所有E元素或F元素，E和F之间用逗号分隔 |
| E F	| 后代元素选择器，匹配所有属于E元素后代的F元素，E和F之间用空格分隔 |
| E > F	| 子元素选择器，匹配所有E元素的子元素F |
| E + F	| 毗邻元素选择器，匹配所有紧随E元素之后的同级元素F |

#### 实例：
```
div p { color:#f00; }

#nav li { display:inline; }

#nav a { font-weight:bold; }

div > strong { color:#f00; }

p + p { color:#f00; }
```

### 3.属性选择器
| 选择器 |	含义|
| ---- | ---- |
|	E[att] |	匹配所有具有att属性的E元素，不考虑它的值。（注意：E在此处可以省略，比如"[cheacked]"。以下同。）|
|	E[att=val] | 匹配所有att属性等于"val"的E元素 |
|	E[att~=val] |	匹配所有att属性具有多个空格分隔的值、其中一个值等于"val"的E元素|
|	E[att\|=val] |	匹配所有att属性具有多个连字号分隔（hyphen-separated）的值、其中一个值以"val"开头的E元素，主要用于lang属性，比如"en"、"en-us"、"en-gb"等等|

```
p[title] { color:#f00; }

div[name=error] { color:#f00; }

td[headers~=col1] { color:#f00; }

p[lang|=en] { color:#f00; }

blockquote[class=quote][cite] { color:#f00; }
```

>以上这些是常用的选择器。
还不是最全的，具体可以参考以下的文章。  
[>>阮一峰的网络日志・CSS选择器笔记](http://www.ruanyifeng.com/blog/2009/03/css_selectors.html)

[>>>下一篇：CSS 伪类](../../lib/CSS/CSS伪类.md)
