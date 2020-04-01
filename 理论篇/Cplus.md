# CPlus 开发指南

### Chapter 01

##### 基本技巧

参数传递的不同方式

- 值传递
- 引用传递
- 常量引用传递

```c++
// 普通值传递
template<class T>
T abc(T a,T b,T c){
    return a+b*c;
}
// 引用传递
template<class T>
T abc(T& a,T& b,T& c){
    return a+b*c;
}
// 常量引用传递
template<class T>
T abc(const T& a,const T&b,const T&c){
    return a+b*c;
}
```

```

函数或者方法返回的不同方式

- 值返回
- 引用返回
- 常量引用返回
```

模板函数

重载函数（根据函数的签名进行判断）

抛出异常

- 0 除数、非法参数值、非法输入值、数组下标越界
- 基类 exception(bad_alloc,bad_typeid)

动态存储空间分配

- 操作符 new
- 一维数组
- 操作符 delete (用来释放由操作符 new 所分配的空间)

```c++
int *y;
*y=new int(10);
// 一维数组指针
float *x=new float[n]; // 如果分配失败，报错bad_alloc

delete y; // 删除指针
delete []x; // 删除数据
```

二维数组

```c++
// 二维数组声明方式
char (*c)[5];
c=new char[n][5];
// 二维字符数组声明方式
char ** x;

template<class T>
bool make2dArray(T **&x,int rows,cols){
    x=new T*[rows];
    for(int i=0;i<cols;i++){
        x[i]=new int [cols];
    }
    return true;
}
```

自有数据类型

- 类 currency
