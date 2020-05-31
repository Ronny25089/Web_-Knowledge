[>>>上一篇：js匿名函数和闭包](../../lib/JavaScript/js匿名函数和闭包.md)
## js 回调函数
---
>※可以先跳过这部分内容，等有更多开发经验后，会更容易理解。

**callback**，回调函数是一个函数，将会在另一个函数完成执行后立即执行。回调函数是一个作为参数传给另一个 JavaScript 函数的函数。这个回调函数会在传给的函数内部执行。

在 JavaScript 中函数被看作是一类对象。对于一类对象，我们的意思是指数字、函数或变量可以与语言中的其他实体相同。作为一类对象，可以将函数作为变量传给其他函数，也可以从其他函数中返回这些函数。  

可以执行这种操作的函数被称为高阶函数。回调函数实际上是一种模式。 “模式”一词表示解决软件开发中常见问题的某种行之有效的方法。最好将回调函数作为回调模式去使用。

### 回调函数运用情景
现有以下两个处理需要执行，但条件是当A处理完后，在执行B处理。
- A处理
- B处理

```
function add(num1, num2, callback){
	var sum = num1 + num2;   // A处理
	callback(sum);           // 通过回调，调用print函数，执行B处理
}

function print(num){         // print函数
	console.log(num);        // B处理
}

add(1, 2, print);		//=>3
```

### 特点
不会立刻执行  
回调函数作为参数传递给一个函数的时候，传递的只是函数的定义并不会立即执行。  
和普通的函数一样，回调函数在函调用函数数中也要通过()运算符调用才会执行。

回调函数是一个闭包，也就是说它能访问到其外层定义的变量。



### "回调地狱"
回调函数真的是一个让人又爱又恨的东西。一方面，它让Javascript能够非常简洁地实现异步函数；一方面，它又让你的代码难以去理解和维护。  
下面是一个有意思的例子，可以了解一下。
```
var p_client = new Db('integration_tests_20', new Server("127.0.0.1", 27017, {}), {'pk':CustomPKFactory});
   p_client.open(function(err, p_client) {
       p_client.dropDatabase(function(err, done) {
           p_client.createCollection('test_custom_key', function(err, collection) {
               collection.insert({'a':1}, function(err, docs) {
                   collection.find({'_id':new ObjectID("aaaaaaaaaaaa")}, function(err, cursor) {
                       cursor.toArray(function(err, items) {
                           test.assertEquals(1, items.length);

                           // Let's close the db
                           p_client.close();
                       });
                   });
               });
           });
       });
   });

```

[>>掘金网__深入理解 JavaScript 回调函数](https://juejin.im/post/5dc1474df265da4d1518ee76)

HTML/CSS/JS 在线工具https://c.runoob.com/front-end/61

[>>>下一篇：了解 jQuery](../../lib/JavaScript/了解jQuery.md)
