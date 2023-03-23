# leetcode-note

## C++ Grammer

### set
https://blog.csdn.net/yas12345678/article/details/52601454

### priority_queue
https://blog.csdn.net/weixin_36888577/article/details/79937886

### 字符切割

1. split

#include<sstream>  
string mytext("some-text-to");  
istringstream iss(mytext);  
string token;  
while(getline(iss, token, '-')){  
   cout<<token<<endl;  
}  
//对输入缺省换行  
string token;  
while(getline(cin, token)){  
   cout<<token<<endl;  
}  
//同一个iss先清空再str  
istringstream iss(str1);  
iss.clear();  
iss.str(str2);  



## Python Grammer

### list
https://www.runoob.com/python/python-lists.html

### 函数传值 & deep copy& deep deepcopy
https://developer.aliyun.com/article/373361

### heapq（优先队列）
https://blog.csdn.net/qq_38048756/article/details/123899066?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_baidulandingword~default-0-123899066-blog-79042839.pc_relevant_3mothn_strategy_and_data_recovery&spm=1001.2101.3001.4242.1&utm_relevant_index=2  

### dictionary 
https://www.runoob.com/python/python-dictionary.html
   
   dic = {a:1, b:2, c:3}
   if(a in dic)
   if(d not in dic)
   dic.keys() // get [a, b, c]
   del dic[a]
   del dic
   
堆
时间复杂度：
插入/删除元素/初始化 O(n)
排序 O(nlogn)

### counter
https://www.jianshu.com/p/615bcc4a0124

### join方法
eg:
  symbol = "-";
  seq = ("a", "b", "c"); # 字符串序列
  print symbol.join( seq );
  
### reverse方法

reversed(seq)
参数
seq -- 要转换的序列，可以是 tuple, string, list 或 range。
返回值
返回一个反转的迭代器。
https://blog.csdn.net/gymaisyl/article/details/83785853
   
## Algorithms

### Binary Search:

https://www.cnblogs.com/grandyang/p/6854825.html

### / 和 // 区别

/ 表示浮点数除法，返回浮点结果;

// 表示整数除法，返回不大于结果的一个最大的整数

#### 关于求中点可能的越界问题：

Let us now stress the fact that pivot = (left + right) // 2 works fine for Python3, which has arbitrary precision integers, but it could cause some issues in Java and C++.

If left + right is greater than the maximum int value 2^31-1, it overflows to a negative value. In Java, it would trigger an exception of ArrayIndexOutOfBoundsException, and in C++ it causes an illegal write, which leads to memory corruption and unpredictable results.

Here is a simple way to fix it:
pivot = left + (right - left) / 2;

and here is a bit more complicated but probably faster way using the bit shift operator.
pivot = ((unsigned int)left + (unsigned int)right)) >> 1;


