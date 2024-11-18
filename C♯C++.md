---
share: "true"
---

#### 高级特性

Property 属性 对字段的包装器，通常由 get 和 set 访问器组成。+static 可以作为lazy的实现。

Attribute 特性 在语言特性上规范了宏定义和开发中的Obsolete等，以及serializable等类似rust的trait

Reflection 运行时访问对象的内容和属性

匿名函数 底层实现可以使用仿函数模拟捕获+函数地址封装

转换运算符

dynamic_cast 上行转换

const_cast 改变`const`或`volatile`

static_cast 基本转换

reinterpret_cast 重新解释，整数指针互转

#### 关键字

abstract 标识一个可以扩展但不能被实体化的、必须被实现的类或方法，指示某个类只能是其他类的基类。

delegate，事件event，Action，Func

delegate 指定一个声明为一种委托类型。安全的函数指针。event 对委托类型的限定。

可以支持多播multicast（+=, -=）使用Invoke调用

Action和Func可以理解为系统定义好的带泛型的delegate。Action是无返回值的，Func是有返回值的。

extern 修饰符用于声明在外部实现的方法。extern 修饰符的常见用法是在使用 Interop 服务调入非托管代码时与 DllImport 属性一起使用。

interface 接口定义了所有类继承接口时应遵循的语法合同，对声明实现该接口的对象订立一个必须实现哪些行为的契约。

mutable 突破const限制，在const成员函数仍能被当做mutable。

override + virtual 继承时限制函数为基类virtual函数，如果名称相同但函数签名不同则会报错

overload 对同一个类不同类型参数的同名函数（例子：运算符重载）

如果没有限制override，可能会发生overwrite的情况 基类函数被隐藏，表现为根据类型调用相应函数 

**任何条件下都要禁止重新定义继承而来的非虚函数。**
[C++中的Overload、Override和Overwrite - VictoKu - 博客园 (cnblogs.com)](https://www.cnblogs.com/kuliuheng/p/4107012.html)

partial class 用于将一个类、结构体或接口的定义拆分为多个部分分散在不同文件，最终在编译时会合并成一个整体。

unsafe 标注包含指针操作的代码块、方法或类。

volatile 标识一个可被操作系统、某些硬件设备或并发线程修改的attribute。

#### 闭包

按值捕获，按引用捕获

动态语言可以通过闭包延长生命周期，rust中则需要特化生命周期描述