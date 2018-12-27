# Object

---

* [创建对象的三种方法](#创建对象的三种方法)
* [Object内置属性](#object内置属性)
* [Object内置方法](#object内置方法)
* [setter/getter](#settergetter)

## 创建对象的三种方法

* 通过字面量创建
* 通过构造函数创建（使用new function\_name\(\)创建）
* 通过Object.create\(\)方法创建

一、通过字面量创建对象

```JavaScript
var o = {};
var student = {name:"xiaoming",age:12};
```

二、通过构造函数创建

```JavaScript
function Student(){
}

var student = new Student();
```

三、通过Object.create\(\)方法创建

```JavaScript
// 以匿名对象{}为原型创建一个对象
var o = Object.create({});

// 以o1为原型创建一个对象。属性值与o1相同。
var o1 = {name:"zhang3",age:20};
var o2 = Object.create(o1);
```

## Object内置属性

* constructor
* propertype

1、构造函数 constructor

```JavaScript
var a = {x:1,y:2};
// 结果： [Function: Object]
console.log(a.constructor);

function B(argument) {
}
var b = new B();
console.log(b.constructor); // 结果： [Function: B]
console.log(b.prototype); // 结果：undefined
```

2、原型 propertype

## Object内置方法

* Object.defineProperty

* Object.getOwnPropertyDescriptor

* Object.create

* Object.getPrototypeOf

* Object.assign

* Object.toString

```JavaScript
var a = {
    x: 1,
    y:2,
};

//为对象a定义一个属性 "z"
Object.defineProperty(a,"z",{
    value: 6,
});

// 获取对象a的属性"z" 结果为
/*
{ value: 6,
  writable: false,
  enumerable: true,
  configurable: true 
}
*/
console.log(Object.getOwnPropertyDescriptor(a,"z"));
```

## **setter/getter**

```JavaScript
// 对象a定义了一个属性z
var a = {
    x: 1,
    y:2,

    set z(o){
    },
    get z(){
        return this.x+this.y
    }
};

a.z = 8; // 不能赋值了
console.log(a.z) // 调用get方法获取值，结果为3
/* 结果：
{ get: [Function: get z],
  set: [Function: set z],
  enumerable: true,
  configurable: true 
}
*/
console.log(Object.getOwnPropertyDescriptor(a,"z"));
```



