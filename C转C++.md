#Cpp 

#  1. 内联函数
内联函数是函数，这一点是肯定的。
通过“内存膨胀”的方式，以空间换取时间。提高程序运行的时间。
节约了程序的出栈、入栈时间。

特点：
1. 调用和一般的函数相同；
2. 通过“内存膨胀”实现；
3. 一般内部的代码太过复杂，不建议使用内联函数；
4. 代码简单，但是使用的次数较多，建议使用内联函数；

```cpp
/* 内联函数 调用和普通函数一样*/
inline
void func(int num){
    cout << "num = " << num;
}

int main()
{
    func(5);
    return 0;
}
```

#  2. 函数重载
在同一个项目中定义的函数名字可以重复
1. 函数名称必须一致
2. 函数的参数列表不同
```cpp
/* 两个func,名称一样，入参不一样 */
void func(void) {
    cout << "function without any parameter" << endl;
}

void func(int num1, int num2){
    cout << "num1 + num2 = " << num1 + num2 << endl;
}

int main()
{
    func();
    func(4,6);
    return 0;
}
```
输出
```txt
function without any parameter
num1 + num2 = 10
```


#  3. 函数参数缺省

