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
window.addEventListener('popstate', func) // 监听浏览器前进后退
```
ps: 刷新浏览器网页加载对应路由内容
```js
window.addEventListener('load', func)
```
