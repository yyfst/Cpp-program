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
