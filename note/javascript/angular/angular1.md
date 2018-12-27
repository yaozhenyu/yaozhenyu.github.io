# Angular 1.x

## 全局变量

1，通过var 直接定义global variable，这跟纯js是一样的。

2，用angularjs value来设置全局变量 。

3，用angularjs constant来设置全局变量 。

4，用angularjs rootscope来设置全局变量 。

5、定义服务。

6、$rootScope。

7、定义一个服务 来传 值:

```JavaScript
var test2 = 'tank';         //方法1，定义全局变量  

var app = angular.module('app', [  

  'ngRoute',  

  'phonecatControllers',  

  'tanktest'  

]);  

app .value('test',{"test":"test222","test1":"test111"});  //方法2定义全局变量  
app .constant('constanttest', 'this is constanttest');    //方法3定义全局变量
```

## 创建一个module

```JavaScript
// 第一个参数:模块名，第二个参数：引入其他模块
var app = angular.module("app",[module1,module2]);
```

## 创建一个controller

```JavaScript
app.controller("controller_name",function($scope){
    $scope.var1 = {};
});
```



