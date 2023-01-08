# leetcode-note

## C++ Grammer

### set
https://blog.csdn.net/yas12345678/article/details/52601454


## Python Grammer

### list
https://www.runoob.com/python/python-lists.html

### 函数传值 & deep copy& deep deepcopy
https://developer.aliyun.com/article/373361

## Algorithms

### Binary Search:

https://www.cnblogs.com/grandyang/p/6854825.html


#### 关于求中点可能的越界问题：

Let us now stress the fact that pivot = (left + right) // 2 works fine for Python3, which has arbitrary precision integers, but it could cause some issues in Java and C++.

If left + right is greater than the maximum int value 2^31-1, it overflows to a negative value. In Java, it would trigger an exception of ArrayIndexOutOfBoundsException, and in C++ it causes an illegal write, which leads to memory corruption and unpredictable results.

Here is a simple way to fix it:
pivot = left + (right - left) / 2;

and here is a bit more complicated but probably faster way using the bit shift operator.
pivot = ((unsigned int)left + (unsigned int)right)) >> 1;


