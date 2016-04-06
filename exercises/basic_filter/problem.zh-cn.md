# 任务
使用 Array#filter 写一个叫 `getShortMessages`的函数

`getShortMessages` 接收一个对象数组,其中的对象有 '.message' 属性,返回一个字符串数组,其中的message都小于50个字符

这个函数需要返回一个字符串数组直接包含那些message,*也就是说去掉他们外层的对象*

## 参数

* messages: 一个数组包含随即的10-100 个对象,就像下面那样: 

```js
{
  message: 'Esse id amet quis eu esse aute officia ipsum.' // random
}
```

## 条件

* 不要用for/while循环或者Array#forEach
* 不要创建多余的函数

## 提示

* 你可以链式调用几个Array的方法

## 例子

```
[ 'Tempor quis esse consequat sunt ea eiusmod.',
  'Id culpa ad proident ad nulla laborum incididunt.',
  'Ullamco in ea et ad anim anim ullamco est.',
  'Est ut irure irure nisi.' ]
```

## 资源

* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map

## 模板

```js
function getShortMessages(messages) {
  // 你的代码写在这里
}

module.exports = getShortMessages
```
