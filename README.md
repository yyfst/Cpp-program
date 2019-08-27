# Cpp-program
C++程序设计原理与实践
===
<details>
<summary>1.相邻单词重复检测</summary>
	
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
</details>



为`char`类型的变量赋一个负数值时，打印该变量没有任何符号显示

文字常量又称为“字面常量”，包括数值常量、字符常量和符号常量。其特点是编译后写在代码区，不可寻址，不可更改，属于指令的一部分。
