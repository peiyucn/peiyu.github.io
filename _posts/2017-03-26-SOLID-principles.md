---
layout: post
title: S.O.L.I.D.类设计原则
date: 2017-03-26 21:10:00.000000000 +08:00
tags: tech
---

> 本文是由敏捷宣言签署人之一、《 Clean Code(代码整洁之道)》一书的作者Robert C. Martin为他的《Applying Principles and Patterns》这本书搜集整理而来。

### 单一责任原则(SRP)

只有一个理由去修改一个类。例如，如果一个业务规则的改变会导致这个类的修改，那么，数据库、界面、报表格式或系统任何其它的部分的改变都不该迫使这个类做修改。

### 开发/关闭原则(OCP)

软件构成(类，模块，方法等)向扩展行为开放，向修改行为关闭。

### Liskov替换原则(LSP)

子类必须能够用来当作基类使用。如果类A继承类B，任何能使用A的地方，B也同样可以使用。例如，是否还记得，正方形可以看作是矩形！当进行扩展时：前提条件不许绕过，后置条件不能放宽限制，可见常量不能被修改。常量：在扩展之前或之后，用户都需要依靠这个常量来传递信息。正确的使用set形式的继承关系。不遵守set语义是非常危险的。归纳：使用超类的引用的任何上下文中也可以使用其子类的引用替代。这个原则极大的限制了在纯扩展(继承)机制里可以做的事情。不遵守会带来风险。

### 接口分离原则(ISP)

一个类对另一个类的依赖应该限制在最小化的接口上。

### 反向依赖原则(DIP)

依赖抽象层(接口)，而不是具体类。

## 其它重要原则

### Demeter定律

也被称做封锁信息原则：只跟朋友交流

一个对象O的任何一个方法M只能调用下列类型的对象的方法：

* 它自己
* 它的参量
* 它创建/实例化的对象
* 它的直接组件对象

### 好莱坞原则

不要调用我，我会调用你的。

### 不要自我重复(DRY)

去掉重复代码。

### 对接口编程，而不是对实现

反向依赖的另外一种说法。

### 你不需要它(YAGNI)

不要添加你“认为以后可能有用”的代码。只在“事到临头”时才添加代码。

### 简单化，傻瓜化(KISS)

让它能工作的最简单的方法是什么？