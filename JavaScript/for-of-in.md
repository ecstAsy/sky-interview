<h3 align='center'>for of 和 for in 的区别</h3>

* for of 和 for in 的区别

    - __for of__: 遍历可迭代对象定义要迭代的值

    - __for in__: 任意顺序迭代对象的 *可枚举属性*

```js
Object.prototype.objCustom = function() {};
Array.prototype.arrCustom = function() {};
let iterable = [3, 5, 7];
iterable.foo = 'hello';

for (let i in iterable) {
  console.log(i); // 0, 1, 2, "foo", "arrCustom", "objCustom"
}

for (let i in iterable) {
  if (iterable.hasOwnProperty(i)) {
    console.log(i); // 0, 1, 2, "foo"
  }
}

for (let i of iterable) {
  console.log(i); // 3, 5, 7
}
```