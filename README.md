# interview_questions
面试时 被问到的问题汇总


# 企业面试

## iOS面试

1、 weak原理

* 1、weak的原理在于底层维护了一张weak_table_t结构的hash表，key是所指对象的地址，value是weak指针的地址数组。
* 2、weak 关键字的作用是弱引用，所引用对象的计数器不会加1，并在引用对象被释放的时候自动被设置为 nil。
* 3、对象释放时，调用clearDeallocating函数根据对象地址获取所有weak指针地址的数组，然后遍历这个数组把其中的数据设为nil，最后把这个entry从weak表中删除，最后清理对象的记录。
* 4、文章中介绍了SideTable、weak_table_t、weak_entry_t这样三个结构，它们之间的关系如下图所示。


2、 内存管理

引用计数（Reference counting）是一个简单有效管理对象生命周期的方式。
当我们新建一个新对象时候，它的引用计数+1，当一个新指针指向该对象，将引用计数+1。当指针不再指向这个对象时候，引用计数-1，当引用计数为0时，说明该对象不再被任何指针引用，将对象销毁，进而回收内存。



3、 多线程





4、 Runtime

5、 Runloop




## flutter面试

1、flutter渲染Widget、Element 和 RenderObject
widget 树和 Element 树节点是一一对应关系，每一个 Widget 都会有其对应的 Element，但是 RenderObject 树则不然，只有需要渲染的 Widget 才会有对应的节点


2、状态管理


3、 WidgetFul
