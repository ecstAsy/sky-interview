<h3 align='center'>箭头函数</h3>

* 作用
  - 更简短的函数
  ```js
  // ES5
  const add = function (a, b) {
    return a + b
  }
  // ES6
  const add = (a, b) => a + b
  ```
  - 箭头函数没有prototype属性。
  - 不绑定this 
    - 如果是该函数是一个构造函数，this指针指向一个新的对象
    - 在严格模式下的函数调用下，this指向undefined

