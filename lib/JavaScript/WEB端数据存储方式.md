[>>>下一篇：jQuery 特性](../../lib/JavaScript/jQuery特性.md)

## WEB端数据存储方式
---
js的存储在实际应用中被广泛地使用,
**比如**：记录用户登录状态，初次使用该功能与否

### 浏览器存储技术：
- 本地化存储(离线存储)

- 它们均只能存储字符串类型的对象

- 都是用来存储客户端临时信息的对象

|浏览器存储技术|生命周期|存储容量|服务器 通信|
|---|---|---|---|
|cookie|随浏览器关闭失效，如果设置过期时间，在到过期时间后失效|4KB|每次与服务器通信，都携带再HTTP头当中。|
|sessionStorage|仅在当前网页会话下有效，关闭 页面/浏览器 后会被清除。|5MB|不参与通信|
|localStorage|理论上永久有效的，除非主动清除。|5MB|不参与通信|
|indexDB|理论上永久有效的，除非主动清除。|无限制|不参与通信|

### cookie
Cookie是访问某些网站以后在本地存储的一些网站相关的信息，下次再访问的时候减少一些步骤。

主要内容：

- key：键
- value： 该键的值，只能是字符串类型。
- max_age/expire_time：设置cookie的期限
- domain： 指定在哪个域名中有效，比如www.example.com
- path： 指定在哪些路径下有效

默认情况下，cookie 属于当前页面。domain就是当前的域名。
- 使用 JavaScript 创建/修改 Cookie
    ```
    document.cookie="key=value; expires=期限; path=路径";
    document.cookie="username=John Doe; expires=Thu, 18 Dec 2013 12:00:00 GMT; path=/";
    ```
- 使用 JavaScript 读取 Cookie
    ```
    var x = document.cookie;
    ```
- 使用 JavaScript 删除 Cookie
    ```
    document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 GMT";
    ```

**例如，**我们登录网站时需要输入用户名及密码，如果用户名和密码保存为cookie，以后打开该网站地时候，用户名密码会自动填充。
 一般画面上多是通过以下的方式出现：
- [ ] 记住密码
- [x] 记住密码30天

### sessionStorage
页面中一般的js对象的生存期仅在当前页面有效，因此刷新页面或转到另一页面这样的重新加载页面的情况，数据就不存在了。
只要同源(同origin，即同一个网站)的同窗口中，刷新页面或进入同源的不同页面，数据始终存在，也就是说只要浏览器不关闭，数据仍然存在。

**例如，**用于保存用户在输入框中的临时草稿。
比如用户在编辑发送朋友圈或微博的时候，当要取消的时候都会提示是否保存草稿，这时候草稿保存在sessionStorage中是最有效率的。

- 读取全部数据集合语法
    ```
    window.sessionStorage
    ```
- 保存数据语法：
    ```
    sessionStorage.setItem("key", "value");
    ```
- 读取数据语法：
    ```
    var lastname = sessionStorage.getItem("key");
    ```
- 删除指定键的数据语法：
    ```
    sessionStorage.removeItem("key");
    ```
- 删除所有数据：
    ```
    sessionStorage.clear();
    ```

### localStorage
`localStorage`可以理解为`sessionStorage`的升级版，它不会随着浏览器的关闭而消失。
一般使用在保存用户习惯等的记录。localStorage 属性是只读的。

- 读取全部数据集合语法
    ```
    window.localStorage
    ```
- 保存数据语法：
    ```
    localStorage.setItem("key", "value");
    ```
- 读取数据语法：
    ```
    var lastname = localStorage.getItem("key");
    ```
- 删除数据语法：
    ```
    localStorage.removeItem("key");
    ```

### indexDB
一种存储在客户端本地的 NoSQL 数据库，它可以存储大量的数据。
一个网站可以有多个 indexedDB 数据库，但每个数据库的名称是唯一的。我们需要通过数据库名来连接某个具体的数据库。
 可以理解的是，当以上的`localStorage`和`sessionStorage` 无法满足当前需求的时候，可以使用indexDB。

关于本地存储详细了解[>>掘金网_浏览器端数据存储方案](https://juejin.im/post/5aeaf545518825673b61ddc8)

---
### 服务器端存储技术：

|服务器端存储技术|生命周期|存储容量|
|---|---|---|
|session|仅在当前网页会话下有效，关闭页面或浏览器后会被清除。|没有限制，但是为了服务器性能考虑，一般不能存放太多数据|

### session
session是存在服务器的一种用来存放用户数据的类HashTable结构。

浏览器第一次发送请求时，服务器自动生成了一HashTable和一SessionID来唯一标识这个HashTable，并将其通过响应发送到浏览器。浏览器第二次发送请求会将前一次服务器响应中的SessionID放在请求中一并发送到服务器上，服务器从请求中提取出Session ID，并和保存的所有Session ID进行对比，找到这个用户对应的HashTable。

**例如，**我们浏览一个购物网站，用户将部分商品添加到购物车中，许久以前许多网站都是用服务端session存储购物车内容（现在基本都是用数据库了），就用到了session存储这部分信息。


[>>>下一篇：api接口](../../lib/server/api接口.md)
