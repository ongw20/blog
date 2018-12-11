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
