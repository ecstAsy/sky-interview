<h3 align='center'>闭包</h3>

* 闭包就是能够读取其他函数内部变量的函数。

```js
function _getNum() {
  var a = 0;
  function add() {
     a++;
     console.log(a);
  }
  return add
}

var getNum = _getNum();
getNum();                     //  1
getNum();                     //  2
getNum();                     //  3
.                             //  .
.                             //  .
```