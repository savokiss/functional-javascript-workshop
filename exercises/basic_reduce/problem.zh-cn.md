# 任务

给定一个字符串数组,使用`Array#reduce`创建一个对象,该对象包含每个字符串在数组中出现的次数,最后直接返回这个对象

## 例子

```js
var inputWords = ['Apple', 'Banana', 'Apple', 'Durian', 'Durian', 'Durian']

console.log(countWords(inputWords))//此处是示例,不用打印出来

// =>
// {
//   Apple: 2,
//   Banana: 1,
//   Durian: 3
// }
```

## 参数

* inputWords: 一个包含若干随即字符串的数组

## 条件

* 不要使用for/while循环或者Array#forEach
* 不要创建多余的函数.

## 资源

* https://en.wikipedia.org/wiki/Reduce_(higher-order_function)
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce

## 模板

```js
function countWords(inputWords) {
  // SOLUTION GOES HERE
}

module.exports = countWords
```
