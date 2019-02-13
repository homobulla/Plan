- **基础JS-Api**，判断是不是整数，对数组的操作：增删改查（查重），重组，排序，数组打乱、这些都要求能手写代码,当然这些都有好几种方式实现
- 创建对象、New运算符、事件流（冒泡和捕获）、原生事件绑定、BOM操作（比如对Ie9一下浏览器的判断和一些操作）
- 原型原型链、闭包、类与继承（在class之前的实现继承，构造函数继承、原型链继承、组合方式继承，各自优缺点）、同步异步
- es6/7/8的新特性，基础指令、箭头函数、字符串模板、promise(原理，运用的场景)、面向对象、数据格式（set/map）,async/await(原理，有个cto问我这个函数用babel打包后长什么样子)....
- 模块化、函数式编程，高阶函数的使用，柯里化函数，递归...

## [ES 基础知识点与高频考题解析](https://sunlei4076.gitbooks.io/web/content/Web%20前端面试指南与高频考题解析/1一面%201：ES%20基础知识点与高频考题解析.html)

- 变量类型
  - JS 的数据类型分类和判断
  - 值类型和引用类型
- 原型与原型链（继承）
  - 原型和原型链定义
  - 继承写法
- 作用域和闭包
  - 执行上下文
  - this
  - 闭包是什么
- 异步
  - 同步 vs 异步
  - 异步和单线程
  - 前端异步的场景
- ES6/7 新标准的考查
  - 箭头函数
  - Module
  - Class
  - Set 和 Map
  - Promise

### 变量类型

6种原始值：`Boolean String Number Null Undefined Symbol`

引用值：`Object`

#### 对值类型的判断

`typeof`只能判断原始值，引用值除了`function`其他都是`object`,`typeof null`的结果是`object`，`typeof Symbol()`的值是`symbol`

一般判断引用类型可以使用`instanceof`来判断其构造器

```js
let somefoods = []
somefoods instanceof Array // true
```

或者使用`toString`方法

```js
Object.prototype.toString.call([]) // "[object Array]"
```

### 原型和原型链

- **所有的引用类型（数组、对象、函数），都具有对象特性，即可自由扩展属性（null除外）**
- **所有的引用类型（数组、对象、函数），都有一个__proto__属性，属性值是一个普通的对象**
- **所有的函数，都有一个prototype属性，属性值也是一个普通的对象**
- **所有的引用类型（数组、对象、函数），__proto__属性值指向它的构造函数的prototype属性值**

>  原型和原型链的问题需要好好看一下

