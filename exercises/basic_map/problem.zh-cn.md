# 任务

将以下代码从for循环转换成Array.map:

```js
function doubleAll(numbers) {
  var result = []
  for (var i = 0; i < numbers.length; i++) {
    result.push(numbers[i] * 2)
  }
  return result
}

module.exports = doubleAll
```

## 参数

* numbers: 一个包含0-20个一位数的数组

## 条件

* 你的解法应该使用`Array.prototype.map()`
* 不要使用任何for循环或者`Array.prototype.forEach`.
* 不要创建多余的方法.

## 资源

* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map

## 模板

```js
function doubleAll(numbers) {
  // 这里写你的代码
}

module.exports = doubleAll
```
