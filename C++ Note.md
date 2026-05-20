
+ const 引用不能传入普通引用形参中  
```cpp
void fun(int& x) { }

int a = 10;
const int &b = a;
fun(b);   // 编译报错
```

- 普通引用可以传入 const 引用形参中
```cpp
void fun(const int& x) { }

int a = 10;
int &b = a;   // b 是普通引用
fun(b);       // 合法！
```

- 如果不是引用就可以相互传，但是引用只有普通传入const，所以如果不涉及修改的话形参都用 const，这样会有更好的兼容性