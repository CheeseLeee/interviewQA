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
    A:

计算机网络:
    Q:http和https的区别
    A：http是明文传输数据的，https是http+ssl（secure sockets layer）两种协议，对数据进行了加密，也就是应用层是http，安全层是ssl，传输层，网络层，数据链路层，端口号是443，http是80。https会比http慢一点，因为握手会比较费时。


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
    A：标记清除，函数中的变量进入执行环境时标记上（标记的方式有很多种），离开后清除；
       引用计数，IE使用，可能会出现循环引用的问题
    
    Q:谈谈Promise
    A:Promise契约，是异步编程的一种方案，promise对象有三种状态，pending,fulfilled,rejected,只有异步操作的结果能改变Promise对象的状态，改变后就这个状态就冻结（没办法二次改变）,promise实例上有then，catch方法去处理resolove,reject的回调，Promise构造函数有all，race等方法。

    Q：谈谈async和await
    A：我的理解是他是Generator函数或promise的语法糖，async声明异步，这个函数会返回一个promise对象，awaite可以看作是generator的yiled，,遇到await就暂停执行，后面应该跟一个promise对象，接着就是根据后面promise对象的结果来回调then或者catch了

Vue.js
    Q：谈谈MVVM和MCV吧
    A：MVC的话，M是model逻辑数据层，V是view视图，C是控制器。我理解的是比方说用户input输入信息，这时候就这个input是C控制器，然后控制器把数据通知给逻辑和去手动修改页面也就是v，C得去把数据传输到逻辑层和视图层。
      MVVM的话，就是多了一层vm，在vue里的话，vue就是作为这个vm。实现了双向绑定，此时的input就是view，改了会通过vm通知model，相反model改了也会去通知view，实现了不用手动操作dom，只用关心视图层的交互。但是也有一个说法是vue并非全是MVVM，因为ref还是可以获取dom的。
    
    Q：nextTick
    A：当要用到最新的html数据的时候，就用nextTick，原理是vue内部模仿了一个事件循环，异步更新组件，把相同的Watcher只添加进一个进队列，然后下次个事件循环开始的时候清空并执行这个队列里的方法，

    Q：
