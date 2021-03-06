# JS的执行环境

## 宿主环境

JavaScript 代码的运行一般都是在一个 **宿主环境** 中，常见的有 浏览器 和 Node.js

宿主环境会通过 **JS 引擎**（比如 V8）提供 JavaScript 的执行环境

在执行代码之前，首先需要创建一个供代码解析的初试环境，初始化的内容可能包括：

* 一套与宿主环境相关的 API 和 内置对象
* JS 引擎内核的初始化，相关的语法规则和命令等
* 。。。

不同的 宿主环境 和 JS引擎 所定义的初始化环境是不同的

这就是 **兼容性问题** 的根本所在。在最开始，各家浏览器厂商之间的标准各不相同，造成了大量的兼容性问题

这也促使了之前所说的 [标准](../规范/) 的诞生

## JavaScript 虚拟机

JavaScript引擎 也可以称作 JavaScript 虚拟机

可以简单地把 JavaScript 虚拟机理解成是一个翻译程序，将人类能够理解的编程语言JavaScript，翻译成机器能够理解的机器语言

虚拟机通过模拟实际计算机的各种功能来实现代码的执行，如模拟实际计算机的 CPU、堆栈、寄存器等，虚拟机还具有它自己的一套指令系统

所以对于 JavaScript 代码来说，V8 就是它的整个世界，当 V8 执行 JavaScript 代码时，你并不需要担心现实中不同操作系统的差异，也不需要担心不同体系结构计算机的差异，你只需要按照虚拟机的规范写好代码就可以了

### V8

V8 是JavaScript 虚拟机的一种

V8 是 JavaScript 的实现，在学习 V8 工作原理时，需要格外关注 JavaScript 这些独特的设计思想和特性背后的实现

比如，为了实现函数是一等公民的特性，JavaScript 采取了基于对象的策略；再比如为了实现原型继承，V8 为每个对象引入了 \_\_proto\_\_  属性

**后面的编译原理都将以 V8 的基础**

### 主流的JS引擎

Safari / JavaScriptCore（Apple）

Firefox / SpiderMonkey（Mozilla）

Chrome / V8（Google）



