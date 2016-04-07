递归在编程中是个基本的概念,恰当使用也能带来优雅和高效的算法.事实上递归很强大,所有的迭代都可以写成递归的形式,当你在迭代嵌套的数据类型时,你会发现递归是不可或缺的.

递归方法就是一个方法调用自己. 例如,下面的方法会接收一个单词数组,然后将其中的单词大写后返回.

```js
function toUpperArray(items) {
   if (!items.length) return []             // end condition
   var head = items[0]                      // item to operate on
   head = head.toUpperCase()                // perform action
   var tail = items.slice(1)                // next
   return [head].concat(toUpperArray(tail)) // recursive step
}

toUpperArray(['hello', 'world']) // => ['HELLO', 'WORLD']
```

这个练习的重点是让你熟悉递归的实现.

# 任务

用递归实现Array#reduce

为了验证你的实现,我们会使用它来执行上一节basic_reduce的问题
即:你的实现方法会被传入一个单词数组,一个方法和一个初始值(上一节中是{},最终需要返回出来,并包含每个单词的在数组中出现的次数)
你不需要实现这个功能,这些数据会传入你的函数中

简单起见,你的reduce实现不用考虑忽略那个初始值的情况.

## 参数

* arr: 被reduce的数组
* fn: reduce过程中的回调函数. 就像Array#reduce一样,这个函数必须包含四个参数:previousValue,currentValue,index和array
* init: reduce的初始值. 和Array#reduce不同的是,此值是必填的

## 例子

```js
// 你的reduce方法和Array#reduce的区别就是迭代的数组要在第一个参数中接收

reduce([1,2,3], function(prev, curr, index, arr) {
  return prev + curr
}, 0)
// => 6
```

## 条件

* 不要使用for/while循环
* 不要使用Array#map或者Array#reduce

## 资源

* https://en.wikipedia.org/wiki/Recursion
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce

## 模板

```js
function reduce(arr, fn, initial) {
  // 代码写在这里
}

module.exports = reduce
```
