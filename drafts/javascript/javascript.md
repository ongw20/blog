# Javascript

### Time
```js
new Date().toJSON() // 2018-08-01T07:25:06.595Z
```

### Error
async 立即执行函数捕获内部错误
```js
(async () => {
  throw 'an error'
})().catch(err => {
  console.log(err)
})
```

### Router
- hash
```js
window.location.hash = 'xxx'  // 改变 hash
window.addEventListerner('hashchange', func)  // 监听 hash 改变
```

- url
```js
history.pushState(obj, title, 'url')  // 改变 url
window.addEventListener('popstate', func) // 监听浏览器前进后退
```
ps: 刷新浏览器网页加载对应路由内容
```js
window.addEventListener('load', func)
```

### instanceof
`instanceof` 又叫关系运算符，用来判断某个构造函数的 `prototype` 对象是否存在在另外一个要检测对象的原型链上。
每个js对象都有一个 `proto` 属性（标准表示 `[[prototype]]`)，proto是普通对象的隐式属性，在实例化的时候，会指向 prototype 所指的对象。
```js
a instanceof b // 检查 b.prototype 是否在 a 的原型链上
```

### constructor
`constructor` 存在于每一个 function 的 prototype 属性中，保存了指向 function 的一个引用。
