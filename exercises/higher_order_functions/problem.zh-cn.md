高阶函数最少符合下面的条件之一:

* 接收一个或多个函数作为参数
* 返回一个函数

剩下的函数就都是一阶函数(first order function) [1]

在JS中之所以能使用高阶函数，是因为函数在JS中是第一类对象。这就意味着你可以把函数和其他的数据类型（String, Number）同等对待，函数可以被保存在变量中，属性中或者传递到其他函数中。而函数值本质上就是Object(继承自`Function.prototype`)，所以你甚至可以在函数中添加属性。

函数和其他数据类型的关键不同点在于JS的调用语法：如果一个函数的引用后面跟着一对括号里面可能还有几个参数：`someFunctionValue(arg1, arg2, etc)`，这个函数的函数体就会被执行

在这个练习中我们将会验证函数可以被当做参数传给其它函数。

# 任务

实现一个函数，它的第一个参数是一个函数，第二个参数是`num`，然后执行传入的函数`num`次

使用后面的模板代码开始写吧~

## 参数

* operation: 一个函数, 无参数, 无返回值
* num: 代表了调用`operation`的次数

## 资源

* https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Functions_and_function_scope
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/prototype

## 提示

* 不要想得太复杂，实现的代码应该很简单
* 用循环是可以的，但是如果用递归就更好了
* 你可能会看见一些输出，那是我们传给你的那个函数里面的
* 你不需要用`console.log`打印任何东西

## 模板

```js
function repeat(operation, num) {
  // 这里写你的代码
}

// 不要删除下面这一行
module.exports = repeat
```
