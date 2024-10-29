string类型也可以使用push_back(), .begin(), .end()等函数和迭代器

string中的拼接，最好使用+=。如果直接使用s = s + temp，相当于另外拷贝一份s，极大占用内存

Class中使用相当于全局变量功能的类变量，似乎会延长运行时间？

unordered_map 和 unordered_set 都使用默认的std::hash来计算key，而std::hash无法处理pair类型，因此不能使用unordered_map<pair<int, int>>等类型

使用广度优先搜索（BFS）时，在将待搜索节点添加进队列（queue）时，就应该设置对应的visited数组为true

C++类（class）中的元素默认是私有（private）的

以下代码可以起到按空格分词的作用

```C++
string s="hello world, how are you?";

stringstream ss(s);
string word;

while(ss>>word){
    cout<<word<<endl;
}
```

位运算的优先级比加减低

`ios::sync_with_stdio(false);` 和 `cin.tie(nullptr);` 这两个语句通常用于优化输入/输出（I/O）性能，特别是在处理大量I/O的场合。这种优化通常只在处理大量I/O时才有意义，并且它可能会使程序的行为与预期不符，特别是在混合使用C和C++的I/O函数时。因此，在不需要大量I/O的场合，或者需要确保C和C++的I/O函数一致性的场合，最好不要使用这种优化。
