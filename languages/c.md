# C 中文速查表

## main() 主函数

* main() 函数是程序的起点：int main(int argc，char * argv [])
* main() 函数的返回类型是一个整数（int类型），它被称为程序的返回值。
* main() 函数的返回值为0表示运行成功，而非零表示错误。

## Include Files

* 这些文件的目的是告诉编译器源代码将使用的外部函数的存在。

## 预处理程序指令

指令|含义
:---|:---
\#include "mine.h"|                      首先搜索当前工作目录
\#include <stdio.h>|                     搜索命令行目录系统
\#define TRUE 1|                         宏替换，通常使用大写字母
\#define min(a,b) (a<b)?(a):(b)|         带参数的宏替换
\#define abs(a) (a<0)?(-(a)):(a)|        宏替换函数
\#define note /* comment */|             每次出现注释时都会插入此注释
\#undef TRUE|                            取消定义先前定义的宏
\#error|                                 此时停止编译
\#if 表达式|                             条件编译，如果表达式成立则编译
\#elif 表达式|                           else if expression！= 0编译以下代码
\#else|                                  否则编译以下代码
\#endif|                                 条件编译结束
\#ifdef 宏功能名|                         形如#if，如果宏被定义则编译
\#ifndef|                                形如#if, 如果宏未被定义则编译
\#line number [filename]|                设置__LINE__和__FILE__的原点
\#pragma|                                给出了编译器命令

## 创建并执行一个程序

## 在Linux系统: 
    1. 打开终端
    2. 创建程序：nameProgram.c
    3. 编写程序并保存
    4. 命令行执行：gcc -o nameExecutable nameProgram.c

## 32 Reserved words

术语|            描述
:---|:---
auto|            可选的本地声明
break|           用于退出循环并用于退出开关
case|            switch中的选项
char|            字符类型的声明
const|           无法更改的变量的前缀声明
continuego|      到for,while或do-while循环的底部
default|         switch中的最后一项选择；如果case中的情况都不满足，则执行default
do|              可执行语句，do-while循环
double|          双精度浮点类型的声明
else|            可执行语句，“if”结构的一部分
enum|            枚举类型的声明
extern|          前缀声明，含义为：变量/函数在外部定义
float|           单精度浮点类型的声明
for|             可执行语句，for循环
goto|            在函数内跳转到标签
if|              条件判断语句声明
int|             整数类型的声明
long|            前缀声明适用于多种类型
register|        将变量保存在寄存器中的前缀声明
return|          函数值返回语句
short|           前缀声明适用于多种类型
signed|          某些变量的默认的前缀声明，表示这个变量是有符号的
sizeof|          运算符应用于变量和类型，以字节为单位返回大小
static|          静态变量前缀声明
struct|          结构体声明
switch|          可执行选择语句
typedef|         为现有类型创建新类型名称
union|           声明位于相同内存位置的变量
unsigned|        表示这个变量是无符号的前缀声明
void|            无类型变量的声明
volatile|        前缀声明意味着变量可以随时更改
while|           可执行循环语句，while循环或do-while循环

## Basic types

Type|            Description
:---|:---
char|            character type, usually one byte ( a string is array of char )
int|             integer type, usually 2 or 4 bytes ( default )
float|           floating point type, usually 4 bytes
double|          floating point type, usually 8 bytes
void|            no type, typeless
enum|            enumeration type ( user defines the type name )

## Type modifiers, prefix for basic types

Modifiers|       Description
:---|:---
signed|          has a sign ( default )
unsigned|        no sign bit in variable
long|            longer version of type (short or long alone means short int or
short|           shorter version of type long int because int is the default)
const|           variable can not be stored into


## Storage Types

Prefix|          Description
:---|:---
auto|            local variable ( default )
static|          permanent when function exits, not auto
volatile|        can change from outside influence
extern|          variables are defined elsewhere, externally
register|        assign variable to register

## Operators

    ( )     grouping parenthesis, function call
    [ ]     array indexing, also  [ ][ ]  etc.
    ->      selector, structure pointer  
    .       select structure element     
    !       relational not, complement, ! a  yields true or false
    ~    	bitwise not, ones complement, ~ a
    ++  	increment, pre or post to a variable
    --   	decrement, pre or post to a variable
    -   	unary minus, - a
    +    	unary plus,  + a
    *    	indirect, the value of a pointer,  * p is value at pointer p address
    &    	the memory address, & b is the memory address of variable b
    sizeof  size in bytes,   sizeof a     or  sizeof (int)
    (type)  a cast, explicit type conversion,  (float) i, (*fun)(a,b), (int*)x
    *   	multiply, a * b
    /   	divide, a / b
    %    	modulo, a % b
    +    	add, a + b
    -    	subtract, a - b
    <<   	shift left,  left operand is shifted left by right operand bits
    >>   	shift right, left operand is shifted right by right operand bits
    <    	less than, result is true or false,  a %lt; b
    <=   	less than or equal, result is true or false,  a <= b
    >    	greater than, result is true or false,  a > b
    >=   	greater than or equal, result is true or false, a >= b
    ==   	equal, result is true or false,  a == b
    !=   	not equal, result is true or false,  a != b
    &    	bitwise and,  a & b
    ^   	bitwise exclusive or,  a ^ b
    |    	bitwise or,  a | b
    &&  	relational and, result is true or false,  a < b && c >= d
    ||      relational or, result is true or false,  a < b || c >= d
    ?    	exp1 ? exp2 : exp3  result is exp2 if exp1 != 0, else result is exp3
    =    	store
    +=   	add and store
    -=   	subtract and store
    *=   	multiply and store
    /=  	divide and store
    %=      modulo and store
    <<=  	shift left and store
    >>=  	shift right and store
    &=   	bitwise and and store
    ^=   	bitwise exclusive or and store
    |=   	bitwise or and store
    ,    	separator as in   ( y=x,z=++x )


## Operator precedence
                
    More precedence
    LR	( ) [ ] -> . x++ x--
    RL	! ~ - + ++x --x * & sizeof (type)
    LR	* / %
    LR	+ -
    LR	<< >>
    LR	< <= > >=
    LR	== !=
    LR	&
    LR	^
    LR	|
    LR	&&
    LR	||
    RL	? :
    RL	= += -= *= /= %= >>= <<= &= ^= |=
    LR	,
    Less precedence

## Conditional branching
```C
if (condition)
    statement;
else
    statement_2;            /* optional  else  clause */

Switch statement

switch ( expression )      /* constants must be unique              */
{
    case constant_1:       /* do nothing for this case              */
        break;
    case constant_2:       /* drop through and do same as constant_3*/
    case constant_3:
        statement_sequence  /* can have but does not need  { }       */
        break;
    case constant_4:
        statement_sequence  /* does this and next */
                                    /* statement_sequence also*/
    case constant_5:
        statement_sequence
        break;
    default:               /* default executes if no constant equals*/
        statement_sequence  /* the expression. This is optional      */
}
```
## Function definition
```C
type function_name(int a, float b, const char * ch,...) { function_body }

/* only parameters passed by address can are modified*/ 

/* in the calling function, local copy can be modified*/

char * strcpy( char * s1, const char * s2 ) { statements }

Declarations forms

basic_type variable;

type variable[val][val]...[val]={data,data,...};  /*multidimensional array*/

struct struct_name {     /* struct_name is optional */
     type variable_1;    /* any declaration */
     …                   /* all variable names must be unique*/
} variable_1, ... ;      /* variables are optional */

struct struct_name {          /* struct_name is optional */
     type variable_1: length; /* any declaration : length in bits */
         ...					        /* type is int, unsigned or signed */
} variable_1, ... ;           /* variables are optional, they can also be arrays and pointers */


union union_name {            /* union_name is optional */
    type variable_1;          /* variable_1 overlays variable_2 */
    type variable_2;
        ...
} variable_a, ...;            /* variables are optional */

enum enum_type                /* enum_name is optional */
  { enumeration_name_1,       /* establishes enumeration literals */
    enumeration_name_2=number,/* optional number, */
      ...                     /* default is 0, 1, 2, ... */
  } variable, ...;            /* variables are optional */

 /* use dot notation to select a component of a struct or union */
```
