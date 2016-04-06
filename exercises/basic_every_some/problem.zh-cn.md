# 任务

写一个函数接收一个合法user数组,返回一个函数(如果这个函数接收到的user数组全部存在于合法user数组中,就返回true,否则返回false)

你只需要检查id是否匹配

## 例子

```js
var goodUsers = [
  { id: 1 },
  { id: 2 },
  { id: 3 }
]

// `checkUsersValid` 是你要定义的函数
var testAllValid = checkUsersValid(goodUsers)

testAllValid([
  { id: 2 },
  { id: 1 }
])
// => true

testAllValid([
  { id: 2 },
  { id: 4 },
  { id: 1 }
])
// => false
```

## 参数

* goodUsers: 一个合法用户的列表

使用Array#some 和 Array#every检查传入到你返回函数中的每个用户,是否都在合法用户列表中

## 条件

* 不要使用for/while循环或者Array#forEach
* 不要创建多余的函数

## 资源

* https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Array/every
* https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Array/some

## 模板

```js
function checkUsersValid(goodUsers) {
  return function allUsersValid(submittedUsers) {
    // 代码写在这里
  };
}

module.exports = checkUsersValid
```
