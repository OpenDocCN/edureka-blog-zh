# 如何在 C++中实现优先级队列

> 原文：<https://www.edureka.co/blog/priority-queue-in-cpp>

优先级队列是 STL 中的一个容器。它类似于 queue，只是优先级队列的每个元素都有一定的优先级，当我们从优先级队列中弹出元素时，优先级最高的元素会首先弹出。像优先级队列一样，在 [STL](https://www.edureka.co/blog/stl-in-cpp/) 中有 10 种不同类型的容器。容器是存储数据的对象。STL 容器是在模板类的帮助下实现的，因此定制它来保存不同类型的数据是很容易的。在本帖中，我们将详细讨论优先级队列及其相关概念。以下指针将在 C++文章优先级队列中讨论:

*   [STL 的组件](#ComponentsofSTL)
*   [堆和优先级队列](#HeapsandPriorityqueue)
*   [打印 C++中优先级队列的所有元素](#PrintingalltheelementsofPriorityQueue)

继续这篇关于 C++中优先级队列的文章

## **STL 的组件**

STL 由模板类和函数组成，它们可以用作存储和处理数据的标准方法。让我们讨论一下 STL 的组成部分

**容器-**STL 中定义了 10 种类型的容器，这些容器分为 3 类。在这 3 个队列中，优先级队列属于派生容器的类别。每个容器类都有自己的一组函数，可以用来操作数据。

**算法**–算法是一种用于处理容器对象中存在的数据的方法。STL 提供了许多不同类型的算法，可用于初始化，搜索，排序，合并，复制。算法是借助模板函数实现的。

**迭代器-** 迭代器是指向容器中元素的对象。迭代器有助于遍历容器的内容。迭代器就像指针一样，可以递增和递减。它充当算法和容器之间的链接。迭代器用于操作存储在容器中的数据。

继续这篇关于 C++中优先级队列的文章

## **堆和优先级队列**

正如我们前面看到的，优先级队列属于派生容器的范畴。这个类别的其他成员是堆栈和队列。这些派生容器也称为容器适配器。

堆栈、队列和优先级队列被称为派生容器，因为它们是由不同的序列容器组成的。这些容器不支持任何类型的迭代器，它们不用于数据操作。

**什么是优先级队列？**

简单地说，它是一个我们用来存储数据的容器。存储数据的每个元素都被赋予一定的优先级，这有助于我们按照逻辑顺序存储数据。语法:`priority_queue variable_name;`

为了使用优先级队列，在程序中包含一个头文件是很重要的。

![priority queue in c++](img/ac492a288f00cf9ccdda88602be45ff5.png)例如，如果我们使用 push 函数在优先级队列中添加 2，10，30，5，6，然后使用 pop 函数弹出这些元素，输出将是 30，10，6，5，2。

好了，现在我们知道了优先级队列的用途。但是它怎么知道 30 是否大于 10 呢？它在做某种排序吗？在这一点上，成堆的问题出现了。要详细了解堆，请参考本文。

堆-堆是树状结构。根据子元素节点相对于父节点在堆中的排列方式，堆被细分为两个部分

1.**最小堆-** 在最小堆中，父节点的值小于或等于子节点的值。

2. **Max Heap-** 在 Max Heap 中，父节点的值大于等于子节点的值。

**注-** 优先级队列不使用某种排序算法对元素进行排序，而是以堆的形式存储数据。

继续这篇关于 C++中优先级队列的文章

## **打印优先级队列的所有元素**

理解了优先级队列的基本原理之后，让我们通过实现程序来理解优先级队列最常用的方法

```
#include <iostream>
#include<queue>
using namespace std; 

int main () 
{ 
    priority_queue <int> Prior_q; 
    Prior_q.push(10); 
    Prior_q.push(30); 
    Prior_q.push(6); 
    Prior_q.push(2); 
    Prior_q.push(15);
    Prior_q.push(9);
    Prior_q.push(7);

    while (Prior_q.empty() == false) 
    { 
        cout << Prior_q.top() << " "; 
        Prior_q.pop(); 
    } 

    return 0; 
}
```

**输出:**

`30 15 10 9 6 2`

在上面的程序中，我们使用了 pop()、top()和 push()函数，这些函数在处理优先级队列时经常使用。让我们来看看一些可以用于优先级队列的方法

这个函数返回优先级队列的大小

**empty( ):** 该函数用于检查优先级队列是否为空。如果优先级队列为空，则返回 true。

**push( ):** 在优先级队列中插入一个元素。

**pop( ):** 该函数删除优先级队列中优先级最高的元素。

**swap( ):** 这个函数将优先级队列的元素与另一个优先级队列交换。该函数将优先级队列作为参数。

这个函数用于将一个元素添加到优先级队列的顶部。

让我们再看一个节目。

```
#include <iostream>
#include<queue>
using namespace std; 

int main () 
{ 
    priority_queue <int> Prior_q; 
    Prior_q.push(10); 
    Prior_q.push(30); 
    Prior_q.push(6); 
    Prior_q.push(2); 
    Prior_q.push(15);
    Prior_q.push(9);
    Prior_q.push(7);

    while (Prior_q.empty() == false) 
    { 
        cout << Prior_q.top() << " "; 
        Prior_q.pop(); 
    } 

    return 0; 
}
```

**输出:**

`2 6 7 9 10 15 30`

至此，我们结束了 C++文章中的优先级队列。如果你想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。