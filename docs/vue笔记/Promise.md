#### 介绍

* promise作用就是构造异步操作的一个方式，它的结构包括执行异步操作和异步完成后的处理操作
* 网络请求最常用到异步

```javascript
new Promise((resolve, reject) =>{
  setTimeout(() => {
    resolve()
  }, 1000)
}).then(() => {
  
})
```

* then中放要执行的代码
* 用setTImeout模拟异步操作，一个setTImeout就相当于一次网络请求
* promise将网络请求代码分为两部分：1.网络请求的代码   2.拿到请求结果后的代码

``````javascript
setTimeout(() => {
  console.log('Hello World')
}, 1000)
``````

* 链式编程：每一条链处理自己的，下一次处理交给下一个链条。链式编程不需要嵌套，可以让代码结构变的非常清晰。

#### 操作方式

1. 将异步函数用new promise包裹起来
2. 不要将异步之后的代码放到异步函数中，而是写个resolve()，然后在后面的.then中写
3. 当不成功时，调用reject，对应到.catch中，操作错误信息

#### 返回的位置：

1. 返回的数据：在then的data处

2. 错误信息：catch处

#### promise的三种状态

1. pending等待，正在进行网络请求
2. fulfilled满足（请求到结果）（调用resolve和then）
3. rejected拒绝（网络请求失败）(调用catch)

