# Cpp-program
C++程序设计原理与实践
===

>1.相邻单词重复检测


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

