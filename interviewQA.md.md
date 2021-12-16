HTML:
    Q:对HTML语义化的理解？
    A:让开发者页面结构清晰,更好的阅读，方便维护，利于SEO

    Q:<!DOCTYPE>的作用？
    A:告诉浏览器按照何种规范解析

    Q：盒模型？
    A：w3c的盒子模型：Element width = width + border + padding
       IE的盒子模型:  Element width = width

    Q:块级元素、行内元素、行内块元素
    A:
    block:DIV,P,H,nav,ul,li，独占一行，能设置宽高，margin和padding均对其有效；
    inline：设置宽高无效，不会自动换行，margin上下无效；
    inline-block：能改宽高，不自动换行

CSS:
    Q:什么是BFC?

JS:
    Q:原型
    A:
    var foo = new Foo()
    foo.__proto === Foo.prototype
    Foo.prototype.__proto__ === Object.prototpye
    Object.prototpye.__proto__ === null
    -------------------------------------
    Foo.prototype.constructor === function Foo()
    function Foo().prototype === Foo.prototype
    function Foo().__proto__ === Function.prototype
    Function.prototype.constructor === function Function()
    function Function().prototype === Function.prototype.constructor
    function Function().__proto__ === Function.prototype
    Function.prototype.__proto__ === Object.prototpye
    -----------------------------------------------
    Object.prototpye.constructor === function Object()
    function Object().prototype === Object.prototpye.constructor
    function Object().__proto__ === Function.prototpye

    Q:闭包
    A:一个函数访问了另一个函数的变量就导致那个变量不会被垃圾回收机制清除

    Q：JS垃圾回收机制
    A：标记清楚，函数中的变量进入执行环境时标记上，离开后
