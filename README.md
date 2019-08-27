# Cpp-program &emsp;C++程序设计原理与实践

## 笔记    

1. 相邻单词重复检测
	
```cpp
  string p = "";
  string s;
  while (cin >> s)
  {
    if (s == p)
      cout << "repeat：  " << s << endl;
    p = s;
  }
```

2. 为`char`类型的变量赋一个负数值时，打印该变量没有任何符号显示

 ## 第3章 对象、类型和值

* ### 思考题
 ---

1.&ensp;术语prompt的含义是什么？  
>提示符的意思，在代码中输出一段提示信息，称为提示符.

2.&ensp;哪种操作符用于读取值并存入变量中？  
>`>>`，如`cin>>a`，表示将输入的信息存入a中.

4.&ensp;`\n`的名称是什和它的目的是什么？   
>`\n`是换行符，用于增加一个新行.

8.&ensp;对象是什么？  
>对象是用来保存指定类型值的内存单元.

9.&ensp;文字常量是什么？  
>文字常量又称为“字面常量”，其特点是编译后写在代码区，不可寻址，不可更改，属于指令的一部分.

10.&ensp;C++中有哪几种文字常量？
>文字常量包括数值常量、字符常量和符号常量.    
>* 数值常量  
>包括整型常量和实型常量。整型常量指常整数，有十进制、八进制、十六进制三种表示形式。实型常量包括单精度浮点数（float）、双精度浮点数（double）和长双精度浮点数（long double），表示形式有科学计数法和非科学计数法。
```cpp
  int x=10;            //10为数值常量中的整型常量
  float y=11.2;        //11.2为数值常量中单精度实型常量
  double z=2.5e4;      //2.5e4表示的值为2.5×10^4，是数值常量中双精度实型常量
```
>* 字符常量  
>指ASCII字符，有128个，分为普通字符和转义字符。普通字符指可直接书写的字符，如’a’和’b’。转义字符指不能直接书写的特殊字符，需要使用反斜杠进行表示，比如’\t’表示水平制表符，’\v’表示垂直制表符  

>* 符号常量  
>用标识符代表一个常量，使用之前必须定义。例如宏定义和枚举元素  
```cpp
  #define LENGTH 100 //LENGTH为符号常量，100为整型常量
  enum Week{MON, TUES, WED, THU, FRI};   //SUN,MON等均为符号常量
```

11.&ensp;变量是什么？  
>变量就是命名过的对象

12.&ensp;一个`char`、`int`和`double`的典型大小是多少？  
>`char`:1个字节(8位);
>`int`:4个字节(32位);
>`double`:8个字节(64位)

15.&ensp;定义是什么？  
>定义就是为对象分配内存空间

17.&ensp;什么是字符串连接，如何使它在C++中正确工作？  
>C++中使用符号`+`来实现字符串连接，例如：  
```cpp
  string s1="hello";
  string s2="world";
  string s3=s1+s3;
```
>则`s3 = helloworld`，即：`+`号后面的字符串`s2`会连接到`+`前面的字符串`s1`后面

21.&ensp;什么是类型安全，为什么它是重要的？  
>每个对象在定义时被分配一个类型。对于一个程序或程序的一个部分，如果使用的对象符合它们规定的类型，那么它们是类型安全的。但是很多操作不是类型安全的，比如使用了未初始化的变量
```cpp  
  int x;
  int y=x+1;
```
>这里的x没用初始化，并且使用了它，所以程序会出现错误，这个操作就不是类型安全的

23.&ensp;请定义一个协助判断从一种类型到另一种类型的转换是否安全的规则。
>* 安全类型转换  
>一个值从一种类型转换为另一种类型过程中没用信息丢失，即转换前后值不变
>* 不安全类型转换  
>一个值从一种类型转换为另一种类型过程中发生信息丢失，即转换前后值改变


 ## 第4章 计算

* ### 思考题
 ---
1. 什么是计算？    


2. 什么是计算的输入和输出？举例说明。  

3. 当表示计算的时候，程序员需要谨记哪三项要求？    
>正确，简单，高效

4. 什么是表达式？  
>表达式是程序最基本组成单元。表达式就是通过一系列操作来计算一个数值量。最简单的表达式是字面常量，如`10`,`'a'`,`3.14`和`Norah`.  
变量也是一种表达式

5. 在本章内容中，表达式和语句有什么区别？  

6. 什么是左值？列出要求用左值的运算符。为什么这些运算符需要使用左值？  
>C++11中，将所有的值划分左值和右值，左值指的是可以取地址、有名称的对象；繁殖不能取地址、没用名称的就是右值，右值又分为纯右值、将亡值。例如：  
```cpp
  int z=x+y;
```
>其中x可以取地址`&z`，是左值，表达式(x+y)无法取地址`&(x+y)`，无法通过一个名称找到(x+y),所以该表达式是个右值

7. 什么是常量表达式？

8. 什么是字面常量？

9. 什么是符号常量，我们应该如何使用它？

10. 什么是魔数？举例说明。

11. 哪些运算符既可以用于整型也可以用于浮点型？

12. 哪些运算符只能用于整型而不能用于浮点型？

13. 哪些运算符可以用于字符串？

14. 什么情况下程序员更喜欢用switch语句而不是if语句？

15. switch语句常见的问题有哪些？

16. for循环语句的循环控制中每一部分的功能是什么？它们的执行顺序是怎样的？

17. 什么情况下应该使用for循环？什么情况下应该使用while循环？

18. 如何输出一个字符型数据的ASCII值？

19. 请说明在函数定义中char foo(int x)的含义是什么？

20. 什么情况下你将在程序中定义一个单独的函数？列出原因。

21. 哪些操作可以用于整型数据而不能用于字符串？

22. 哪些操作可以用于字符串而不能用于整型数据？

23. 向量中第三个元素的索引号是多少？

24. 如何用for循环来打印输出向量的所有数据元素？

25. 语句`vector<char> alphabet(26)`;含义是什么？

26. 描述向量中的push_back()的含义。

27. vector的成员函数begin()、end()和size()的功能是什么？

28. 为什么向量被如此广泛的使用？

29. 如何将一个向量中的数据排序？

