---
title: "JS面试题"
date: 2023-04-11T14:38:33+08:00
draft: false
---

## 1.JavaScript中的数据类型

共8种：Number、String、Boolean、Object、null、undefined、Bigint、Symbol

其中，**Object**为引用类型(Array、Date、function)，其余为基本数据类型。

## 2.Promise

Promise是ES6新增的一种对象，表示异步操作的结果。

## 3.async和await

ES2017新增了两个关键字async和await，用于异步JavaScript编程。

await常常放在一个会返回Promise的函数前面，任何使用await的代码都是异步的。

## 4.map()和forEach()

都是用于遍历数组的方法，区别在于：

forEach()对数组的每个元素执行一次回调函数，没有返回值，仅仅是遍历数组。

```
arr = [1, 2, 3, 4];
 arr.forEach((num) => {
 console.log(num * 2); // 输出2 4 6 8
});
```

map()方法会对数组的每个元素执行一次回调函数，并将回调函数的返回值组成一个新的数组返回，不会修改原数组。

```
arr = [1, 2, 3, 4]; 
const newArr = arr.map((num) => {
    return num * 2; 
});
console.log(newArr); // 输出[2, 4, 6, 8]
```

## 5.

### 参考资料

《JavaScript权威指南第7版》
