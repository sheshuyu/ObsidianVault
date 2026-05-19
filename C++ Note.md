+ const 引用不能传入普通的形参中  
比如 
void fun(int& x) { }

int a = 10;
const int &b = a;
fun(b);   // 编译报错