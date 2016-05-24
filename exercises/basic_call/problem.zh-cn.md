
JavaScript中可以实现鸭子类型. 鸭子类型是一种动态类型的风格即:一个对象的方法和属性决定了它的语义(而不是它继承的某个class或实现的某个接口决定的). 这个概念的名称来源于James Whitcomb Riley的鸭子测试,具体内容为:

"当我看见一只鸟,它走起来像个鸭子,游泳像个鸭子,叫起来像个鸭子,那我就叫它鸭子."

在JavaScript中,为了写出健壮的代码,我们有时需要检查一个对象是否符合我们需要.
我们可以用Object#hasOwnProperty来判断一个对象是否`有`一个自己定义的属性(而不是继承自prototype)

```js
var duck = {
  quack: function() {
    console.log('quack')
  }
}

duck.hasOwnProperty('quack') // => true
```

我们没有给duck对象定义`hasOwnProperty`方法,它从哪来呢?

duck对象是用`{}`这个字面量表示法创建的,所以这个`hasOwnProperty`继承自Object.prototype:

```js
var object = {quack: true}

Object.getPrototypeOf(object) === Object.prototype // => true
object.hasOwnProperty('quack')                     // => true
```

但是如果一个对象不继承自Object.prototype呢?

```js
// 创建一个继承自 'null' prototype的对象
var object = Object.create(null)
object.quack = function() {
  console.log('quack')
}

Object.getPrototypeOf(object) === Object.prototype // => false
Object.getPrototypeOf(object) === null             // => true

object.hasOwnProperty('quack')
// => TypeError: Object object has no method 'hasOwnProperty'
```

我们仍然可以通过某种方式让这个对象也使用`hasOwnProperty`

Function#call允许我们调用任何方法并传入一个可选的`this`

```js
// the first argument to call becomes the value of `this`
// 第一个参数作为
// the rest of the arguments are passed to the function as per
// 剩余的参数作为

Object.prototype.hasOwnProperty.call(object, 'quack') // => true
```

# 任务:

写一个`duckCount`函数,接收很多个对象,返回直接含有`quack`属性的对象的个数(而不是从原型链上继承的`quack`)

例子:

```js
var notDuck = Object.create({quack: true})
var duck = {quack: true}
duckCount(duck, notDuck) // 1
```
## 参数

* 你可以传0-20个参数,每个参数都可以任意类型或含有任意属性.其中的一些含有`quack`属性

## 条件

* 不要使用for/while循环或Array#forEach
* 不要创建保存数量的变量
* 不要创建不必要的工具方法

## 提示

* `arguments`变量在每个方法中都可用,是一个类似Array的Object

```js
{
  0: 'argument0',
  1: 'argument1', // etc
  length: 2
}
```

## 资源

* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/call
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwnProperty
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/in
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice#Array-like
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions_and_function_scope/arguments


## 模板

```js
function duckCount() {
  // SOLUTION GOES HERE
}

module.exports = duckCount
```
