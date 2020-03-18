# day02

### Ep01 git使用

- 先拉取再提交

- ~~rm -rf从删库到跑路~~
### Ep02课前预习

> 变量
>
> > 数据类型
> > > 整型型
> > > 浮点型
> > > 字符型
> > > 变量的名字
>
> 常量
>
> > 字面值常量：宏定义（使用方式）
>
> 内存布局（计组相关？）
>
> > 进制转换（详细）
> >
> > 补码（负数）
> >
> > 大端法和小端法
> >
> > 浮点型编码
> >
> > 字符型编码
>
> 编译过程

### Ep03 编译过程

- 调试办法：设置断点 || 用F10单步调试(VS逐语句)  ||  VS逐过程

- 静态语言

  > C C++ Java go 

- 区别编译错误

  > error双击时会直接跳转到错误行
  >
  > 连接错误不会

- 一个项目可有多个main.c

- main.c----->main.obj（完成编译 待链接）---->main.exe(可运行)

- 代码----> 编译---->链接--->运行

- 程序运行

  > 进程的地址空间（整理 在pdf中）
  >
  > 
  >
  > | 左对齐 | 右对齐 |
  > | :----:| :---: |
  > | 栈空间 | 单元格 |
  > | 代码段 | 单元格 |
  > 
  > dd

### Ep04变量

- 命名方法

  > 区分大小写  注意命名规范

- 内存布局

  > 进制转换（详细）
  >
  > > 进制赋值（整理 在pdf中）
  > >
  > > > 1. 赋值8进制：  0开头
  > > > 2. 赋值16进制：0x开头
  > >
  > > 进制转换（整理 在pdf中）
  > >
  > > > math：早上课件补充笔记
  >
  > 补码（负数）
  >
  > > 原理（整理 在pdf中）
  > >
  > > > cpu只能做加法 负数用补码实现
  > >
  > > 负数为补码存储 为正数的取反加一
  > >
  > > > e.g. 5-> 0000 0101
  > > >
  > > >    	-5->1111 1011
  > >
  > > 有符号和无符号（整理 在pdf中）
  > >
  > > > 最高位来代表数据
  > > >
  > > > 
  >
  > 大端法和小端法
  >
  > > 仅整型/浮点型存在大小端问题
  > >
  > > 高位在前就是大端，低位在前就是小端
  > >
  > > 无优劣 知道排序即可
  >
  > > > 浮点型编码（整理 在pdf中）计算花时间
  > > >
  > > > > 不可用==来判断  会出现转换值出错的现象
  > > >
  > > > 字符型编码
  > >
  > > 
  > >
  > > 

### Ep04

- 数据类型

  > 浮点型（在部分输出情况时会出现精度丢失）
  >
  > > ```
  > > #include<iostream>
  > > int main(){
  > > 	float a = 1.23456789e10;
  > > 	//此处会造成精度丢失 应用double
  > > 	b = a+20;
  > > 	cout<<"a ="<< a << "b = "<<b<<endl；
  > > 	return 0;
  > > }
  > > ```
  >
  > 字符型 ：ASCⅡ表
  >
  > > 部分符号 字符 
  > >
  > > 
  > >
  > > 大写~小写差32 
  > >
  > > 大写的A为65 小写的a为97
  > >
  > > - 转义字符
  > >
  > >   - \n	换行（C++ 用endl）
  > >
  > >   - \t	横向跳格
  > >
  > >   - \r	回车
  > >
  > >   - \\\	反斜杠
  > >
  > >   - \b	退格
  > >
  > >   - \0	空字符 区别 空类型（void）
  > >
  > >   - \ddd
  >
  > 字符数组
  >
  > > - 需要多一个来塞结束符  

- 混合运算

  > - 短字节->长字节	不需要强制类型转换
  >
  > - 长字节->短字节	需要强制类型转换
  >
  > - 数值按照int运算
  >
  > - 移位运算符
  >
  > > - 数值在运算时候为四个字节运算
  > > 
  > 	  > ```C++
  >     >   > char a,b,c;          0x93 二进制为 1001 0011 0x93
  > 	b = 0x93;                   左移为 0010 0110 0x26
  > 	  > //c = b <<1>>1;此时c为0x93   右移为 0001 0011 0x13
  > 	  > a = b<<1; //此时a为0x26
  > 	  > c = a>>1; //此时c0x13
  > 	  > ```
  >
  > - 防止运算时数值溢出：在计算之前进行强制类型转换
  > - 在混合多种数据时：等号两边的类型要自己用强制类型转换



