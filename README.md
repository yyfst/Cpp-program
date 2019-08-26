# Cpp-program
C++程序设计原理与实践
===

><summary>1.相邻单词重复检测</summary>


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

