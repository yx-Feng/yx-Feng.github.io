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

## 5.ES6新增特性

**（1）新增了一种数据类型symbol，**

每个symbol类型的值都是唯一的。

```
let a = Symbol('test')
let b = Symbol('test')
a == b // false
```

**（2）新增let和const两个声明变量的关键字**

let和const声明的变量具有块级作用域。
const如果声明的变量是基本数据类型的，一旦声明就不能改变。
但如果声明的是引用数据类型，能改变。

```
const obj = {
    name: 'Tom',
    age: 16
};
obj.sex = male;
```

**（3）解构赋值**

是对赋值运算符的扩展，把 "=" 右边的对象或数组的值取出来，然后赋给左边的变量。

```
let [a,b,c] = [1,2,3];
```

**（4）新增Map对象和Set对象**

Map对象用来保存键值对，Set对象用来存储一组不重复的值。

```
let demo = new Map([['name', 'Tom'], ['age', 12]);  // 可以接受一个二维数组来创建Map对象
demo.set('sex', 'male'); // {'name' => 'Tom', 'age' => 12}
demo.get('name');
```

**（5）对象的扩展运算符（...）**

```
let obj = {name:'ren',age:12};
let another = {sex:'male'};
let someone = {...person,...another};//合并对象
console.log(someone);//{name:'ren',age:12,sex:'male'}
```

**（6）箭头函数**

```
let add = (a, b) => {
    return a+b;
}
let fn = a => a*a; // 只有一个参数,括号可以省略
```

## 6. 数组常用方法

**push()**：向数组的末尾添加一个或多个元素，并返回新的长度。
**pop()**：删除并返回数组的最后一个元素。
**shift()**：删除数组的第一个元素，并返回第一个元素的值。
**unshift()**：向数组的开头添加一个元素，并返回新的长度。
**sort()**：对数组进行排序。
**reverse()**：颠倒数组中元素的顺序。
**slice(start,end)**：数组截取。
**filter()**：过滤数组。

```
let arr = [1,4,6,8,10]
let result = arr.filter(function(curValue) {
    return curValue>5;
})
console.log(result); // [ 6, 8, 10 ]
```

**map()**：遍历数组，对数组的每个元素执行一次回调函数，并将回调函数的返回值组成一个新的数组返回。

### 参考资料

《JavaScript权威指南第7版》
