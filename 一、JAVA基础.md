# 一、Java语言基础

## 1.1 关键字

### 1.1.1.概述

被java语言赋予特定含义的单词

### 1.1.2.特点

组成关键字的字母全部小写

### 1.1.3.注意事项

1、goto和const作为保留字存在，目前并不适用

2、类似Notepad++ 这样的高级记事本，针对关键字有特色的颜色标记，非常直观

### 1.1.4.练习

1、判断下列哪些是关键字

> class,HelloWorld,public,static,void,main,String System

2、答案：

> class,public,static,void

3、注意：

> main不是关键字，颜色没有变，虽然也被虚拟机识别，但main只是一个名称

### 1.1.4关键字表

![1](F:\01、java基础\笔记的截图图片\1.png)

![2.关键字](F:\01、java基础\笔记的截图图片\2.关键字.png)

## 1.2.标识符

### 1.2.1.概述

> 给类，接口，方法，变量等起名字时使用的字符序列

### 1.2.2.组成规则

> 1、英文大小写字母

> 2、数字字符

> 3、$和_

### 1.2.3.命名规则（见名知意）

1、包（其实就是文件夹，用于解决相同类名问题）

> 全部小写：test,cn.test



2、类或者接口

> 每个单词的首字母必须大写：Student,Dog,HelloWorld

3、方法和变量

> 一个单词：首字母小写（main,age,name）

> 多个单词：从第二个单词开始，每个单词的首字母大写（studentAge，showAllNames）

4、常量

> 一个单词，全部大写：PI

> 多个单词，每个字母大写，用_隔开：MAX_AGE



### 1.2.4.注意事项

> 1、不能以数字开头

> 2、不能是Java中的关键字

> 3、区分大小写

### 1.2.5.练习

> 下面那些合法，那些不合法
>
> HelloWorld,DataClass,_983,$bS5_c7,class,DataClass#,98.3,Hell World

> 不合法答案：
>
> class：关键字
>
> DataClass#：不能用#
>
> Hell World：不能有空格

## 1.3.注解

### 1.3.1.概述

> 用于解释说明程序的文字

### 1.3.2、分类格式

> 单行注释：//注释文字

> 多行注释： /* 注释文字  */

> 文档注释：/** 注释文字  **/

### 1.3.3、注释的作用

> 1、解释说明程序，提高程序的阅读性

> 2、可以帮助我们调试程序。

### 1.3.4、注意

> 1:对于单行和多行注释，被注释的文字，不会被JVM（java虚拟机）解释执行。

> 2:对于文档注释，是java特有的注释，其中注释内容可以被JDK提供的工具 javadoc 所解析，生成一套以网页文件形式体现的该程序的说明文档

## 1.4、常量

### 1.4.1、概述

> 在程序执行的过程中，其值不可以发生改变

### 1.4.2、常量的分类

> 1、字符串常量：用双引号括起来的内容（“hello”，“world”）

> 2、整数常量：所有的整数（100,200）

> 3、小数常量：所有的小数（10.2,100.3）

> 4、字符常量：用单引号括起来的单个内容（‘a','A','0'）

> 5、布尔常量：只有true和false两个值

> 6、空常量：null

## 1.5、进制

### 1.5.1、概述

> 进制就是进位制，二进制就是逢二进一，八进制就是逢八进一，十进制就是逢十进一，十六进制就是逢十六进一

### 1.5.2、二进制，八进制，十进制，十六进制图解

> 二进制

![3.二进制图解](F:\01、java基础\笔记的截图图片\3.二进制图解.png)

> 八进制：用二进制表达数据的表型形式有点长，所以想要简化一下

![4.八进制图解](F:\01、java基础\笔记的截图图片\4.八进制图解.png)

> 十六进制

![5.十六进制图解](F:\01、java基础\笔记的截图图片\5.十六进制图解.png)

> 总结：进制越大，表现形式越短

### 1.5.3、不同进制的表现形式

> 二进制：有0,1组成。以0b开头

> 八进制：由0,1，...7组成，以0开头

> 十进制：由0,1，...9组成，整数默认是十进制

> 十六进制：由0,1，...,9,a,b,c,d,e,f(大小写均可)组成，。以0x开头

### 1.5.3、练习

> 分别输出:0b100,0100,100,0x100，在通过计算器验证结果。

> 结果：
>
> 0b100=1*2^2+0 * 2^1+0*2^0=4，
>
> 0100=1^8^2+0 * 8^1+0*8^0=64，
>
> 100=1*10^2+0 * 10^1+0*10^0=100，
>
> 0x100=1*16^2+0 * 16^1+0*16^0=256

### 1.5.5、任意进制到十进制转换图解(位权展开法)

![6.任意进制到十进制转换图解(位权展开法)](F:\01、java基础\笔记的截图图片\6.任意进制到十进制转换图解(位权展开法).png)

#### 1.5.5.1、练习

> 得到下面数据的十进制
>
> 0b10101=1 * 2 ^ 4+1 * 2 ^2 +1=21
>
> 0123=1 * 8 ^ 2+2 * 8 ^1+ 3=83
>
> 0x3c=3 * 16^1+12 * 16^0=60

### 1.5.6、十进制到任意进制转换图解

![7.任意进制到十进制转换图解(位权展开法)](F:\01、java基础\笔记的截图图片\7.任意进制到十进制转换图解(位权展开法).png)

#### 1.5.6.1、练习

> 52分别得到二进制，八进制，十六进制
>
> 二进制：110100
>
> 八进制：64
>
> 十六进制：34



### 1.5.7、快速的进制转换法（8421法）

![8.快速的进制转换法](F:\01、java基础\笔记的截图图片\8.快速的进制转换法.png)

#### 1.5.7.1、练习

> 1、0b1011001转到八进制
>
> 八进制进制：0b1011001 = 64+16+8+1=89=0131（先从二进制转到十进制，再到8进制）

![9.快速的进制转换法练习](F:\01、java基础\笔记的截图图片\9.快速的进制转换法练习.png)

> 注意：
>
> 使用方式二，八进制是3位一组，十六进制是4位一组，不够补0

## 1.6、原码，反码，补码

### 1.6.1、概述

> 在计算机中，有符号数有三种表示法：原码、反码和补码。所有数据的运算都是采用补码进行的。

![10.讲解源码补码反码](F:\01、java基础\笔记的截图图片\10.讲解源码补码反码.png)

### 1.6.2、原码

> 就是二进制定点表示法，即最高位为符号位，“0”表示正，“1”表示负，其余位表示数值的大小。

![11.源码](F:\01、java基础\笔记的截图图片\11.源码.png)

### 1.6.3、反码

> 正数的反码与其原码相同；负数的反码就是对其原码逐位取反，但是符号位除外

![12.反码](F:\01、java基础\笔记的截图图片\12.反码.png)

### 1.6.4、补码

> 正数的补码与其原码相同；负数的补码是在其反码的末位+1.

![13.补码](F:\01、java基础\笔记的截图图片\13.补码.png)



### 1.6.5、练习

> 已知某数X的源码为10110100B，求X的补码和反码

![14.反码补码源码练习1](F:\01、java基础\笔记的截图图片\14.反码补码源码练习1.png)

> 2、已知某数X的补码11101110B，试求其源码

![15.反码补码源码练习2](F:\01、java基础\笔记的截图图片\15.反码补码源码练习2.png)

## 1.7、变量

1.7.1、概述及格式

> 概述：在程序的执行过程中，其值可以在一定范围内发生改变的量

> 格式：数据类型 变量名 = 初始化值 ;

![16.变量的概述和格式](F:\01、java基础\笔记的截图图片\16.变量的概述和格式.png)

## 1.8、数据类型

### 1.8.1、概述和分类

> 概述：Java语言是强类型语言，对于每一种数据都定义了明确的具体数据类型，在内存总分配了不同大小的内存空间



> 分类

![17、数据类型](F:\01、java基础\笔记的截图图片\17、数据类型.png)

> 声明long类型常量要在后面加“L”或者“l”，声明float，要在后面加“F”或者f

> 整数默认的是int类型
>
> 浮点类型默认double类型



### 1.8.2、注意 

> 1、作用域：变量定义在哪一级大括号中，他就在这个大括号内有效，并且在同一个大括号内，不能同时定义同名的变量。

![18.变量作用域](F:\01、java基础\笔记的截图图片\18.变量作用域.png)

> 2、初始化值：没有初始化值的变量不能直接使用。只要在使用前给值就行，不一定非要在定义的时候立即给值。

> 3、在一行上建议只定义一个变量，可以定义多个，但是不建议

### 1.8.3、数据类型转换

> 一般来说，我们在运算的时候，要求参与运算的数据类型必须一致，
>

![19.两个int类型做加法](F:\01、java基础\笔记的截图图片\19.两个int类型做加法.png)

> 定义一个byte类型，一个int类型做加法

![20.byte，int做加法](F:\01、java基础\笔记的截图图片\20.byte，int做加法.png)

输出的a+b没有错误，输出的c编译错误，可能损失精度

#### 1.8.3.1、默认转换（从小到大的转换）

> 1、byte,short,char-->int-->long->-float-->double

> 2、byte,short,char相互之间不转换，他们参与运算首先转换为int类型

#### 1.8.3.2、图解

> 隐式转换

![21.数据类型的隐式转换](F:\01、java基础\笔记的截图图片\21.数据类型的隐式转换.png)

> 强制转换：从大得数据类型到小的数据类型

> 格式：目标数据类型 变量 = （目标数据类型）（被转换的数据）；

> 注意：不要随意去使用强制转换，因为它隐含了损失精度的问题
>



#### 1.8.3.3、强制转换思考题



> 1、请问下面这个有没有问题
>
> double d=12.345;
>
> float f=d;

这是有问题的，编译时出现问题，有可能损失精度，要把double赋值给float，需要强制类型转换float f=(double)d;

> 2、下面两个定义有没有区别？
>
> float f=(float)12.345;
>
> float f=12.345f;

有区别，第一个是把double类型的数据强转成float类型，float f=12.345f;是声明一个f的变量，并赋值

### 1.8.4、面试题

#### 面试题1

> 1、byte b1=3,b2=4,b;
>
> b=b1+b2;
>
> b=3+4;
>
> 哪句是编译失败的呢，为什么？

> b=b1+b2;编译失败，因为b1+b2变量参与运算会先把b1，b2转换成int的类型（类型提升），然后在计算，最后赋值给b， 把int赋值个byte，编译失败，有可能回损失精度；而3+4是常量，会把3+4的结果计算出来，然后看是否在byte的范围内，在就不报错，不在就报错

#### 面试题2

> byte b=130;有没有问题？如果我想赋值正确，可以怎么做？结果是多少？

> byte的取值范围是-128~127之间，所以编译回出现可能损失精度问题。强制转换就成：byte b=(byte)130;赋值就正确了，结果是-126

![22.轻质类型转换数据溢出的分析](F:\01、java基础\笔记的截图图片\22.轻质类型转换数据溢出的分析.png)

## 1.9、运算

### 1.9.1、字符和整数相加

![23.字符数据参与运算](F:\01、java基础\笔记的截图图片\23.字符数据参与运算.png)

> 通过字符和一个整数相加，我们给出一张ASCII码表，需要记住三个值
>
> <u>***'a'			97***</u>
>
> <u>***'A'			64***</u>
>
> <u>***'0'			48***</u>

### 1.9.2、字符串参与运算

![24.字符串数据参与运算](F:\01、java基础\笔记的截图图片\24.字符串数据参与运算.png)

> 字符串数据和其他数据做+，结果是字符串类型，这里的+不是加法运算，而是字符串连接符，结果是helloa1和98hello

### 1.9.3、注意

> 1、在定义long或者float类型变量的时候要加L或者f，整数默认时候int类型，浮点数默认是double

> 2、byte，short在定义的时候，接收的其实是一个int类型的值

> 3、byte值的问题

![25.byte值的问题](F:\01、java基础\笔记的截图图片\25.byte值的问题.png)

> 4、数据类型转换之默认转换：byte,short,char--int--long--float--double
>
> long:8个字节
>
> float：4个字节
>
> ​	A:他们底层的存储结构不同
>
> ​	B: float表示的数据范围比long大（long:2^63-1,float:3.4*38=2 * 2^114）

> 5、Java语言中的字符char可以存储一个中文汉字吗？为什么
>
> 可以，因为java语言中的字符占用两个字节。java采用unicode编码

## 2.1、运算符

> 概念：对常量和变量进行操作的符号

### 2.1.1、算数运算符

#### 2.1.1.1、基本运算符

> +，-，*，/，%，++，--
>
> 注意事项：1、整数相除只能得到整数，如果想得到小数，必须把数据变化为浮点数据类型
>
> ​					2、“/”获取的是除法操作的商，“%”获取的操作的余数

![26、算数运算符的基本使用](F:\01、java基础\笔记的截图图片\27、++和--的参与操作使用.png)

#### 2.1.1.2、++和--的用法

> ++,--的使用：
>
> ​		1、单独使用：放在操作数的前面和后面效果一样（这种用法是我们比较常见的）
>
> ​		2、参与运算使用：
>
> ​						放在前面，先自增或者自减，然后在参与运算。
>
> ​						放在右面，先参与运算，在自增或者自减

![27、++和--的使用](F:\01、java基础\笔记的截图图片\27、++和--的使用.png)

> ++,--运算符的作用：就是对变量进行自增或者自减

![27、++和--的用法](F:\01、java基础\笔记的截图图片\27、++和--的用法.png)

#### 2.1.1.3、++和--的练习

> 第一题：分别计算出abc的值
>
> ```
> int a=10;
> 
> int b=10;
> 
> int c=10;  
> 
> a=b++;//a=10,b=11,c=10
> 
> c=--a;//a=9,b=11,c=9
> 
> b=++a;//a=10,b=10,c=9
> 
> a=c--;//a=9,b=10,c=8
> ```
>
> 



> 第二题：计算出x,y的值
>
> ```
> int x=4;
> 
> int y=(x++)+(++x)+(x*10);//int y=4+6+60=70
> ```
>
> 



### 2.1.2、赋值运算符

> =，+=，-=，/=，%=，*=

> 面试题：short s=1,s=s+1;short s=1,s+=1;两个代码有没有问题，如果有，哪里有问题？
>
> 有，s=s+1编译会报错，因为s=s+1赋值给s之前会先转成int类型，int类型赋值给short可能会损失精度，s+=1不会报错，因为他其实他隐含了一个强制类型转换，s=(short)(s+1)的形式

### 2.1.3、比较运算符

> ==,！=,<,>,<=,>=

> 特点：无论你的操作是简单还是复杂，结果是boolean类型

> 注意事项：“==”不能写成“=”

### 2.1.4、逻辑运算符

> 特点：一般用于连接boolean类型的表达式或值



> &：与

![28、逻辑运算&](F:\01、java基础\笔记的截图图片\28、逻辑运算&.png)

> |：或--有true则true

![28、逻辑运算-或](F:\01、java基础\笔记的截图图片\28、逻辑运算-或.png)

> ^：异或--相同为false，不同为true

![28、逻辑运算^](F:\01、java基础\笔记的截图图片\28、逻辑运算^.png)

> !：非---非false则true，非true则false

![28、逻辑运算-！](F:\01、java基础\笔记的截图图片\28、逻辑运算-！.png)

> &&：双与（短路）

![29、双与（&&）](F:\01、java基础\笔记的截图图片\29、双与（&&）.png)

> ||：双或（短路），参考&&



> &和&&的区别：最终结果一样，&&具有短路效果，左边是false，右边不执行，&左右边都要执行，&&效率比较高

![30、&&和&的区别](F:\01、java基础\笔记的截图图片\30、&&和&的区别.png)

### 2.1.5、位运算符

> 注意：要做位运算，首先要把数据转换成二进制（还要是补码）

```
<<:左移，左边最高位丢弃，右边补齐0
```

![32、1](F:\01、java基础\笔记的截图图片\32、1.png)

```
>>：右移，最高位是0，左边补齐0，最高位时1，左边补齐1
```

```
>>>：无符号右移，无论最高位是0还是1，左边补齐0，永远都是正号
```

![32、2](F:\01、java基础\笔记的截图图片\32、2.png)

![32、3](F:\01、java基础\笔记的截图图片\32、3.png)

```
&
|
^:位异或--一个数据对另一个数据位异或两次，该数本身不变
~
```

![31、位运算](F:\01、java基础\笔记的截图图片\31、位运算.png)



![31、位运算分析](F:\01、java基础\笔记的截图图片\31、位运算分析.png)

#### 2.1.5.1、位运算面试题

1. 面试题1

   

   ```
   int a=10;
   int b=20;
   System.out.println("a:"+a+"，b:"+b);
   实现整数变量的交换
   方法1：(开发中用)
   int temp =a;
   a=b;
   b=temp;
   
   方式二：(面试用)
   a=a^b;
   b=a^b;
   a=a^b;
   ```

   ![31、位运算的面试题](F:\01、java基础\笔记的截图图片\31、位运算的面试题.png)

   ```
   方式三：
   a=a+b;
   b=a-b;
   a=a-b;
   
   方式四：
   b=(a+b)-(a=b);
   ```

   

2. 面试题2:请用最有效率的方式写出计算2乘以8的结果：

   ```
   2<<3
   ```

   

### 2.1.6、三元(三目)运算符

#### 2.1.6.1、格式

> (关系表示式)？表达式1：表达式2；
>
> 结果是一个boolean类型

#### 2.1.6.2、执行流程

> 根据表达式的计算返回一个true或者false
>
> 如果是true，就把表示式1作为结果，
>
> 如果是false，就把表达式2作为结果。

![33、三目运算](F:\01、java基础\笔记的截图图片\33、三目运算.png)

#### 2.1.6.3、练习

​	1. 获取两个整数中的最大值

```
int x=100;
int y=200;
int max=(x>y?x:y);
```

​	2. 获取三个整数中的最大值

```
int x=1;
int y=2;
int z=3;
int temp=(x>y?x:y)?
int max=temp>z?temp:z;
```



 3. 比较两个数是否相同

    ```
    int a=1;
    int b=2;
    boolean flag=(a==b)
    ```

    

## 3、键盘录入

> 格式：
>
> 1. 导包 import java.util.Scanner;
> 2. 创建键盘录入对象：Scanner sc=new Scanner(System.int);
> 3. 通过对象获取数据：int x=sc.nextInt();

![34、键盘录入](F:\01、java基础\笔记的截图图片\34、键盘录入.png)



3.1.3、键盘录入练习

1. 录入两个数据，并对这两个数据求和，输入结果
2. 录入两个数据，获取最大值
3. 录入三个数据，获取最大值
4. 录入两个数据，比较是否相等。





## 4.1、结构语句

### 4.1.1、顺序结构

> 按照代码的先后顺序，从上往下，依次执行

![35、顺序结构](F:\01、java基础\笔记的截图图片\35、顺序结构.png)

### 4.1.2、选择结构

#### 4.1.2.1、if语句

> 格式1：
>
> ```
> if(关系表达式){
> 	语句体；
> }
> ```

![36、if语句1](F:\01、java基础\笔记的截图图片\36、if语句1.png)

##### 4.1.2.1.1、案例

![36、if语句1-1](F:\01、java基础\笔记的截图图片\36、if语句1-1.png)

##### 4.1.2.1.2、注意事项

1. 关系表达式无论简单还是复杂，结果必须是boolean类型；
2. if语句如果是一条语句，大括号可以省略，如果是多条就不能省略，建议不要省略；
3. 一般来说：有左大括号就没有分好，有分号就没有左大括号；



> 格式2
>
> ```
> if(关系表达式){//true执行该语句体
> 	语句体；
> }else{//false执行该语句体
> 	语句体；
> }
> 执行流程：
>     1、比较表达式的值，看其返回的是true还是false。
>     2、如果是true，就执行语句体1，
>     3、如果是false，就执行语句体2；
> 注意：else后面是没有关系表达式的，只有if右面有。
> ```
>
> ![36、if语句体2](F:\01、java基础\笔记的截图图片\36、if语句体2.png)

![36、if语句体2-1](F:\01、java基础\笔记的截图图片\36、if语句体2-1.png)

##### 4.1.2.1.3、if格式2的练习

1. 获取两个数据中较大的值

```
int a=10;
int b=20;
int max;
if(a>b){
	max=a;
}else{
	max=b;
}
System.out.println("较大数是："+max);

```

 2. 判断一个数据是奇数还是偶数

    ```
    int a =21;
    if(a%2==0){
    	System.out.println("a是偶数");
    }else{
    	System.out.println("a是奇数");
    }
    ```

##### 4.1.2.1.4、if格式2和三元的相互转换问题

> 1. 三元都可以使用if语句实现，反之不成立
> 2. 当if语句控制的操作是一个输出的语句，就不能够使用三元运算符；因为三元操作完毕i就应该有一个结果。

![36、if格式2和三元的相互转换问题](F:\01、java基础\笔记的截图图片\36、if格式2和三元的相互转换问题.png)



> 格式3：
>
> ```
> if(关系表达式1){
> 	语句体1；
> }else if(关系表达式2){
> 	语句体2；
> }
> ...
> else{
> 	语句体n+1;
> }
> ```
>
> 

##### 4.1.2.1.5、if语句格式3案例

![36、if格式3](F:\01、java基础\笔记的截图图片\36、if格式3.png)

##### 4.1.2.1.6、if语句格式3练习

1. 键盘录入x的值，计算出y的值并输出

   ```
   x>=3	y=2x+1;
   -1<=x<3	y=2x;
   x<=-1	y=2x-1;
   
   Scanner sc=new Scanner(System.in);
   int x=sc.nextInt();
   int y;
   if(x>=3){
   	y=2*x+1;
   }else if(x>=-1&&x<3){
   	y=2*x;
   }else{
   	y=2*x-1;
   }
   System.out.println("y:"+y);
   ```

   

 2. 键盘录入月份的值，输出对应的季节

    方法1：

    ```
    Scanner sc=new Scanner(System.in);
    int month=sc.nextInt();
    if(month==3||month==4||month==5){
    	System.out.println(month+"是春季");
    }else if(month==6||month==7||month==8){
    	System.out.println(month+"是夏季");
    }else if(month==9||month==10||month==11){
    	System.out.println(month+"是秋季");
    }else if(month==12||month==1||month==2){
    	System.out.println(month+"是冬季");
    }else{
    	System.out.println("你输入的季节有误");
    }
    ```

    方法2：

    ![36、if格式3练习](F:\01、java基础\笔记的截图图片\36、if格式3练习.png)

    



##### 4.1.2.1.5、if语句分别适合做什么事情

1. 格式1：适合做单个判断
2. 格式2：适合做两个判断
3. 格式3：适合做多个判断
4. if语句的使用场景，针对表达式是一个boolean类型的数据，针对一个范围的判断

#### 4.1.2.2、switch语句（先走case在走default）

##### 4.1.2.2.1、格式：



> ```
> switch(表达式){
> 	case 值1://case：后面跟的是要和表达式进行比较的值
> 		语句体1;//要执行的代码
> 		break;//表示中断，结束的意思，可以控制switch语句的结束
>     case 值2:
>        	语句体2;
>         break;
>      ...
>      default://当所有的值都跟表达式不匹配的时候，就执行default控制的语句，相当于else
>      	语句体n+1;
>      	break;
> }
> 表达式取值：byte，short，int,char
> JDK5以后可以是枚举：enum
> JDK7以后可以是，字符串String
> ```

##### 4.1.2.2.2、执行流程



> 1. 首先计算出表达式的值
> 2. 和case依次比较，一旦有对应的值，就会执行相应的语句，在执行的过程中，遇到break就会结束
> 3. 最后，如果所有的case都和表达式的值不匹配，就会执行default语句体部分，然后结束掉。

##### 4.1.2.2.3、案例

> 键盘录入一个数据，根据这个数据，我们输出对应的星期
>
> 1...星期1，2...星期2。。。。。。。
>
> ```
> Scanner  sc=new Scanner(System.in);
> System.out.println(请输入一个数据（1~7）);
> int week = sc.nextInt();
> switch(week){
> 	case 1:
> 		System.out.pirntln("星期一");
> 		break;
> 	case 2:
> 		System.out.pirntln("星期二");
> 		break;
> 	case 3:
> 		System.out.pirntln("星期三");
> 		break;
> 	case 4:
> 		System.out.pirntln("星期四");
> 		break;
> 	case 5:
> 		System.out.pirntln("星期五");
> 		break;
> 	case 6:
> 		System.out.pirntln("星期六");
> 		break;
> 	case 7:
> 		System.out.pirntln("星期日");
> 		break;
> 	default:
> 		System.out.println("你输入的星期有误");
> 		break;
> }
> ```

##### 4.1.2.2.4、switch使用过程中需要注意的事项

> 1. case 后面只能是常量，不能是变量，而且多个case后面的不能出现相同的；
>
> 2. default可以省略，但是不建议省略，因为他的作用是对不正确的情况给出提示，特殊情况：case就可以把值固定（A，B，C，D）单选按钮；
>
> 3. break可以省略吗？可以，但是结果可能不是我们想要的，会出现一个现象：case穿透，建议不要省略；
>
> 4. **default一定要在最后吗？可以在任意位置；但是建议在最后**
>
> 5. **switch语句的结束条件，遇到break就结束，执行到末尾就结束了**
>
>    

##### 4.1.2.2.5、看程序写结果

```
int x=2;
int y=3;
switch(x){//先走的case，在走default
	default:
		y++;
		break;
	case 3:
		y++;
	case 4:
		y++;
}
System.out.println("y="+y);
System.out.println("==============");

int a=2;
int b=3;
switch(a){
	default:
		b++;
	case 3:
		b++;
	case 4:
		b++;
}
System.out.println("b="+b);
```



> 答案：4和6



##### 4.1.2.2.6、switch语句练习

1. 模拟做单项选择题，根据你的选择，给出对应的答案（表达式是字符的情况）

   ```
   分析：
   	A:出一个选择题，然后供你选择
   	B:键盘录入选择的数据
   	C：根据选择来给出你选择的结论
   	
   //由于现在没有办法键盘录入得到‘A’，“B”，就用65，66替代
   System.out.println("下面的几个人你最爱谁");
   System.out.println("65 林青霞");
   System.out.println("66 张曼玉");
   System.out.println("67 刘德华");
   System.out.println("68 王力宏");
   
   Scanner sc=new Scanner(System.in);
   System.out.println("请输入你的选择");
   int choiceNumber=sc.nextInt();
   char choice=(char)(choiceNumber);
   switch(choice){
   	case 'A':
   		System.out.println("恭喜你选择正确");
   		break;
   	case 'B':
   		System.out.println("选择有误");
   		break;
   	case 'C':
   		System.out.println("选择有误");
   		break;
   	case 'D':
   		System.out.println("选择有误");
   		break;
   	default:
   		System.out.println("没有该选项");
   		break;
   }
   ```

   

2. 键盘录入字符串，根据给定的字符串，来输出你选择的字符串是什么（表达式是字符串）

   ```
   //根据你键盘录入的字符串，判断是否有满足要求的，如果有，就输入，否则提示有误
   Scanner sc=new Scanner(System.in);
   System.out.println("请输入字符串");
   String str=sc.nextLine();
   switch(str){
   	case "hello":
   		System.out.println("你输入的是hello");
   		break;
   	case "world":
   		System.out.println("你输入的是world");
   		break;
   	case "java":
   		System.out.println("你输入的是java");
   		break;
   	default:
   		System.out.println("没有找到你输入的数据");
   		break;
   }
   
   ```

   

3. 用switch语句实现键盘录入月份，输出对应的季节

   ```
   Scanner sc=new Scanner(System.in);
   int month=sc.nextInt();
   System.out.println("输入月份");
   switch(month){
   	case 3:
   	case 4:
   	case 5:
   		System.out.println("pring");
   		break;
   	case 6:
   	case 7:
   	case 8:
   		System.out.println("summer");
   		break;
   	case 9:
   	case 10:
   	case 11:
   		System.out.println("autumn");
   		break;
   	case 12:
   	case 1:
   	case 2:
   		System.out.println("winter");
   		break;
   	default:
   		System.out.println("你输入的月份有误");
   		break;
   }
   ```

   > if语句和switch语句的区别
   >
   > if语句：
   >
   > 	1. 针对结果是boolean类型的判断
   >  	2. 针对一个范围的判断
   >  	3. 针对几个常量值的判断
   >
   > switch语句：
   >
   > ​	1. 针对几个常量值的判断

   

##### 4.1.2.2.3、面试题

###### 面试题1

```
byte可以作为switch的表达式吗，long可以吗，String可以吗？
byte可以，long不可以，String：JDK7以后可以
```



## 4.2、循环结构

### 4.2.1、需求：

> 请在控制台输出10次“HelloWorld“
>
> ```
> System.out.println("HelloWorld");
> System.out.println("HelloWorld");
> System.out.println("HelloWorld");
> ....
> ```

### 4.2.2、循环语句的组成

```
1. 初始化语句：
	一条或多条语句，这些语句完成一些初始化操作
2. 判断条件语句
	这是一个boolean表达式，这个表达式能决定是否执行循环体
3. 循环体语句
	这个部分是循环体语句，也就是我们要多次做的事情
4. 控制条件语句
	这个部分在一次循环体结束后，下一次循环判断题条件执行前执行。
	通过用于控制循环条件的变量，使得循环在核实的时候结束
```

### 4.2.3、for循环语句

#### 4.2.3.1、for循环语句格式

```
for(初始化语句;判断条件语句;控制条件语句){
	循环体语句；
}
执行流程：
	1. 执行初始化语句
	2. 执行判断条件语句
		false：循环技术
		true:继续执行
	3. 执行循环体语句
	4. 执行控制条件语句
	5. 回到步骤2继续
	
```

#### 4.2.3.2、案例

> 在控制台输出10次HelloWorld
>
> ```
> for(int i =0;i<10;i++){
> 	System.out.println("HelloWorld");
> }
> ```
>
> 

#### 4.2.3.3、注意事项

> 1. 判断条件语句无论简单还是复杂，结果是boolean类型
> 2. 循环体语句如果是一条语句，大括号可以省略，但不建议
> 3. 一般来说：有左大括号就没有分好，有分好就没有左大括号

#### 4.2.3.4、for循环练习

> 1. 请在控制台输出数据1-10

```
for(int i =1;i<=10;i++){
	System.out.println(i);
}
```

> 2.  请在控制台输出数据10-1

```
for(int i=10;i<0;i--){
	System.out.pirntln(i);
}
```

> 3. 求出1-10之间数据之和

```
int sum=0;
for(int i=1;i<10;i++){
	sum+=i;
}
System.out.println("sum="+sum);
```

> 4. 求出1-100之间偶数和

```
int sum=0;
for(int i=2;i<=100;i++){
	if(i%2==0){
		sum+=i;
	}
}
System.out.println(sum);
```

> 5. 求出1-100之间奇数和

```
int sum=0;
for(int i=1;i<=100;i++){
	if(i%2!=0){
		sum+=i;
	}
}
System.out.println(sum);
```

> 6. 求5的阶乘

```
int sum=1;

//这里的i其实可以从2开始，从1开始没有意义
for(int i=2;i<=5;i++){
	sum*=i;
}
System.out.println(sum);
```

> 7. 在控制台输出所有的”水仙花数”

```
/*
分析：
	所谓的水仙花数是指一个三位数，其各位数字的立方和等于该数本身。
		举例：153就是一个水仙花数。
		153 = 1*1*1 + 5*5*5 + 3*3*3
*/
for(int i=100;i<=999;i++){
	int ge=i%100;
	int shi=i%10;
	int bai=i%1;
	if(bai*bai*bai+shi*shi*shi+ge*ge*ge==i){
		System.out.println(sxh);
	}
	
}
```

> 8. 统计”水仙花数”共有多少个

```
int sum=0;
for(int i=100;i<=999;i++){
	int ge=i%10;//对10取余；
	int shi=i/10%10;
	int bai=i/10/10%10;
	if(bai*bai*bai+shi*shi*shi+ge*ge*ge==i){
		sum++;
	}	
}
System.out.println(sum);
```

> 9. 请在控制台输出满足如下条件的五位数
>
>    ​	•个位等于万位
>
>    ​	•十位等于千位
>
>    ​	•个位+十位+千位+万位=百位

```
for(int i=10000;i<=99999;i++){
	int ge=i%10;
	int shi =i/10%10;
	int bai =i/10/10%10;
	int qian=i/10/10/10%10;
	int wan =i/10/10/10/10%10;
	if((gei==wan)&&(shi==qian)&&(ge+shi+qian+wan==bai)){
		System.out.println(i);
	}
}
```

> 10. 请统计1-1000之间同时满足如下条件的数据有多少个：
>
>     ​	•对3整除余2
>
>     ​	•对5整除余3
>
>     ​	•对7整除余2

```
int count=0;
for(int i=1;i<=1000){
	if(i%3==2&&i%5==3&&i%7==2){
		count++；
	}
}
System.out.println("共有："+count+"个");
```

### 4.2.4、while循环语句

#### 4.2.4.1、while循环语句格式

> 1. 基本格式
>
>  
>
> ```
> while(判断条件语句){
> 	循环体语句;
> }
> ```
>
> 2. 扩展语句
>
> ```
> 初始化语句;
> while(判断条件语句){
> 	循环体语句;
> 	控制条件语句;
> }
> ```

#### 4.2.4.2、while循环案例

> 输出10次Helloworld

```
int i =1;
while(i<=10){
	System.out.println(i);
	i++;
}
```

#### 4.2.4.3、while练习

> 1. 求出1-100之和

```
int i =1;
int sum=0;
while(i<=100){
	sum+=i;
	i++;
}
System.out.println(sum);
```

> 2. 统计水仙花个数有多少个

```
int i=100;
int count=0;
while(i<1000){
	int ge=i%10;
	int shi=i/10%10;
	int bai=i/10/10%10;
	if((ge*ge*ge+shi*shi*shi+bai*bai*bai)==i){
		count++;
	}
	i++;
}
```

#### 4.2.4.3、for循环和while循环的区别

> 1. 使用区别：如果想在循环结束后，继续使用控制条件的那个变量，就用while循环，否则用for循环，不知道就用for循环。
>
>    ​	A. 因为变量急躁从内存中消失，可以提高内存的使用率
>
> 2. 如果是一个范围的，用for循环，如果不明确要做多少次，就用while循环较为合适
>
>    
>
> 3. 



> 3. 我国最高山峰是珠穆朗玛峰：8848m，我现在有一张足够大的纸张，厚度为：0.01m。请问，我折叠多少次，就可以保证厚度不低于珠穆朗玛峰的高度?

```
分析：
	1. 定义一个统计变量，默认是0；
	2. 最高峰是珠穆朗玛峰：8848m这个是最终的厚度
		现在有一张足够大的纸，厚度为0.01m这个初始厚度
	3. 折叠多少次，就可以保证厚度不低于珠穆朗玛峰的高度
		折叠一次有什么变化呢，就是厚度是以前的2倍
	4. 只要每次变化的厚度没有超过珠穆朗玛峰的高度，就折叠，统计变量++;
	5. 输出统计变量


int end=8848*100
int start=1;
int count=0;
while(start>end){
	count++;
	start*=2;
	System.out.println(start);
}
System.out.println(count);
```

### 4.2.5、do...while循环语句

#### 4.2.5.1、do...while循环格式

> 1.基本格式
>
> ```
> do {
> 	循环体语句;
> }while((判断条件语句);
> 
> ```

> 2. 扩展格式
>
> ```
> 初始化语句;
> do {
> 	循环体语句;
> 	控制条件语句;
> } while((判断条件语句);
> 
> ```



#### 4.2.5.2、do...while循环案例

> 1. 输出10次hello
>
> ```
> int i=1;
> do{
> 	System.out.println(""HelloWorld);
> 	i++;
> }while(i<=10);
> ```

> 2. 求和：1-100
>
> ```
> int i=1;
> int sum=0;
> do{
> 	sum+=i;
> 	i++;
> }while(i<=100);
> ```



#### 4.2.5.3、do...while、for、while三种循环的区别

> 1. do...while至少执行一次循环体，而for，while循环必须先判断条件是否成立，然后决定时候执行循环体语句；
> 2. 那么我们一般使用哪种循环呢？
>    1. 先考虑for，在考虑while，最后考虑do...while

```
int x=3;
while(x<3){
	System.out.println("java");
	x++;
}
int x=3;
do{
	System.out.println("java");
	x++;
}while(x<3);
```



#### 4.2.5.4、注意事项---死循环

> 1. 一定要注意控制条件语句控制的那个变量问题，不要弄丢了，否则就容易死循环。
>
> ```
> int x=0;
> while(x<10){
> 	System.out.println(x);
> 	//没有控制条件语句
> }
> ```
>
> 2. 两种最简单的死循环格式
>
> ```
> while(true){
> 	System.out.println("死循环");
> }
> ```
>
> ```
> for(;;){
> 	System.out.println("死循环");
> }
> ```



### 4.2.6、案例

> 1. 请输出一个4行5列的星星(*)图案
>
> ```
> for(int i=1;i<=4;i++){
> 	for(int j=1;j<=5;j++){
> 		System.out.print("* ");
> 	}
> 	System.out.println();
> }
> ```

> 2. 需求：请输出如下图形
>
>    ```
>    *
>    **
>    ***
>    ****
>    *****
>    
>    
>    for(int i=1;i<=5;i++){
>    	for(int j=i;j<=i;j++){
>    		System.out.print("*");
>    	}
>    	System.out.println();
>    }
>    ```
>
>    

> 3. 九九乘法表
>
> ```
> for(int i=1;i<=9;i++){
> 	for(int j=i;j<=i;j++){
> 		System.out.print(i+" * "+j+" = "+ i*j+"\t");
> 	}
> 	System.out.println();
> }
> ```
>
> ‘\x’：x表示任意，这种做法叫做转义字符
>
> '\t'：tab键的位置
>
> '\r'：回车
>
> '\n'：换行



## 4.3、控制语句结构（控制跳转）

### 4.3.1、break--中断

#### 4.3.1.1、break的使用场景

> 1. 在选择结构switch语句中
> 2. 在循环语句中（循环语句加入了if判断的情况）
>
> 注意：离开使用场景的存在是没有意义的

#### 4.3.1.2、break的作用

##### 4.3.1.2.1、跳出单层循环

> 跳出单层循环
>
> ```
> for(int i=0;i<10;i++){
> 	if(x==2){
> 		break;
> 	}
> 	System.out.println("HelloWorld");
> }
> System.out.println("over");
> ```

##### 4.3.1.2.2、跳出单层循环

> 跳出多层循环
>
> 1. 带标签的跳出
> 2. 格式：标签名：循环语句
> 3. 标签名要符合java的命名规则
>
> ```
> 
> wc:for(int i=0;i<3;i++){
> 	nc:for(int j=0;j<4;j++){
> 		if(j==2){
> 			break wc;
> 		}
> 		System.out.print("* ");
> 	}
> 	System.out.println();
> }
> ```

### 4.3.2、continue--继续

#### 4.3.2.1、continue使用场景

> 1. 在循环语句中
>
> 2. 离开使用场景的存在是没有意义的

#### 4.3.2.2、continue的作用

> 单层循环对比break，然后总结两个的区别
>
> ​	1. break 退出当前循环
>
> 	2. continue 退出本次循环

```
for(int i=0;i<10;i++){
	if(i==3){
		continue;
	}
	System.out.println(i);
}
```

#### 4.3.2.3、填空练习题

```
for(int i=1;i<=10;i++){
	if(i%3==0){
		//在此处填写代码
	}
	System.out.println("Java基础班")
}
我想在控制台输出2次“Java基础班”；break;
我想在控制台输出7次“Java基础班”；continue;
我想在控制台输出13次“Java基础班”；System.out.println("Java基础班");
```



### 4.2.3、return--返回

> return关键字不是为了跳转出循环体，而是跳出方法

```
for(int i=0;i<10;i++){
	if(i==3){
		System.out.println("退出");
		return;
	}
	System.out.println(i);
}
System.out.println("over");
```



### 4.2.4、while语句和break结合练习

> 小芳的妈妈每天给她2.5元钱，她都会存起来，但是，每当这一天是存钱的第5天或者5的倍数的话，她都会花去6元钱，请问，经过多少天，小芳才可以存到100元钱
>
> ```
> //每天存2.5 double money=2.5
> //初始化day day=1;
> //天数是5的倍数：money-6;
> //总数：double totalMoney=100;
> 
> double daySum=0;//天数
> double dayMoney=2.5;//每天要存2.5
> double totalMoney=100;//总共要存的钱
> int dayCount=1;//从第1天开始存钱
> while(true){
> 	//累加钱
> 	daySum+=dayMoney;
> 	if(daySum>=totalMoney){
> 		System.out.println("共花了"+dayCount+"天存了100元");
> 		break;
> 	}
> 	if(daySum%5==0){
> 		daySum-=6;
> 		System.out.println("第"+dayCount+"天共花了6元");
> 	}
> 	//天数变化
> 	dayCount++;
> 	
> }
> ```



## 4.4、方法

### 4.4.1、方法的定义及格式

#### 4.4.1.1、定义

> 方法就是完成特定功能的代码块
>
> 	1. 在很多的语言里面都有函数的定义
>
>  	2. 函数在java中被称为方法

#### 4.4.1.2、格式

> ```
> 修饰符 返回值类型 方法名(参数类型 参数名1，参数类型 参数名2...){
> 	函数体;
> 	return 返回值;
> }
> ```
>
> 方法格式的解释
>
> ```
> 1. 修饰符：比较多，后面会详细介绍，目前是public static；
> 2. 返回值类型：用于限定返回值的数据类型；
> 3. 方法名：一个名称，为了方便我们调用方法；
> 4. 参数
> 	实际参数：就是实际参与运算的
> 	形式参数：就是方法定义上的，用于接收实际参数的。
> 5. 参数类型：限定调用方法时传入参数的数据类型；
> 6. 参数名：是一个变量，接受调用方法时传入的参数；
> 7. 方法体：完成功能的代码；
> 8. return：结束方法以及返回方法指定类型的值；
> 9. 返回值： 程序被return带回的结果，返回给调用者。
> 
> ```
>

#### 4.4.1.3、两个明确

> 1. 返回值类型 ：明确功能结果的数据类型
>
> 2. 参数列表： 明确有几个参数，以及参数的类型

#### 4.4.2.1、两个数据之和的案例

> 求两个数据之和
>
> ```
> public static int getSum(int a,int b){
> 	return a+b;
> }
> public static void main(String args[]){
> 	int result=getSum(4,6);
> 	System.out.println(result);
> }
> ```

#### 4.4.2.1、方法调用的图解

![37、方法调用的图解](F:\01、java基础\笔记的截图图片\37、方法调用的图解.png)



### 4.4.2、有明确返回值的方法练习

> 1. 键盘录入两个数据，返回两个数中的较大值
>
> ```
> public static int getMax(int a,int b){
> 	return (a>b)?a:b;
> }
> public static void main(String args[]){
> 	int max=getMax(5,-2);
> 	System.out.println("max="+max);
> }
> ```

> 2. 键盘录入两个数据，比较两个数是否相等
>
> ```
> public static boolean isEquals(int a,int b){
> 	return a==b;
> }
> public static void main(String args[]){
> 	boolean result=isEquals(5,-2);
> 	System.out.println("result="+result);
> }
> ```

> 3. 键盘录入三个数据，返回三个数中的最大值
>
> ```
> public static int getMax(int a,int b,int c){
> 	int temp=(a>b)?a:b;
> 	return (temp>c)?temp:c;
> }
> public static void main(String args[]){
> 	int result=getMax(50,7,9);
> 	Systme.out.println(result);
> }
> ```

### 4.4.3、方法的注意事项

```
1. 方法不调用不执行；
2. 方法与方法时平级关系，不能嵌套定义；
3. 方法定义的时候参数之间用逗号隔开；
4. 方法调用的时候不用再传递参数类型
5. 如果方法有明确的返回值，一定要有return带回一个值。
```

### 4.4.3、没有明确返回值的方法调用

> 其实就是void类型方法的调用
>
> ​	1.只能单独调用

### 4.4.4、返回值为void类型的方法练习

> 1. 键盘录入行数和列数，输出对应的星形
>
> ```
> public static void printXX(int x,int y){
> 	for(int i=1;i<=x;i++){
> 		for(int j=1;j<=y;j++){
> 			System.out.print("* ");
> 		}
> 		System.out.println();
> 	}
> }
> public static void main(String args[]){
> 	pringXX(4,5);
> }
> ```
>
> 



> 2. 键盘录入一个数据n(1<=n<=9)，输出对应的nn乘法表
>
> ```
> public static void printNN(int n){
> 	for(int i=1;i<=n;i++){
> 		for(int j=i;j<=i;j++){
> 			System.out.print(i+" * "+j+" = "+(i*j)+"\t");
> 		}
> 		System.out.println();
> 	}
> }
> public static void main(String args[]){
> 	printNN(9);
> }
> ```
>
> 

### 4.4.4、方法重载

#### 4.4.4.1、举例

> 需求1：求两个数的和
>
> ```
> public static int getSum(int a,int b){
> 	return a+b;
> }
> ```
>
> 需求2：求三个数的和
>
> ```
> public static int getSum1(int a,int b,int c){
> 	return a+b+c;
> }
> ```
>
> 需求3：求四个数的和
>
> ```
> public static int getSum2(int a,int b,int c,int d){
> 	return a+b+c+d;
> }
> ```



> 我们的需求不断的发生改变，就对应提供了多个求和的方法，但是他们的名字不一样，而命名规则又要求见名知意。针对这种情况，方法的功能相同，参数列表不同的情况，为了见名知意，Java允许他们起一样的名字。





> ```
> public static int getSum(int a,int b){
> 	return a+b;
> }
> ```
>
> ```
> public static int getSum(int a,int b,int c){
> 	return a+b+c;
> }
> ```
>
> ```
> public static int getSum(int a,int b,int c,int d){
> 	return a+b+c+d;
> }
> ```
>
> ```
> public static void main(String args[]){
> 	//jvm会根据不同的参数调用不同的功能
> 	System.out.println(getSum(1,2));
> 	System.out.println(getSum(1,2,5));
> 	System.out.println(getSum(1,2.5.8));
> }
> ```
>
> 

#### 4.4.4.2、方法重载的概念

> 在同一个勒种，允许存在一个以上的同名方法，只要他们的参数个数或者参数类型不同即可

#### 4.4.4.3、方法重载的特点

> 1. 与返回值类型无关，只看方法名和参数列表；
> 2. 调用时，虚拟机通过参数列表的不同来区分同名方法。

#### 4.4.4.4、方法重载的练习

> 1. 比较两个数据是否相等。参数类型分别为两个byte类型，两个short类型，两个int类型，两个long类型，并在main方法中进行测试
>
> ```
> public static boolean compare(byte a,byte b){
> 	System.out.println("byte");
> 	return a==b;
> }
> public static boolean compare(short a,short b){
> 	System.out.println("short");
> 	return a==b;
> }
> public static boolean compare(int a,int b){
> 	System.out.println("int");
> 	return a==b;
> }
> public static boolean compare(long a,long b){
> 	System.out.println("long");
> 	return a==b;
> }
> public static void main(String args[]){
> 	byte b1=3;
> 	byte b2=4;
> 	System.out.println(compare(b1,b2));
> 	
> 	
> }
> ```



## 4.5、数组

### 4.5.1、一维数组

#### 4.5.1.1、数组的概念和格式

存储多个变量（元素）的东西（容器）就较多数组，多个变量的类型要一直

> 概念：
>
> 1. 数组是存储同一种数据类型多个元素的集合，也可以看做是一个容器；
> 2. 数组既可以存储基本类型，也可以存储引用类型。

> 格式1（推荐使用）：
>
> ```
> 数据类型 [] 数组名;
> int [] a; //定义一个int类型的数组a变量
> ```
>
> 格式2：
>
> ```
> 数据类型 数组名[];
> int a [];//定义一个int类型的a数组变量
> ```
>
> 注意：这两种定义做完了，数组中是没有元素值的。如何对数组的元素进行初始化呢？

#### 4.5.1.2、数组的初始化（静态初始化）

> ```
> public static void main(String[] args){
> 	int [] a;
> 	System.out.print(a);//可能尚未初始化
> }
> ```



> 初始化的概念：为数组中的数组元素分配内存空间，并为每个数组元素赋值。

##### 4.5.1.3.1、初始化的方式

> 1、动态初始化：指定长度，有系统给出初始化值
>
> ```
> 格式：
> 数据类型[] 数组名 = new 数据类型[数组长度];
> int[] arr = new  int[3];
> 左边：
> 	int：说明数组中的元素的数据类型是int类型
> 	[]:说明这是一个数组
> 	arr：是数组的名称
> 右边：
> 	new：为数组分配内存空间
> 	int：说明数组中的元素的数据类型是int类型
> 	[]:说明这是一个数据
> 	3：数组的长度，其实就是数组中元素的个数
> 
> ```

```
public static void main(String[] args){
	int[] arr = new  int[3];
	System.out.println(arr);//[I@175078b，这是一个地址值。
}

```

我们要地址值没有意义，要的是数据值，怎么办呢？
其实数组中的每个元素都是有编号的，并且是从0开始，最大编号是数组的长度-1；
用数组名和编号的配合就可以获取数组中的指定编号的元素，这个编号的专业叫法：索引
通过数组名访问数据的格式是：数组名[索引]；

```
public static void main(String[] args){
	int[] arr = new  int[3];
	System.out.println(arr[0]);//0
	System.out.println(arr[1]);//0
	System.out.println(arr[2]);//0
}
```

#### 4.5.1.3、java中的内存分配以及栈和堆的区别

lJava 程序在运行时，需要在内存中的分配空间。为了提高运算效率，就对空间进行了不同区域的划分，因为每一片区域都有特定的处理数据方式和内存管理方式。

> 1. 栈： 存储局部变量，栈内存的数据用完就释放。
>
> ```
> 局部变量：在方法定义中或者方法声明上的变量都称为局部变量，
> 
> 	int[] arr = new  int[3];
> 	System.out.println(arr);//[I@175078b，这是一个地址值
> 	System.out.println(arr[0]);//0
> 	System.out.println(arr[1]);//0
> 	System.out.println(arr[2]);//0
> ```
>
> 
>
> 2. 堆 ：存储new出来的东西
>
> ```
> 特点：
> 1. 每个new出来的东西都有地址值
> 2. 每个变量都有默认值：
> 	byte，short,int,long---0
> 	float,double---0.0
> 	char ---'\u0000'
> 	boolean ---false
> 	引用类型----null
> 3. 使用完毕就变成了垃圾，但并没有回收；会在垃圾回收器空闲的时候回收。
> ```
>
> 
>
> 3. 方法区： (面向对象部分讲)
>
> 4. 本地方法区： (和系统相关)
>
> 5. 寄存器 ：(给CPU使用)

![38、java中的内存分配以及栈和堆的区别](F:\01、java基础\笔记的截图图片\38、java中的内存分配以及栈和堆的区别.png)



#### 4.5.1.4、一个数组内存图解

> ![39、一个数组内存图解](F:\01、java基础\笔记的截图图片\39、一个数组内存图解.png)



#### 4.5.1.5、两个数组内存图解

> ![39、两个数组内存图解](F:\01、java基础\笔记的截图图片\39、两个数组内存图解.png)



#### 4.5.1.6、三个数组内存图解

> ![39、三个数组内存图解](F:\01、java基础\笔记的截图图片\39、三个数组内存图解.png)

#### 4.5.1.7、数组的初始化（静态初始化）



> 2、静态初始化（推荐使用）:给出初始化值，有系统决定长度。
>
> ```
> 格式：
> 数据类型[] 数组名=new 数据类型[]{元素1，元素2,...};
> 
> int[] arr=new int[]{1,2,3};
> 
> 简化版格式：
> 数据类型[] 数组名={元素1，元素2,...};
> 
> int[] arr={1,2,3};
> ```
>
> ![40、数组的初始化（静态初始化）](F:\01、java基础\笔记的截图图片\40、数组的初始化（静态初始化）.png)

注意事项：

​	不要同时动态和静态进行（int [] arr=new int [3]{1，2，3}这是错误的）

#### 4.5.1.8、数组操作的两个常见小问题

##### 4.5.1.8.1、数组索引越界异常

> ![41、数组索引越界异常](F:\01、java基础\笔记的截图图片\41、数组索引越界异常.png)

##### 4.5.1.8.2、空指针异常

> ![42、空指针异常](F:\01、java基础\笔记的截图图片\42、空指针异常.png)



#### 4.5.1.9、数组练习

##### 4.5.1.9.1、数组遍历

> ```
> int[] arr={11,22,33,44,55};
> for(int i=0;i<arr.length;i++){
> 	System.out.println(arr[i]);
> }
> ```
>
> 

##### 4.5.1.9.2、数组获取最值

> 最大值：

> ```
> int[] arr={11,22,33,44,55};
> int max=arr[0];
> for(int i=1;i<arr.length;i++){
> 	if(max<arr[i]){
> 		max=arr[i];
> 	}
> }
> System.out.println(max);
> ```
>
> 最小值
>
> ```
> int[] arr={11,22,33,44,55};
> int min=arr[0];
> for(int i=1;i<arr.length;i++){
> 	if(min>arr[i]){
> 		max=arr[i];
> 	}
> }
> System.out.println(min);
> ```
>
> 

##### 4.5.1.9.3、数组逆序

方法1：

> 分析：
>
> 1. 定义个一个数组，并进行静态初始化
> 2. 思路
>    1. 把0索引和arr.length-1的数据交换
>    2. 把1索引和arr.length-2的数据交换
>    3. 。。。
>    4. 只要做到arr.length/2的时候即可

> ```
> public static void main(String[] args){
> 	int[] arr={11,22,33,44,55};
> 	printArr(arr);
> 	resevse(arr);
> 	printArr(arr);
>     
> }
> public static void resevse(int[] arr){
>   for(int i=0;i<arr.length/2;i++){
>      int temp=arr[i];
>      arr[i]=arr[arr.length-i-1];
>      arr[arr.length-i-1]=temp;
>   }
> }
> public static void printArr(int[] arr){
> 	for(int i=0;i<arr.length;i++){
>         System.out.println(arr[i]);
>     }
> }
> 
> ```
>
> 方法二：
>
> ```
> public static void main(String[] args){
> 	int[] arr={11,22,33,44,55};
> 	printArr(arr);
> 	resevse(arr);
> 	printArr(arr);
>     
> }
> public static void resevse(int[] arr){
>   for(int start =0,end=arr.length-1;start<end;start++,end--){
>      int temp=arr[start];
>      arr[start]=arr[end];
>      arr[end]=temp;
>   }
> }
> public static void printArr(int[] arr){
> 	for(int i=0;i<arr.length;i++){
>         System.out.println(arr[i]);
>     }
> }
> ```
>
> 

##### 4.5.1.9.4、数组查表法(根据索引找值)

> ```
> public static void main(String[] args){
> 	//int[] arr={11,22,33,44,55};
> 	String[] week={"星期一","星期二","星期三","星期四","星期五","星期六","星期日"}
> 	 System.out.println(getIndex(arr,9));   
> }
> public static String getIndex(String arr[],int index){
>    String value=0;
>    if(index>arr.length||index<0){
>    		return null;
>     }
>    for(int i=0;i<arr.length;i++){
>        if(arr[index]==arr[i]){
>              value= arr[i];
>         }
>     }
>    return value;
> }
> ```
>
> 

##### 4.5.1.9.5、数组基本查找法(根据值找索引)

> ```
> public static void main(String[] args){
> 	int[] arr={11,22,33,44,55};
> 	 System.out.println(getValue(arr,9));   
> }
> public static int getValue(int arr[],int value){
> 	int index=-1;
> 	for(int i =0;i<arr.length;i++){
> 		if(arr[i]==value){
> 			index=i;
> 			break;
> 		}
> 	}
> 	return index;
> }
> ```



### 4.5.2、二维数组

#### 4.5.2.1、概念

> 其实二维数组其实就是一个元素为一维数组的数组。

#### 4.5.2.2、格式1（动态-列固定）

> 格式1：
>
> ```
> 数据类型[][]变量名=new 数据类型[m][n];
> 	m:表示这个二维数组有多少个一维数组；
> 	n:表示每一个一维数组的元素个数
> 	
> int [][]arr=new int[3][2];
> 	1. 定义了一个二维数组arr；
> 	2. 这个二维数组有3个以为数组，名称是arr[0],arr[1],arr[2];
> 	3. 每个一维数组有2个元素，可以通过arrarr[m][n]来获取
> 		表示获取第m+1个一维数组的第n+1个元素
> ```
>
> 注意：
>
> 1. 以下格式也可以表示二维数组
>
>    1. ​	数据类型 数组名[] []=new 数据类型 [m] [n];
>    2. 数据类型 [] 数组名[]=new 数据类型 [m] [n];
>
> 2. 注意下面定义的区别
>
>    ```
>    int x;
>    int y;
>    int x,y;
>    
>    int []x;
>    int[]y[];//二维数组
>    int []x,y[];//一维数组x，二维数组y
>    ```
>
>    

```
int [] [] arr=new int [3][2];
System.out.println(arr);//[[I@987b124;
System.out.println(arr[0]);//[I@650a215;
System.out.println(arr[1]);//[I@651a215;
System.out.println(arr[2]);//[I@652a215;

System.out.println(arr[0][0]);//0
System.out.println(arr[0][1]);//0
System.out.println(arr[0][2]);//0
```

##### 4.5.2.2.1、二维数组格式1的内存图解

> ![43、二维数组格式1的内存图解](F:\01、java基础\笔记的截图图片\43、二维数组格式1的内存图解.png)

#### 4.5.2.3、格式2（动态-列变化）

> 格式2：
>
> ```
> 数据类型[][] 变量名 = new 数据类型[m][];
> 	m表示这个二维数组有多少个一维数组
> 	这一次没有直接给出一维数组的元素个数，可以动态的给出。
> 
> int[][] arr = new int[3][];//二维数组有3个一维数组
> arr[0] = new int[2];//二维数组的第一个数组有2个元素
> arr[1] = new int[3]；//二维数组的第二个数组有3个元素
> arr[2] = new int[1];//二维数组的第三个数组有1个元素
> 
> 
> ```
>
> 

##### 4.5.2.3.1、格式2内存图解

> ![44、格式2内存图解](F:\01、java基础\笔记的截图图片\44、格式2内存图解.png)

#### 4.5.2.4、格式3（静态）

> 格式3：
>
> ```
> 数据类型[][] 变量名 = new 数据类型[][]{{元素1…},{元素2…},{元素3…}};
> 	int[][] arr =new int[3][2]{{1,2,3},{4,6},{6}};
> 	
> 简化版格式：
> 	数据类型[][] 变量名 = {{元素…},{元素…},{元素…}};
> 
> int[][] arr =  {{1,2,3},{4,6},{6}};
> 
> ```
>
> 

##### 4.5.2.4.1、格式3的内存图解

> ![45、格式3的内存图解](F:\01、java基础\笔记的截图图片\45、格式3的内存图解.png)

#### 4.5.2.5、二维数组的练习

##### 4.5.2.5.1、二维数组遍历

> ```
> int[][] arr =  {{1,2,3},{4,6},{6}};
> for(int i=0;i<arr.length;i++){
> 	for(int j=0;j<arr[i].length;j++){
> 		System.out.print(arr[i][j]+" ");
> 	}
> 	System.out.println();
> }
> ```
>
> 

##### 4.5.2.5.2、销售额求和

> 某公司按照季度和月份统计的数据如下：单位(万元)
>
> ​	第一季度：22,66,44
>
> ​	第二季度：77,33,88
>
> ​	第三季度：25,45,65
>
> ​	第四季度：11,66,99
>
> ```
> int[][] arr =  {{22,66,44},{77,33,88},{25,45,65},{11,66,99}};
> int sum=0;
> for(int i=0;i<arr.length;i++){
> 	for(int j=0;j<arr[i].length;j++){
> 		sum+=arr[i][j];
> 	}
> }
> System.out.println(sum);
> ```
>
> 

##### 4.5.2.5.3、打印杨辉三角形（行数可键盘录入）

> 分析：
>
> ![46、杨辉三角形分析](F:\01、java基础\笔记的截图图片\46、杨辉三角形分析.png)
>
> 
>
> ```
> Scanner sc=new Scanner(System.int);
> System.out.println("请输入一个数据");
> int n=sc.nextInt();
> int [][] arr=new int[n][n];
> for(int x=0;x<arr.length;x++){
> 	arr[0][0]=1;//任何一行第一列
> 	arr[x][x]=1;//任何一行的最后一列
> }
> for(int x=2;x<arr.length;x++){
> 	//这里如果y<=x是有一个小问题的，就是最后一列已经给过值了
> 	//所以这里要-1,
> 	//并且y也应该从1开始，因为第一列也是有值了
> 	for(int y=1;y<=x-1;y++){
> 		//每一个数据是它上一行的前一列和他上一行的本列之和
> 		arr[x][y]=arr[x-1][y-1]+arr[x-1][y];
> 	}
> }
> //遍历
> for(int x=0;x<arr.length;x++){
> 	for(int y=0;y<=x;y++){
> 		System.out.print(arr[x][y]+"\t");
> 	}
> 	System.out.println();
> }
> ```
>
> 



#### 4.5.2.6、思考题

##### 4.5.2.6.1、思考题1-基本类型和引用类型参数的传递问题

> 看程序写结果，并总结基本类型和引用类型参数的传递问题
>
> ```
>     public static void main(String[] args){
>         int a = 10;
>         int b = 20;
>         System.out.println("a:"+a+",b:"+b);//a=10,b=20
>         change(a,b);//a=10,b=20--a=20,b=40
>         System.out.println("a:"+a+",b:"+b);//a=10;b=20
> 
>         int[] arr = {1,2,3,4,5};
>         change(arr);//不输出
>         System.out.println(arr[1]);//4
>     }
> 
>     public static void change(int a,int b)  {
>         System.out.println("a:"+a+",b:"+b);//a=10,b=20
>         a = b;//a=20;b=20
>         b = a + b;//b=40
>         System.out.println("a:"+a+",b:"+b);//a=20,b=40
>     }
> 
>     public static void change(int[] arr){
>         for(int x=0; x<arr.length; x++){
>             if(arr[x]%2==0){
>         		arr[x]*=2;
>         	}
> 		}
> 	}
> 
> ```
>
> ![47、基本类型和引用类型参数的传递问题图解](F:\01、java基础\笔记的截图图片\47、基本类型和引用类型参数的传递问题图解.png)
>
> 基本类型：传递的是数据值，形式参数的改变对实际参数没有影响
>
> 引用类型：传递的是地址值，形式参数的改变直接影响实际参数



##### 4.5.2.6.2、思考题2-数据加密

> 
>
> 某个公司采用公用电话传递数据信息，数据是小于8位的整数，为了确保安全，
>
> ​	 在传递过程中需要加密，加密规则如下：
>
> ​		 首先将数据倒序，然后将每位数字都加上5，再用和除以10的余数代替该数字，
>
> ​		 最后将第一位和最后一位数字交换。 请任意给定一个小于8位的整数，
>
> ​		 然后，把加密后的结果在控制台打印出来。
>
> ![48、加密问题分析](F:\01、java基础\笔记的截图图片\48、加密问题分析.png)
>
> 
>
> ```
> class JiaMiDemo {
> 	public static void main(String[] args) {
> 		//定义一个数据
> 		int number = 123456;
> 		
> 		//定义一个数组
> 		int[] arr = new int[8];
> 		
> 		//把数据中每一位上的数据获取到后存储到数组中
> 		/*
> 		int index = 0;
> 		arr[index] = number%10; //arr[0]=6;
> 		index++;
> 		arr[index] = number/10%10; //arr[1]=5;
> 		index++;
> 		arr[index] = mumber/10/10%10; //arr[2]=4;
> 		*/
> 		
> 		//通过观察这个代码，我们发现应该是可以通过循环改进的
> 		int index = 0;
> 		
> 		while(number > 0) { 				
> 			arr[index] = number%10; 
> 			index++;
> 			number/=10;			
> 		}
> 		
> 		//然后将每位数字都加上5，再用和除以10的余数代替该数字
> 		for(int x=0; x<index; x++) {
> 			arr[x] += 5;
> 			arr[x] %= 10;
> 		}
> 		
> 		//最后将第一位和最后一位数字交换
> 		int temp = arr[0];
> 		arr[0] = arr[index-1];
> 		arr[index-1] = temp;
> 		
> 		//输出数据
> 		for(int x=0; x<index; x++) {
> 			System.out.print(arr[x]);
> 		}
> 		System.out.println();
> 	}
> }
> ```
>
>  

改进版

> ```
> /*
> 	把刚才的代码改进一下：
> 		A:把数据改进为键盘录入
> 		B:把代码改进为方法实现
> 		
> 		
> 		另一个数据的测试：
> 		number:1234567
> 		第一步：7654321
> 		第二步：2109876
> 		第三步：6109872
> 		
> 	知识点：
> 		变量
> 		数据类型
> 		运算符
> 		键盘录入
> 		语句
> 		方法
> 		数组
> */
> import java.util.Scanner;
> 
> class JiaMiDemo2 {
> 	public static void main(String[] args) {
> 		//创建键盘录入对象
> 		Scanner sc = new Scanner(System.in);
> 		
> 		//请输入一个数据
> 		System.out.println("请输入一个数据(小于8位)：");
> 		int number = sc.nextInt();
> 		
> 		//写功能实现把number进行加密
> 		//调用
> 		String result = jiaMi(number);
> 		System.out.println("加密后的结果是："+result);
> 	}
> 	
> 	/*
> 		需求：写一个功能，把数据number实现加密。
> 		两个明确：
> 			返回值类型：String 做一个字符串的拼接。
> 			参数列表：int number
> 	*/
> 	public static String jiaMi(int number) {
> 		//定义数组
> 		int[] arr = new int[8];
> 		
> 		//定义索引
> 		int index = 0;
> 		
> 		//把number中的数据想办法放到数组中
> 		while(number > 0) {
> 			arr[index] = number%10;
> 			index++;
> 			number /= 10;
> 		}
> 		
> 		//把每个数据加5，然后对10取得余数
> 		for(int x=0; x<index; x++) {
> 			arr[x] += 5;
> 			arr[x] %= 10;
> 		}
> 		
> 		//把第一位和最后一位交换
> 		int temp = arr[0];
> 		arr[0] = arr[index-1];
> 		arr[index-1] = temp;
> 		
> 		//把数组的元素拼接成一个字符串返回
> 		//定义一个空内容字符串
> 		String s = "";
> 		
> 		for(int x=0; x<index; x++) {
> 			s += arr[x];
> 		}
> 		
> 		return s;
> 	}
> }
> ```
>
> 



# 二、面向对象

## 2.1、面向对象思想

### 2.1.1、概述

> 面向对象是基于面向过程的编程思想
>
> 面向过程：强调的是每一个功能的步骤
>
> 面向对象：香调的是对象；然后由对象去调用功能



### 2.1.2、特点

> 1. 是一种更符合我们思想习惯的思想；
> 2. 可以将复杂的事情简单化；
> 3. 将我们从执行者变成指挥者。
>
> 

### 2.1.3、面向对象开发，设计，特征

#### 2.1.3.1、开发

> 不断的创建对象，使用对象，指挥对象做事情

#### 2.1.3.2、设计

> 其实就是在管理和维护对象之间的关系

#### 2.1.3.3、特征

> 1. 封装(encapsulation)
> 2. 继承(inheritance)
> 3. 多态(polymorphism)



## 2.2、类与对象及其作用

### 2.2.1、类与对象的关系

> 类：是一组相关的属性和行为的集合；是一个抽象的概念
>
> 对象：是该类事物的具体体现；是具体存在的个体
>
> ```
> 类：学生类
> 对象：班长就是一个对象
> ```
>
> ```
> 事物：					类：					
> 	属性(身高，体重)		成员变量：和变量的定义一样的格式，但是位置不同，在类中方法外
> 	行为(吃饭，睡觉)		成员方法：和的方法定义一样的格式，但是今天把static先去掉
> ```
>
> ```
> 
> ```

#### 2.2.1.1、学生类的定义

```
class Student {
	//定义变量
	//姓名
	String name;
	//年龄
	int age;
	//地址
	String address;
	
	//定义方法
	//学习的方法
	public void study() {
		System.out.println("学生爱学习");
	}
	
	//吃饭的方法
	public void eat() {
		System.out.println("学习饿了,要吃饭");
	}
	
	//睡觉的方法
	public void sleep() {
		System.out.println("学习累了,要睡觉");
	}
}
```

#### 2.2.1.2、学生类的使用

```
class StudentDemo {
	public static void main(String[] args) {
		//类名 对象名 = new 类名();
		Student s = new Student();
		
		//输出成员变量值
		//System.out.println(s.name);
		//System.out.println(s.age);
		//System.out.println(s.address);
		//改进写法
		System.out.println(s.name+"---"+s.age+"---"+s.address);
		
		
		//给成员变量赋值
		s.name = "林青霞";
		s.age = 27;
		s.address = "北京";
		//赋值后的输出
		System.out.println(s.name+"---"+s.age+"---"+s.address);
		
		//调用方法
		s.study();
		s.eat();
		s.sleep();
	}
}
```



#### 2.2.1.3、手机类的定义的练习

```
/*
	手机事物：
		属性：品牌，价格，颜色...
		行为：打电话，发短信，玩游戏...
		
	手机类：
		成员变量：品牌，价格，颜色
		成员方法：打电话，发短信，玩游戏
*/
class Phone {
	//品牌
	String brand;
	//价格
	int price;
	//颜色
	String color;
	
	//打电话的方法
	public void call(String name) {
		System.out.println("给"+name+"打电话");
	}
	
	//发短信的方法
	public void sendMessage() {
		System.out.println("群发短信");
	}
	
	//玩游戏的方法
	public void playGame() {
		System.out.println("玩游戏");
	}
}
```

#### 2.2.1.4、手机类的使用

```
class PhoneDemo {
	public static void main(String[] args) {
		//创建手机对象
		//类名 对象名 = new 类名();
		Phone p = new Phone();
		
		//直接输出成员变量值
		System.out.println(p.brand+"---"+p.price+"---"+p.color);
		
		//给成员变量赋值
		p.brand = "诺基亚";
		p.price = 100;
		p.color = "灰色";
		//再次输出
		System.out.println(p.brand+"---"+p.price+"---"+p.color);
		
		//调用方法
		p.call("林青霞");
		p.sendMessage();
		p.playGame();
	}
}
```



## 2.3、对象的内存图



### 2.3.1、一个对象的内存图---一个对象的基本初始化过程

> ![49、一个对象的内存图](F:\01、java基础\笔记的截图图片\49、一个对象的内存图.bmp)



### 2.3.2、两个对象的内存图--•方法的共用

> ![50、二个对象的内存图](F:\01、java基础\笔记的截图图片\50、二个对象的内存图.bmp)



### 2.3.2、三个对象的内存图--其中有两个引用指向同一个对象

> ![51、三个对象的内存图](F:\01、java基础\笔记的截图图片\51、三个对象的内存图.bmp)

## 2.4、成员变量和局部变量的区别

> 1. 在类中的位置不同
>
> ​	•成员变量 类中方法外
>
> ​	•局部变量 方法内或者方法声明上
>
> ![49、在类中的位置不同](F:\01、java基础\笔记的截图图片\49、在类中的位置不同.png)
>
> 2. 在内存中的位置不同
>
>    ​	•成员变量 堆内存
>
>    ​	•局部变量 栈内存
>
> 3. 生命周期不同
>
>    ​	•成员变量 随着对象的存在而存在，随着对象的消失而消失
>
>    ​	•局部变量 随着方法的调用而存在，随着方法的调用完毕而消失
>
> 
>
> 4. 初始化值不同
>
>    ​	•成员变量 有默认的初始化值
>
>    ​	•局部变量 没有默认的初始化值，必须先定义，赋值，才能使用
>
> ![52、初始化值不同](F:\01、java基础\笔记的截图图片\52、初始化值不同.png)

注意事项：局部变量名称可以和成员变量的名称一样，在方法中是用的时候，采取就近原则

### 2.4.2、形式参数问题

#### 2.4.2.1、以前讲过的

> 基本类型：形式参数的改变不影响实际参数
>
> 引用类型：形式参数的改变会影响实际参数

#### 2.4.2.2、现在要讲的

##### 2.4.2.2.1、形式参数是基本类型

> ![53、形式参数是基本类型](F:\01、java基础\笔记的截图图片\53、形式参数是基本类型.png)

##### 2.4.2.2.2、形式参数是引用类型

> ![54、形式参数是引用类型](F:\01、java基础\笔记的截图图片\54、形式参数是引用类型.png)

## 2.5、匿名对象

> 就是没有名字的对象。
>
> ​	•是对象的一种简化表示形式

### 2.5.1、匿名对象应用场景

#### 2.5.1.1、对象调用方法----仅仅一次的时候

> ![55、匿名对象应用场景1](F:\01、java基础\笔记的截图图片\55、匿名对象应用场景1.png)
>
> 好处：匿名对象调用完毕就是垃圾，可以被垃圾回收器回收

#### 2.5.1.2、作为实际参数传递

> ![55、匿名对象应用场景2](F:\01、java基础\笔记的截图图片\55、匿名对象应用场景2.png)
>
> 
>
> 第二种方式：
>
> ![55、匿名对象应用场景2-2](F:\01、java基础\笔记的截图图片\55、匿名对象应用场景2-2.png)

## 2.6、封装

### 2.6.1、概述

> 是指隐藏对象的属性和实现细节，仅对外提供公共访问方式。

#### 2.6.1.2、代码说明

![56、封装的概述1](F:\01、java基础\笔记的截图图片\56、封装的概述1.png)

#### 2.6.1.2、代码改进版

![56、封装的概述2](F:\01、java基础\笔记的截图图片\56、封装的概述2.png)



#### 2.6.1.3、再次改进

![56、封装的概述3](F:\01、java基础\笔记的截图图片\56、封装的概述3.png)



### 2.6.2、封装的好处

> 1. 隐藏实现细节，提供公共的访问方式
>
> 2. 提高了代码的复用性
>
> 3. 提高安全性。
> 4. d

### 2.6.3、封装的原则

> 1. 将不需要对外提供的内容都隐藏起来。
>
> 2. 把属性隐藏，提供公共方法对其访问。

## 2.7、this关键字

### 2.7.1、this关键字的概述

> 1. 是一个权限修饰符
> 2. 可以修饰成员（成员变量和成员方法）
> 3. 被private修饰的成员只有在本类中才能访问
>
> 

![57、this关键字的概述](F:\01、java基础\笔记的截图图片\57、this关键字的概述.png)

### 2.7.2、this关键字的应用场景

> 1. 把成员变量用private修饰
>
> 2. 提高对应的getXXX()和setXXX()方法
>
>    ![58、this的应用场景](F:\01、java基础\笔记的截图图片\58、this的应用场景.png)



**this：是代表所在类的对象引用，方法被哪个对象调用，this就代表那个对象**

**this：的场景：解决局部变量隐藏成员变量**



### 2.7.3、this关键字的内存图解

![59、this内存图](F:\01、java基础\笔记的截图图片\59、this内存图.png)



## 2.8、构造方法

### 2.8.1、构造方法的概述

> 给对象的数据进行初始化

### 2.8.2、构造方法的格式

> 1. 方法名与类名相同
>
> 2. 没有返回值类型，连void都没有
>
> 3. 没有具体的返回值
>
> 

![60、构造方法的概述和格式](F:\01、java基础\笔记的截图图片\60、构造方法的概述和格式.png)

### 2.8.3、构造方法的重载和注意事项

> 1. 如果你不提供构造方法，系统会给出默认构造方法
>
> 2. 如果你提供了构造方法，系统将不再提供
>
> 3. 构造方法也是可以重载的
>
> 

给成员变量赋值有两种方法：

1. setXXX
2. 构造方法

### 2.8.4、成员方法

> 类的组成
>
> 	1. 成员方法
>  	2. 局部变量
>  	3. 构造方法

#### 2.8.4.1、分类和使用

> •根据返回值
>
> ​		•有明确返回值方法：`public String getString(){return "name";}`
>
> ​		•返回void类型的方法：`public void show(){System.out.println("aaa");}`
>
> •根据形式参数
>
> ​		•无参方法 ：`public void method(int age){System.out.println(age)}`
>
> ​		•带参方法：`public void show(){System.out.println("aaa");}`
>
> 

#### 2.8.4.2、一个基本类的标准代码写法

> 类
>
> ​	成员变量
>
> ​	构造方法
>
> ​	无参构造方法
>
> ​	带参构造方法
>
> ​	成员方法
>
> ​	getXxx()
>
> ​	setXxx()
>
> 给成员变量赋值的方式
>
> ​	无参构造方法+setXxx()
>
> ​	带参构造方法



#### 2.8.4.3、什么时候定义成员变量

> 如果这个变量是用来描述这个类的信息的，那么改变来那个就应该定义为成员变量
>
> 变量到底定义在哪里好呢？
>
> 变量的范围是越小越好，因为能及时的被回收

### 2.8.6、创建对象做了哪些事情

> `Student s=new Student();//在内存中做了哪些事情?`
>
> ​	1. 加载Student.class文件进内存
>
>  	2. 在栈内存为s开辟空间
>
> ​	3. 在堆内存为学生对象开辟空间`new Student`
>
> ​	4. 对学生对象的成员变量进行默认初始化
>
> ​	5. 对学生对象的成员变量进行显示初始化
>
> ​	6. 通过构造方法对学生对象的成员变量赋值
>
> ​	7. 学生对象初始化完毕，把对象地址赋值给s变量

#### 2.8.6.1、内存图

![61、创建对象做了哪些事情](F:\01、java基础\笔记的截图图片\61、创建对象做了哪些事情.png)

#### 2.8.6.2、加减乘除的练习

> ![62、加减乘除练习_功能类](F:\01、java基础\笔记的截图图片\62、加减乘除练习_功能类.png)



> ![62、加减乘除练习_测试类](F:\01、java基础\笔记的截图图片\62、加减乘除练习_测试类.png)

## 2.9、static关键字

> 可以修饰成员变量和成员方法

### 2.9.1、static的引入

> 1、
>
> ![63、static的引入](F:\01、java基础\笔记的截图图片\63、static的引入.png)
>
> 2、
>
> ![63、static的引入2](F:\01、java基础\笔记的截图图片\63、static的引入2.png)

### 2.9.2、static关键字的特点

> 1. 可以随着类的加载而加载（`回想main方法`）
>
> 2. 优先于对象存在
>
> 3. 被类的所有对象共享（`学生可以共用一个班级编号`）
>
>    ```
>    这也是我们判断是否使用静态关键字的条件：如果某个成员变量是被所有对象共享的那么它就应该被定义为静态
>    ```
>
> 4. 可以通过类名调用
>
>    ​	其实他本身也可以通过对象名调用
>
>    ​	`推荐使用类名调用，静态修饰的内容一般我们称其为：与类相关的，类成员`
>
>    

### 2.9.3、static关键字的内存图解

> ![64、static内存图](F:\01、java基础\笔记的截图图片\64、static内存图.png)

### 2.9.4、static的注意事项

> static关键字注意事项
>
>  1. 在静态方法中是没有this关键字的:
>
>     `静态是随着类的加载而加载，this是随着`对象的创建二存在，静态比对象先存在
>
> ![65、static注意事项1](F:\01、java基础\笔记的截图图片\65、static注意事项1.png)
>
> ​	
>
> 2. 静态方法只能访问静态的成员变量和静态的成员方法
>
>    ```
>    静态方法：
>    	成员变量：只能访问静态变量
>    	成员方法：只能访问静态成员方法
>    非静态方法：
>    	成员变量：可以是静态的， 也可以是费静态的。
>    	成员方法：可以是静态的成员方法，也可以是费静态的成员方法
>    
>    简单记：静态只能访问静态的。
>    ```
>
>    
>
> ![65、static注意事项2](F:\01、java基础\笔记的截图图片\65、static注意事项2.png)
>
> 

### 2.9.5、静态变量和成员变量的区别

> 1. 所属不同
>
>    ```
>    •静态变量属于类，所以也称为为类变量
>    
>    •成员变量属于对象，所以也称为实例变量(对象变量)
>    ```
>
> 2. 内存中位置不同
>
>    ```
>    •静态变量存储于方法区的静态区
>    
>    •成员变量存储于堆内存
>    ```
>
> 3. 内存出现时间不同
>
>    ```
>    •静态变量随着类的加载而加载，随着类的消失而消失
>    
>    •成员变量随着对象的创建而存在，随着对象的消失而消失
>    ```
>
>    
>
> 4. 调用不同
>
>    ```
>    •静态变量可以通过类名调用，也可以通过对象调用
>    
>    •成员变量只能通过对象名调用
>    ```
>
>    

### 2.9.6、main方法的格式详解

> ```
> public static void main(String[] args) {}
> 	public 公共的，访问权限是最大的。由于main方法是被jvm调用，所以权限要大
> 	static 静态的，需要创建对象，不用创建对象，通过类名就可以被调用直接类名访问，方便jvm的调用
> 	void：方法的返回值是返回给调用者，而main被jvm调用，返回内容给jvm没有意义
> 	main ：是一个常见的方法入口，大部分语言都是以main作为入口一个通用的名称，虽然不是关键字，但是被jvm			  识别
> 	String[] args ：这是一个字符串数组，值去哪里了？
> 			这个东西到底有什么用，怎么给值，以前用于接收键盘录入的数据的(JDK1.5以后被Scanner替代了)
> 			格式是：
> 				java MainDemo hello world java
> 				
> ```
>
> ![66、main方法的格式详解](F:\01、java基础\笔记的截图图片\66、main方法的格式详解.png)

## 2.10、代码块

> 在Java中，使用｛｝括起来的代码被称为代码块
>
> 

### 2.10.1、代码块的分类

> 1. 局部代码块：局部位置
>
>     `用于限定变量的生命周期`
>
> ![67、局部代码块](F:\01、java基础\笔记的截图图片\67、局部代码块.png)
>
> 2. 构造代码块：在构造方法中（类中的成员位置），用{}括起来的代码，每次调用构造方法前，都会先执行构造代码块。
>
> `作用：可以把多个构造方法中的共同代码放在一起，对对象进行初始化`
>
> ![67、构造代码块](F:\01、java基础\笔记的截图图片\67、构造代码块.png)
>
> 3. 静态代码块：构造代码块：在构造方法中（类中的成员位置），用{}括起来的代码，只不过它用static修饰
>
> `作用：一般是对类进行初始化`
>
> ![67、静态代码块](F:\01、java基础\笔记的截图图片\67、静态代码块.png)

### 2.10.2、面试题

> 静态代码块，构造代码块，构造方法的执行顺序
>
> ```
> 静态代码块---构造代码块---构造方法
> 静态代码块：只执行一次，对类进行初始化
> 构造代码块：每次调用构造方法都执行，对对象进行初始化
> ```

2.10.3、看程序写结果

> ```
> class Student{
> 	static{
> 		System.out.println("Student 静态代码块");
> 	}
> 	{
> 		System.out.println("Student 构造代码块");
> 	}
> 	public Student(){
> 		System.out.println("Student 构造方法");
> 	}
> }
> 
> class StudentDemo{
> 	static{
> 		System.out.println("林青霞");
> 	}
> 	public static void main(){
> 		System.out.println("main");
> 		Student s1=new Student();
> 		Student s2=new Student();
> 	}
> 	
> }
> 
> ```
>
> `执行结果：`
>
> `1.林青霞，main,Student 静态代码块，Student 构造代码块，Student 构造方法`
>
> `2.Student 构造代码块，Student 构造方法`
>
> 

## 2.11、继承

### 2.11.1、继承的概述

> 概述：多个类中存在相同的属性和行为，将这些内容抽取到一个单独的类中，那么多个类无需在定义这些属性和行为，只要继承那个类即可。
>
> ```
> 格式：class 子类名 extends 父类名{}
> 
> class Fu{}
> class Zi extends Fu{}
> ```
>
> 

### 2.11.2、继承的好处

> 1. 提高代码的复用性。
>
> 2. 提高了代码的维护性
>
> 3. 让类与类之间产生了关系，是多态的前提
>
>    ​	`这里其实也是继承的一个弊端：类的耦合性增强了`
>
> 4. 7
>
> 开发的原则：低耦合，高内聚
>
> 耦合：类与类的关系
>
> 内聚：就是自己完成某件事情的能力

### 2.11.3、继承的弊端

> ​	`这里其实也是继承的一个弊端：类的耦合性增强了`

### 2.11.4、Java继承的特点

> 1. Java中只支持单继承，不支持多继承
>
> 2. Java支持多层继承（继承体系）
>
> ![68、java中继承的特点](F:\01、java基础\笔记的截图图片\68、java中继承的特点.png)



### 2.11.5、Java继承的注意事项

> 1. 子类只能继承父类所有非私有的成员（成员方法和成员变量）
>
>    ![69、继承的注意事项1](F:\01、java基础\笔记的截图图片\69、继承的注意事项1.png)
>
>    
>
>    ![69、继承的注意事项2-子类不能访问父类的私有成员变量](F:\01、java基础\笔记的截图图片\69、继承的注意事项2-子类不能访问父类的私有成员变量.png)
>
>    2. 子类不能继承父类的构造方法，但是可以通过supper关键字去访问父类构造方法
>    3. 不要为了部分功能而去继承
>       1. 继承其实体现的是一种关系：`is a`

### 2.11.6、继承中成员变量的关系

> 类的组成：	
>
> ```
> 
> 构造方法
> 成员方法：
> ```

> 继承中成员变量的关系
>
> 成员变量：
>
> ```
> 子类中的成员变量和父类中的成员变量名称不一样。
> ```
>
> ![70继承中成员变量的关系1](F:\01、java基础\笔记的截图图片\70继承中成员变量的关系1.png)
>
> 
>
> ​	
>
> ```
> 子类中的成员变量和父类中的成员变量名称一样。
> 	在子类方法中访问一个变量的查找顺序
> 		1.在子类方法的局部范围找，有就使用
> 		2. 在子类的成员范围找，有就使用
> 		3. 在父类的成员范围中，有就使用
> 		4. 如果还找不到，就报错
> ```
>
> ![70继承中成员变量的关系2](F:\01、java基础\笔记的截图图片\70继承中成员变量的关系2.png)

### 2.11.7、this和super的区别和应用

> 1. this和super分别是什么
>
>    ```
>    this：代表本类对应的引用
>    
>    super：代表父类存储空间的标识（可以理解为父类引用，可以操作父类的成员）
>    ```
>
>    
>
>    this和super怎么用?
>
>     1. 调用成员变量
>
>        this.成员变量：调用本类的成员变量
>
>        super.成员变量：调用父类的成员变量
>
>     2. 调用构造方法
>
>        this(...)：调用本类的构造方法
>
>        super(...)：调用f父类的构造方法
>
>     3. 调用成员方法
>
>        this.成员方法：调用本类的成员方法
>
>        super.成员方法：调用父类的成员方法
>
>    ![71、this和super](F:\01、java基础\笔记的截图图片\71、this和super.png)

### 2.11.8、继承中构造方法的关系

> 1.子类中所有的构造方法默认都会访问父类的无参的构造方法
>
> ![72、继承中构造方法的关系](F:\01、java基础\笔记的截图图片\72、继承中构造方法的关系.png)
>
> ![72、继承中构造方法的关系2](F:\01、java基础\笔记的截图图片\72、继承中构造方法的关系2.png)
>
> 

#### 2.11.8.1、为什么子类所有的构造方法默认都会访问父类的无参构造

​		**因为子类会继承父类中的数据，可能会使用父类的数据，所以子类初始化之前，一定要先完成父类数据的初始化**

​		**注意：子类每个构造方法的第一条语句默认是：super();**

### 2.11.9、继承中构造方法的注意事项

如果父类没有无参构造方法，那么子类的构造方法会出现什么现象呢

![73、继承的注意事项](F:\01、java基础\笔记的截图图片\73、继承的注意事项.png)

那么如何解决呢如何解决？

​	1.在父类中加一个无参构造方法

![73、继承的注意事项](F:\01、java基础\笔记的截图图片\73、继承的注意事项.png)

​	2.通过使用super关键字去显式的调用带参构造方法

![73、继承的注意事项-显式](F:\01、java基础\笔记的截图图片\73、继承的注意事项-显式.png)

​	3.子类通过this去调用本类的其他构造方法

![73、继承的注意事项-this](F:\01、java基础\笔记的截图图片\73、继承的注意事项-this.png)

> 注意事项：this(...)和super(...)一定要出现在第一条语句上
>
> 如果不是放在第一条语句上，就可能对父类的数据进行了多次初始化

### 2.11.10、面试题

#### 2.11.10.1、看程序写结果

> 1.成员变量：就近原则
>
> 2. this访问本类成员
>
> 3.super访问父类成员
>
> 4.子类构造方法执行前默认先执行父类的无参构造方法
>
> 5.一个类的初始化过程
>
> ​		成员变量进行初始化
>
> ​			默认初始化-
>
> ​			显示初始化--
>
> ​			构造方法初始化
>
> ​			
>
> ​	

![74、看程序写结果1](F:\01、java基础\笔记的截图图片\74、看程序写结果1.png)

```

```

#### 2.11.10.2、看程序写结果2

> ![75、继承面试2](F:\01、java基础\笔记的截图图片\75、继承面试2.png)



面试题目

![75、继承面试2-题目](F:\01、java基础\笔记的截图图片\75、继承面试2-题目.png)

#### 2.11.10.3、看程序写结果3

> ![75、继承面试3](F:\01、java基础\笔记的截图图片\75、继承面试3.png)



面试题目

![75、继承面试3-题目](F:\01、java基础\笔记的截图图片\75、继承面试3-题目.png)

### 2.11.11、继承中成员方法的关系

![76、继承中成员方法的关系](F:\01、java基础\笔记的截图图片\76、继承中成员方法的关系.png)



## 2.12、方法重写

> ![78、方法重写的概念](F:\01、java基础\笔记的截图图片\78、方法重写的概念.png)

方法重载

> ![78、方法重载](F:\01、java基础\笔记的截图图片\78、方法重载.png)





### 2.12.1、方法重写的注意事项

1.

> ![79、方法重写注意事项1](F:\01、java基础\笔记的截图图片\79、方法重写注意事项1.png)

2.

> ![79、方法重写注意事项2](F:\01、java基础\笔记的截图图片\79、方法重写注意事项2.png)

3.

> 总结：
>
> ![79、方法重写注意事项3](F:\01、java基础\笔记的截图图片\79、方法重写注意事项3.png)

### 2.12.2、面试题

#### 2.12.2.1、面试题1

> ![80、方法重载面试题1](F:\01、java基础\笔记的截图图片\80、方法重载面试题1.png)

答案1

![80、方法重载面试题1-答案](F:\01、java基础\笔记的截图图片\80、方法重载面试题1-答案.png)

#### 2.12.2.2、面试题2

> ![80、方法重载面试题2](F:\01、java基础\笔记的截图图片\80、方法重载面试题2.png)

答案

![80、方法重载面试题2-答案](F:\01、java基础\笔记的截图图片\80、方法重载面试题2-答案.png)

## 2.13、final关键字

### 2.13.1、引入

![81、final关键字的引入](F:\01、java基础\笔记的截图图片\81、final关键字的引入.png)

final：最终的意思。最常见的是它可以修饰类，方法，变量。

![81、final关键字的引入2](F:\01、java基础\笔记的截图图片\81、final关键字的引入2.png)

### 2.13.2、final关键字的特点

> final关键字修饰：
>
> ​	类，被final修饰的类，该类不能被继承
>
> ![82、final修饰类](F:\01、java基础\笔记的截图图片\82、final修饰类.png)
>
> ​	方法：被final修饰的方法，该方法不能被重写
>
> ![82、final修饰方法](F:\01、java基础\笔记的截图图片\82、final修饰方法.png)
>
> ​	变量：被final修饰的变量，该变量不能被重新赋值。因为这个变量其实是常量
>
> ![82、final修饰变量](F:\01、java基础\笔记的截图图片\82、final修饰变量.png)
>
> 去

### 2.13.3、final面试题

#### 2.13.3.1、final修饰局部变量

> 局部变量是基本数据类型：基本类型的值不能变
>
> ![83、final面试题1](F:\01、java基础\笔记的截图图片\83、final面试题1.png)

> 局部变量是引用数据类型：引用类型的地址值不能发生改变，但是该对象堆内存的值是可以改变的
>
> ![83、final面试题1-2](F:\01、java基础\笔记的截图图片\83、final面试题1-2.png)
>
> ![83、final面试题1-3](F:\01、java基础\笔记的截图图片\83、final面试题1-3.png)
>
> ss=new Student();才会报错，ss.age=100是不会报错的
>
> 



#### 2.13.3.2、final修饰变量的初始化时机

![83、final面试题2](F:\01、java基础\笔记的截图图片\83、final面试题2.png)

![83、final面试题2-1](F:\01、java基础\笔记的截图图片\83、final面试题2-1.png)

#### 

## 2.14、多态

### 1、概念

> 某一个对象(事物)，在不同时刻表现出来的不同状态
>
> ` 猫是猫，猫是动物`
>
> 

### 2、多态的前提和体现

> 1. 有继承关系
>
> 
>
> 2. 有方法重写：其实没有也可以，但是如果没有这个就没有意义
>
> 
>
> ```
> 动物 d=new 猫();
> d.show();
> 动物 d=new 狗();
> d.show();
> ```
>
> 
>
> 
>
> 3. 有父类引用指向子类对象：`fu f=new zi()`
>
> ![84、多态的前提](F:\01、java基础\笔记的截图图片\84、多态的前提.png)

### 3、多态中的成员访问特点

> 1. 成员变量：编译看左边，运行看左边
>
>    ![84、多态的特点1](F:\01、java基础\笔记的截图图片\84、多态的特点1.png)
>
> 2. 构造方法：
>
> ```
> 创建子类对象的时候，访问父类的构造方法，对父类的数据进行初始化
> ```
>
> ![84、多态的前提](F:\01、java基础\笔记的截图图片\84、多态的前提.png)
>
> 3. 成员方法：编译看左边，运行看右边
>
>    ![84、多态的特点2](F:\01、java基础\笔记的截图图片\84、多态的特点2.png)
>
>    4. 静态方法：编译看左边，运行看左边（静态和类相关，算不上重写，所以访问还是左边的）
>
>       ![84、多态的特点3](F:\01、java基础\笔记的截图图片\84、多态的特点3.png)
>
> **结论：由于成员方法存在放法重写，所以他运行看右边**

### 4、多态的好处

> 1. 提高了代码的维护性（由继承保证）
> 2. 提高了代码的扩展性(由多态保证)

### 5、多态的弊端

> 1、不能使用子类的功能(多态中向上转型)
>
> ![85、多态的弊端1](F:\01、java基础\笔记的截图图片\85、多态的弊端1.png)
>
> 
>
> 3、多态中向下转型
>
> ![85、多态中向下转型](F:\01、java基础\笔记的截图图片\85、多态中向下转型.png)
>
> 对象间的转型问题：
>
> ​	向上转型：从子到父，父类引用指向子类对象
>
> ```
> Fu f=new Zi();
> ```
>
> ​	向下转型：从父到子，弗雷引用转为子类对象
>
> ```
> Zi z=(Xi)f;//要求该f必须是能够转换为zi的
> ```
>
> 

### 6、多态继承中的内存图解

![85、多态继承中的内存图解](F:\01、java基础\笔记的截图图片\85、多态继承中的内存图解.png)

### 7、多态中的对象变化内存图解

> ClassCastException：类型转换异常（多出现在向下转型中出现）

![86、多态中的对象变化内存图解](F:\01、java基础\笔记的截图图片\86、多态中的对象变化内存图解.png)

### 8、多态练习-看程序写结果

#### A、第一题

> 多态中的成员访问特点

![87、多态的练习题-看程序写结果](F:\01、java基础\笔记的截图图片\87、多态的练习题-看程序写结果.png)

#### B、第二题

![87、多态的练习题-看程序写结果2](F:\01、java基础\笔记的截图图片\87、多态的练习题-看程序写结果2.png)



## 2.15、抽象类

> 在java中，一个没有方法体的方法应该定义为抽象类，而类中如果有抽象发那个发，该类必须定义为抽象类

### 1、抽象类的特点

> 1、抽象类和抽象方法必须用abstract关键字修饰
>
> ![88、抽象类的格式](F:\01、java基础\笔记的截图图片\88、抽象类的格式.png)
>
> 2、抽象类中不一定有抽象方法，但是有抽象方法的类必须定义为抽象类
>
> 3、抽象类不能实例化：因为它不是具体的类
>
> ```
> 抽象类有构造方法，但是不能实例化，构造方法的作用是什么？
> 	用于子类访问父类数据的初始化
> ```
>
> ![88、抽象类的不能实例化](F:\01、java基础\笔记的截图图片\88、抽象类的不能实例化.png)
>
> 4、抽象类的子类
>
> ```
> 1、如果不想重写抽象方法，抽象类的子类是一个抽象类
> 2、抽象所有的抽象方法，这个时候子类是一个具体的类
> ```
>
> 抽象类的实例化是靠具体的子类实现的，是多态的方式
>
> ```
> Animal a=new Cat();
> ```
>
> 

### 2、抽象类的成员特点

> 1、成员变量：既可以是变量，也可以是常量
>
> 2、构造方法：有，用于自子类访问父类数据的初始化
>
> 3、成员方法：既可以是抽象，也可以非抽象的
>
> ![89、抽象类的成员特点](F:\01、java基础\笔记的截图图片\89、抽象类的成员特点.png)
>
> ```
> 抽象类的成员方法个性：
> 	1、抽象方法	强制要求子类做的事情
> 	2、非抽象方法	子类继承的事情，提高代码复用性
> ```
>
> 

### 3、抽象类中的小问题

> 1、一个类如果没有抽象方法，可不可以定义为抽象类，如果可以，有什么意义
>
> ```
> 可以，不让创建对象
> ```
>
> 

> 2、抽象类不能喝那些关键字共存
>
> ```
> private 	冲突
> ```
>
> ![90、abstract——private](F:\01、java基础\笔记的截图图片\90、abstract——private.png)
>
> ```
> final 		冲突
> ```
>
> ![90、abstract——final](F:\01、java基础\笔记的截图图片\90、abstract——final.png)
>
> ```
> static		无意义（抽象类没有方法体，调他没有意义）
> ```
>
> ![90、abstract——static](F:\01、java基础\笔记的截图图片\90、abstract——static.png)

## 2.16、接口

### 1、概述

> 为了体现事物功能的扩展性，Java中就提供了接口来定义这些额外的功能，并不给出具体实现
>
> ![91、接口的概述](F:\01、java基础\笔记的截图图片\91、接口的概述.png)

### 2、接口的特点

> 1、接口用关键字interface表示：
>
> ```
> 格式： inteface接口名
> ```
>
> 2、类实现接口用implements表示
>
> ```
> class 类名 implements 接口名{}
> ```
>
> 3、接口不能实例化
>
> ```
> 那么接口如何实例化呢？
> 	按照多态的方式来实例化
> ```
>
> 4、接口的子类
>
> ```
> 1、可以是抽象类，但是意义不大
> 2、可以是具体类，要重写接口中的所有抽象方法（推荐方案）
> ```
>
> 
>
> 由此可见，多态有下列几种方式
>
> ```
> 1、具体类多态（几乎没有）
> 2、抽象类多态（常用）
> 3、接口多态（最常用）
> ```
>
> 

### 3、接口的成员特点

> 1、成员变量：
>
> ```
> 在接口中，只能是常量，并且是静态的：
> 	默认修饰符：public static final
> 	建议自己手动给出
> ```
>
> ![91、接口的成员特点1](F:\01、java基础\笔记的截图图片\91、接口的成员特点1.png)
>
> 
>
> ![91、接口的成员特点2](F:\01、java基础\笔记的截图图片\91、接口的成员特点2.png)
>
> 2、构造方法：
>
> ```
> 接口没有构造方法
> ```
>
> ![91、接口的成员特点3](F:\01、java基础\笔记的截图图片\91、接口的成员特点3.png)
>
> 3、成员方法：
>
> ```
> 接口中的方法只能是抽象方法
> 	默认修饰福：public abstract
> 	建议：自己手动给出。
> ```
>
> **所有的类都继承Object类，Object是类层次结构的根类。每一个类都使用Object作为超类**

### 4、类与类，雷雨接口，接口与接口的关系

> 1、类与类：
>
> ```
> 继承关系，只能单继承，但是可以多层继承
> ```
>
> 2、类与接口
>
> ```
> 实现关系，可以单实现，也可以多实现，还可以继承一个类的同时实现多个接口
> ```
>
> 3、接口与接口
>
> ```
> 继承关系，可以单继承也可以多继承
> ```
>
> 

### 5、抽象类与接口的区别

> 1、成员区别
>
> ```
> A、抽象类：
> 	成员变量：可以变量，可以常量
> 	构造方法：有
> 	成员方法：可以抽象方法，也可以非抽象放大
> B、接口：
> 	成员变量：只可以是常量；
> 	成员方法：只可以是抽象方法
> ```
>
> 2、关系区别
>
> ```
> A、类与类：继承，单继承
> B、类与接口：实现，单实现，多实现
> C、接口与接口：继承，单继承，多继承
> ```
>
> 3、设计理念区别
>
> ```
> 	a、抽象类：被继承体现是：“is a”的关系，抽象类中定义的是该继承体系的共性功能（是什么）
> 	b、接口：被实现体现的是：“like a”的关系，接口中定义的是该继承体系的扩展功能（像什么）
> ```
>
> 

## 2.17、返回值

### 1、形式参数



> ​		A 、基本类型：（太简单，不是我们今天要讲解的）
> ​		B、引用类型：
> ​				a 、类（匿名对象的时候我们就讲过了），需要的是该类的对象
>
> ![92、返回值_类名作为形式参数](F:\01、java基础\笔记的截图图片\92、返回值_类名作为形式参数.png)
>
> ​				b、抽象类：需要的是该抽象的子类对象
>
> ![92、返回值_抽象类作为形式参数](F:\01、java基础\笔记的截图图片\92、返回值_抽象类作为形式参数.png)
>
> 
>
> ​				c、接口：需要的是该接口的子类对象
>
> ![92、返回值_接口作为形式参数](F:\01、java基础\笔记的截图图片\92、返回值_接口作为形式参数.png)
>
> 

### 2、返回值类型



> ​		A、基本类型：（太简单，不是我们今天要讲解的）
> ​		B、引用类型				
>
> ```
> 		a、类名：返回的是该类的对象
> ```
>
> ![93、类名作为返回值类型](F:\01、java基础\笔记的截图图片\93、类名作为返回值类型.png)				
>
> ```
> 			b、抽象类：返回的是该抽象类的子类对象
> ```
>
> ![93、抽象类作为返回值类型](F:\01、java基础\笔记的截图图片\93、抽象类作为返回值类型.png)			
>
> ```
> 			c、接口:返回的是该接口的子类对象
> ```
>
> ![93、接口作为返回值类型](F:\01、java基础\笔记的截图图片\93、接口作为返回值类型.png)
>
> 

### 3、链式编程

> 每次调用完毕后，都返回一直对象
>
> ![93、链式编程](F:\01、java基础\笔记的截图图片\93、链式编程.png)

## 2.18、package关键字(包)

### 1、概念和作用

> 概念：包其实就是文件夹，
>
> 作用：
>
> ```
> 把相同的类名放到不同的包中，
> 
> 对类进行管理
> ```
>
> 

### 2、包的定义和注意事项

> 格式：
>
> ```
> package 包名;
> 多级包用“，”分开
> ```
>
> 注意事项：
>
> ```
> 1、package语句必须是程序的第一条可执行的代码
> 2、package语句在一个java文件夹中只能有一个
> 3、如果没有package，默认表示无包名
> ```
>
> 

### 3、带包的类编译和运行

> 1、手动式
>
> ```
> 1、编写一个带包的java文件
> 2、通过javac命令编译该java文件
> 3、手动创建报名
> 4、把b步骤的class文件放到c步骤的最底层包（cn.liang.xxx）
> 5、回到和包根目录在同一目录的地方，然后运行
> 	带包运行（java cn.liang.xxx.Holloworld）
> ```
>
> 2、自动式
>
> ```
> 1、编写一个带包的java文件
> 2、通过javac命令编译带上-d即可
> 		javac -d .Helloworld
> 3、运行：java cn.liang.xxx.Holloworld
> 
> ```
>
> 

### 4、面试题

> ### package,import,.class有没有顺序关系
>
> ```
> package>import>class
> ```
>
> package：只能有一个
>
> import：可以有多个
>
> class:可以有多个，以后建议是一个

### 5、权限修饰符

![94、权限修饰符](F:\01、java基础\笔记的截图图片\94、权限修饰符.png)



### 6、类以及组成所使用的常见修饰符

![95、类以及组成所使用的常见修饰符](F:\01、java基础\笔记的截图图片\95、类以及组成所使用的常见修饰符.png)

## 2.19、内部类

### 1、概念

> 把类定义在其他类的内部，这个类就是被称为内部类
>
> 

### 2、特点

> 1、内部类可以直接访问外部类的成员，包括私有
>
> 2、外部类要访问内部类的成员，必须创建对象
>
> ![96、内部类的特点](F:\01、java基础\笔记的截图图片\96、内部类的特点.png)

### 3、内部类分类

#### 3.1、内部类位置

> 成员位置：在成员位置定义的类，被称为成员内部类
>
> ```
> 如何直接访问内部类的成员
> 	外部类名.内部类名 对象名=外部类对象.内部类对象
> ```
>
> ![97、直接访问成员内部类](F:\01、java基础\笔记的截图图片\97、直接访问成员内部类.png)
>
> 局部位置：在局部位置定义的类，被称为局部内部类
>
> 

#### 3.2、成员内部类的修饰符

> private： 为了保证数据的安全性
>
> static：为了让数据访问更方便
>
> ```
> 1、注意：静态内部类只能方位外部类的静态成员
> 2、
> 成员内部类被静态修饰后的访问方式：外部类名.内部类名 对象名=new 外部类名.内部类名()；
> ```
>
> ![98、成员内部类的修饰符](F:\01、java基础\笔记的截图图片\98、成员内部类的修饰符.png)
>
> 



#### 3.3、成员内部类的面试题

> 注意：
>
> 1、内部类和外部类没有继承关系
>
> 2、通过外部类名限定this对象

![99、成员内部类的面试题](F:\01、java基础\笔记的截图图片\99、成员内部类的面试题.png)

```
1、num,this.num,new Outer().num;
2、num,this.num,Outer.this.num;
```



### 4、局部内部类

> 可以直接访问外部类的成员
>
> ![100、局部内部类访问外部类的成员](F:\01、java基础\笔记的截图图片\100、局部内部类访问外部类的成员.png)
>
> 可以创建内部类对象，通过对象调用内部类方法，来使用局部内部类功能
>
> ![100、局部内部类访问外部类的成员2](F:\01、java基础\笔记的截图图片\100、局部内部类访问外部类的成员2.png)
>
> 为

### 5、局部内部类面试题 

> 局部内部类访问局部变量的注意问题
>
> ```
> 局部内部类访问局部变量必须用final修饰
> 	为什么呢？
> 		局部变量是随着方法的调用二调用，随着调用完毕而消失
> 		而堆内存的内容并不会立即消失，所以我们加final修饰
> 		加入final修饰后，这个变量就成了常量。既然是常量，消失了
> 		我在内存中存储了数据20，所以，我还是有数据在使用
> ```
>
> ![100、局部内部类访问外部类的成员3](F:\01、java基础\笔记的截图图片\100、局部内部类访问外部类的成员3.png)

### 6、匿名内部类***

#### 格式

> 就是内部类的简化写法
>
> 前提：存在一个类或者接口，类可以是抽象，可以是具体的
>
> ```
> new 类名或接口名(){
> 	方法重写;
> }
> 本质是一个继承了该类或实现了该接口的子类匿名对象
> ```
>
> ![101、匿名内部类的格式](F:\01、java基础\笔记的截图图片\101、匿名内部类的格式.png)

#### 方法调用

> 一个方法
>
> ![101、匿名内部类的方法调用](F:\01、java基础\笔记的截图图片\101、匿名内部类的方法调用.png)

有两个方法的调用

![101、匿名内部类的方法调用2](F:\01、java基础\笔记的截图图片\101、匿名内部类的方法调用2.png)

#### 匿名内部类在开发中的应用

![101、匿名内部类在开发中的应用](F:\01、java基础\笔记的截图图片\101、匿名内部类在开发中的应用.png)

#### 面试题

> 要求按照要求，补齐代码，在控制台输出helloworld
>
> ```
> interface Inter{void show();}
> class Outer{//补齐代码}
> class OuterDemo{
> 	public static void main(String[]args){
> 		Out.method().show();
> 	}
> }
> ```
>
> ![101、匿名内部类面试题](F:\01、java基础\笔记的截图图片\101、匿名内部类面试题.png)

# 三、String类

> 字符串是由多个字符组成的一串数据。也可以看陈格式一个字符数组
>
> 通过API，我们可以知道
>
> ```
> 1、字符串字面值“abc”也可以看陈更是一个字符对象
> 2、字符串是常量，一旦赋值，其值不能被改变。
> ```
>
> 

## 3.1、String类的构造方法

### 1、空构造

> ```
> public String ():空构造
> ```
>
> 

### 2、把字节数组转成字符串

> ```
> public String(byte[] bytes):
> ```
>
> ```
> public class StringDemo {
>     public static void main(String[] args) {
>         String s1=new String();
>         System.out.println("s1:"+s1);
>         System.out.println("s1.length():"+s1.length());
>     }
> }
> 
> ```
>
> 



### 3、把字节数组的一部分转成字符串

> ```
> public String(byte[] bytes,int index,int length):
> ```

```
public class StringDemo {
    public static void main(String[] args) {
        byte[] bys={97,98,99,100};
        String s1=new String(bys);
        System.out.println("s1:"+s1);
        System.out.println("s1.length():"+s1.length());
    }
}

```



### 4、把字符数组转成字符串

> ```
> public String (char[] value)
> ```
>
> ```
> public class StringDemo {
>     public static void main(String[] args) {
>         byte[] bys={97,98,99,100};
>         String s1=new String(bys,1,3);
>         System.out.println("s1:"+s1);
>         System.out.println("s1.length():"+s1.length());
>     }
> }
> ```
>
> 

### 5、把字符数组的一部分转成字符串

> ```
> public String (char[]value,int index,int count)//包左不包右
> ```
>
> ```
> public class StringDemo {
>     public static void main(String[] args) {
>        char[]chs={'a','b','c','d','e','爱','我'};
>         String s1=new String(chs,5,2);
>         System.out.println("s1:"+s1);
>         System.out.println("s1.length():"+s1.length());
>     }
> }
> ```

### 6、把字符串常量值转成字符串

> ```
> public String(String original)
> ```
>
> ```
> public class StringDemo {
>     public static void main(String[] args) {
>         //String s1=new String("abcde");
>         String s1="abcde";
>         System.out.println("s1:"+s1);
>         System.out.println("s1.length():"+s1.length());
>     }
> }
> 
> ```



## 3.2、String类的特点

### 1、字符串是常量，他得知在创建后不能改变

```
String s="hello";
s+=“world”;
问s的结果是多少？
s=helloworld
```

> ![102、String的特点](F:\01、java基础\笔记的截图图片\102、String的特点.png)

## 3.3、面试题

### 1、String s=new String("hello")和String s="hello"的区别

> 有，前者会创建两个对象，后者创建1个对象
>
> ![103、String字面值对象和构造方法创建爱你对象的区别](F:\01、java基础\笔记的截图图片\103、String字面值对象和构造方法创建爱你对象的区别.png)

### 2、字符串比较之看程序写结果

> ```
> public class StringDemo {
>     public static void main(String[] args) {
>         String s1=new String("hello");
>         String s2=new String("hello");
>         System.out.println(s1==s2);
>         System.out.println(s1.equals(s2));
> 
>         String s3=new String("hello");
>         String s4="hello";
>         System.out.println(s3==s4);
>         System.out.println(s3.equals(s4));
> 
>         String s5="hello";
>         String s6="hello";
>         System.out.println(s5==s6);
>         System.out.println(s5.equals(s6));
>     }
> }
> ```
>
> 

### 3、字符串拼接之看程序写结果

> 字符串如果是变量相加，先开空间，然后在拼接
>
> 字符串如果是常量相加，先加，然后在常量池找，如果有就返回，如果没有就创建

> ```
> public class StringDemo {
>     public static void main(String[] args) {
>         String s5="hello";
>         String s6="world";
>         String s7="helloworld";
>         System.out.println(s7==s6+s5);
>         System.out.println(s7.equals(s5+s6));
>         System.out.println(s7=="hello"+"world");//"hello"+"world"是常量，先加再常量池里找，如果有就直接返回，否则就创建
>         System.out.println(s7.equals("hello"+"world"));
>     }
> }
> ```

## 3.4、String类的方法

### 1、判断

#### A、比较字符串的内容是否相同

```
boolean equels(Object obj):
```

#### B、比较字符串的内容是否相同，忽略大小写

```
boolean equelsIgnoreCase(String str):
```



#### C、判断大字符串中是否包含小字符串

```
boolean contians(String str)：
```



#### D、判断字符串是否以xxx开头

```
boolean startsWith(String str):
```



#### E、判断字符串是否以xxx结尾

```
boolean endsWith(String str):
```



#### F、判断字符串是为空

```
boolean isEmpty():
```

#### 注意：

字符串内容为空和字符串对象为空

```
String s="";//字符串内容为空
String s=null;//字符串对象为空
```

#### 2、登录案例

> 模拟登陆，给三个机会，并提示还有几次
>
> ```
> public class GuessNumberGame {
>     public static void start() {
>         // int number=(int)(Math.random()*100)+1;
>         Random random = new Random();
>         int number = random.nextInt(100) + 1;
>         System.out.println(number);
>         while (true) {
> 
>             Scanner scanner = new Scanner(System.in);
>             System.out.println("请输入你要猜的数字");
>             int guessNumber = scanner.nextInt();
> 
>             if (number == guessNumber) {
>                 System.out.println("恭喜你猜中了");
>                 break;
>             } else {
>                 if (number > guessNumber) {
>                     System.out.println("你猜的数小了");
>                 } else {
>                     System.out.println("你猜的数大了");
>                 }
>             }
> 
>         }
>     }
> }
> ```
>
> ```
> public class StringDemo {
>     public static void main(String[] args) {
>         Scanner scanner = new Scanner(System.in);
>         //while (true) {
>         for (int i = 1; i <= 3; i++) {
>             System.out.println("请输入用户名");
>             String userName = scanner.nextLine();
>             System.out.println("请输入密码");
>             String password = scanner.nextLine();
>             if ((userName.equals("") || userName == null) || (password.equals("") || password == null)) {
>                 System.out.println("用户名或者密码不能为空");
>             } else {
>                 if (userName.equals("888") && password.equals("888")) {
>                     System.out.println("登录成功,开始玩游戏");
>                     GuessNumberGame.start();
>                     break;
>                 } else {
>                     if (i >= 3) {
>                         System.out.println("错误密码输入3次，请联系管理员");
>                         break;
>                     } else {
>                         System.out.println("你还有" + (3 - i) + "次机会");
>                     }
>                 }
>             }
>         }
>     }
> }
> ```
>
> 

### 2、获取功能

> 获取字符串的长度

```
int length();
```



> 获取指定索引位置的字符

```
char charAt(int index)
```



> 返回指定字符在此字符串中第一次出现的索引

```
int indexOf(int ch)
	为什么治理是int类型，而不是char类型
		原因是‘a’和97其实都可以代表‘a’
```

> 返回指定字符串在此字符串中第一次出现的索引

```
int indexOf(String str)
	为什么治理是int类型，而不是char类型
		原因是‘a’和97其实都可以代表‘a’
```

> 返回指定字符在此字符串中从指定位置后第一次出现的索引

```
int indexOf(int ch,int fromIndex)
```

> 返回指定字符串在此字符串中从指定位置后第一次出现的索引

```
int indexOf(String str,int fromIndex)
```

> 从指定位置开始截取字符串，默认到末尾

```
String subString(int start)
```

> 从指定位置开始到结束截取字符串

```
String subString(int start,int end)
```

### 3、字符串的遍历

> 遍历获取字符串中的每一个字符
>
> ```
> public class StringTest {
>     public static void main(String[] args) {
>         String s="helloworld";
>         for (int i=0;i<s.length();i++){
>             char c = s.charAt(i);
>             System.out.print(c+" ");
>         }
> 
>     }
> }
> ```



#### A、统计字符个数

> 一个字符串中大写字母字符，小写字母字符，数字字符出现的次数（不考虑其他字符）
>
> 举例“Hello123World”
>
> ```
> package com.liang.string;
> 
> public class StringTest {
>     public static void main(String[] args) {
>         String s = "Hello123World";
> 
>         getCount(s);
> 
>     }
> 
>     private static void getCount(String s) {
>         int max = 0;
>         int min = 0;
>         int num = 0;
>         for (int i = 0; i < s.length(); i++) {
>             char ch = s.charAt(i);
>             if (ch > 'a' && ch < 'z') {
>                 min++;
>             }
>             if (ch > 'A' && ch < 'Z') {
>                 max++;
>             }
>             if (ch > '0' && ch < '9') {
>                 num++;
>             }
>         }
>         System.out.println("大写字母字符有" + max + "个，小写字母字符有" + min + "个，数字字符有" + num + "个");
>     }
> 
>     private static void printString(String s) {
>         for (int i = 0; i < s.length(); i++) {
>             char c = s.charAt(i);
>             System.out.print(c + " ");
>         }
>     }
> 
> }
> 
> ```

### 4、字符串的转换

> 把字符串转换为字节数组

```
byte[] getBytes()
```

> 把字符串转换成字符数组

```
char[] toCharArray()
```

> 把字符数组转成字符串

```
static String valueOf(char[]chs)
```

> 把int类型的数据转成字符串

```
static String valueOf(int i)
```

> 把字符串转成小写

```
String toLowerCase()
```

> 把字符串转成大写

```
String concat(String str)
```

#### 1)、练习

> 把一个字符串的首字母转成大写，其他为小写
>
> ```
> public class StringTest {
>     public static void main(String[] args) {
>         String s = "helloWOELD";
> 
>         getOther(s);
> 
>     }
> 
>     private static void getOther(String s){
>         String s2 = s.substring(0, 1).toUpperCase();
>         String s1 = s.substring(1).toLowerCase();
> 
>         System.out.println(s2.concat(s1));
>     }
>  }   
> ```



### 5、字符串的其他功能

1）、替换功能

```
String replace(char old,char new)
```

```
String replace(String old,String new)
```

2）、去除字符串两空格

```
String trim()
```

3）、按照字典顺序比较两个字符串

```
int compareTo(String str)
```

```
int compareToIgnoreCase(String str)
```

#### A、把int数组拼接字符串

> int [] arr={1，2，3}输出结果是[1,2,3]
>
> ```
> public class StringTest {
>     public static void main(String[] args) {
>         int []arr={1,2,3};
>         printArr(arr);
> 
>     }
>     private static void printArr(int []arr){
>         System.out.print("[");
>         for (int i = 0; i <arr.length ; i++) {
>             if(i==arr.length-1){
>                 System.out.println(arr[i]+"]");
>             }else {
>                 System.out.print(arr[i]+",");
>             }
>         }
>     }
>  }
> ```



#### B、字符串翻转

> 键盘录入“abc”,输出结果：“cba”
>
> ```
> public class StringTest {
>     public static void main(String[] args) {
>         String s="abc123";
>         stringToReserve(s);
> 
>     }
>     private static void stringToReserve(String s){
>         char[] chars = s.toCharArray();
>         for(char i=0;i<chars.length/2;i++){
>             char temp=chars[chars.length-1-i];
>             chars[chars.length-1-i]=chars[i];
>             chars[i]=temp;
>         }
>         System.out.println(String.valueOf(chars));
>     }
>   }
> ```



C、统计大串中小串出现的次数

> woaijavawozhendeaijavawozhendeaijavawozhendehenaijavaxinbuxinwoaijavagun中java出现了5次

```
public class StringTest {
    public static void main(String[] args) {
        String s="woaijavawozhendeaijavawozhendeaijavawozhendehenaijavaxinbuxinwoaijavagun";
        String small="java";
        int count=getCount2(s,small);
        System.out.println(count);

    }

    private static int getCount2(String s, String small) {
        int count=0;
        int index;
        while((index=s.indexOf(small))!=-1){
            count++;
            s=s.substring(index+small.length());
        }
        return count;
    }
 }

```

# 四、StringBuffer类

## 1、概述

> 如果对字符串进行拼接操作，每次拼接都会构建一个新的String，既耗时，又浪费空间，StringBuffer就可以解决这个问题
>
> 线程安全的可变字符序列

## 2、StringBuffer和String的区别？

> StringBuffer长度和内容可变，String都不可变
>
> 如果使用前者做字符串拼接，不会浪费太多的资源

## 3、构造方法

> 无参构造
>
> ```
> public StringBuffer()
> ```
>
> 

> 指定容量的字符串缓冲区对象
>
> ```
> public StringBuffer(int capacity)
> ```
>
> 



> 指定字符串内容的字符串换中去对象
>
> ```
> public StringBuffer(String str)
> ```
>
> 

## 4、StringBuffer的方法

### 1)、添加功能

> 可以把任意类型添加到字符串缓冲区里面

```
public StringBuffer append(String str)
```

> 指定位置吧任意类型的数据插入到字符串缓冲区里面，并放回字符串缓冲区本身

```
public StringBuffer insert(int offset,String str)
```



### 2)、删除功能

> 删除指定位置的字符，并返回本身（删除一个）

```
public StringBuffer deleteCharAt(int index):索引从0开始
```

> 删除从指定位置开始指定位置结束的内容，并返回本身

```
public StringBuffer delete(int start,int end)：从0开始，包左不包右
```



### 3)、替换功能

> 从start开始到end用str替换

```
public StringBuffer replace(int start,int end,String str)
```

### 4)、反转功能

```
public StringBuffer reverse()
```

### 5)、截取功能

`返回的不再是StringBuffer本身`

```
public String subString(int start)
```



```
public String subString(int start,int end)
```

### 6)、练习

> 1、StringBuffer和String的相互转换
>
> ```
> String转成StringBuffer
> String s="hello";
> StringBuffer sb=new StringBuffer(s);
> 或者
> StringBuffer sb=new StringBuffer();
> sb.append(s);
> ```
>
> ```
> StringBuffer转成String
> StringBuffer sb=new StringBuffer("s");
> String str=new String(sb);
> 或者
> String str=sb.toString();
> ```
>
> 

#### A、把数组拼接成指定格式的字符串

> ![104、把数组拼接成一个字符串_StringBuffer](F:\01、java基础\笔记的截图图片\104、把数组拼接成一个字符串_StringBuffer.png)

#### B、字符串翻转

> ![105、StringBuffer字符串反转](F:\01、java基础\笔记的截图图片\105、StringBuffer字符串反转.png)

#### C、判断一个字符串是否对称

> ```
> public class StringBufferDemo {
>     public static void main(String[] args) {
>         String s="abvba";
>         System.out.println(isSame(s));
> 
>     }
>     public static boolean isSame(String s){
>         boolean flag=false;
>         char[] chars = s.toCharArray();
>         for(int start=0,end=chars.length-1;start<=end;start++,end--){
>             if(chars[start]==chars[end]){
>                 flag=true;
>             }
>         }
>         return flag;
>     }
> 
> }
> 
> ```
>
> 方法2
>
> ```
> public class StringBufferDemo {
>     public static void main(String[] args) {
>         String s="abvba";
>         System.out.println(isSame2(s));
> 
>     }
>     public static boolean isSame2(String s){
>         return new StringBuffer(s).reverse().toString().equals(s);
>     }
> }
> ```
>
> 

## 5、StringBuffer的面试题

### 1）、String，StringBuffer，StringBuilder的区别

> ```
> 1、String是内容不可变的，StringBuffer，Stringbuilder都是内容可变的
> 
> 2、StringBuffer是同步的，数据安全，效率低；StringBuilder是不同步的，数据不安全的，效率高
> ```
>
> 

### 2）、StringBuffer和数组的区别

> ```
> StringBuffer和数组都可以看作是一个容器，装其他的数据，但是StringBuffer最终的数据是一个字符串数据
> 而数组可以放多种数据，但必须是同一种类型
> ```
>
> 

#### 3）、看程序写结果

> String作为参数传递
>
> StringBuffer作为参数传递
>
> ![106、StringBuffer面试题3](F:\01、java基础\笔记的截图图片\106、StringBuffer面试题3.png)
>
> ```
> 注意：
> 基本类型：形式参数的改变不影响实际参数
> 引用类型：形式参数的改变直接影响实际参数
> ```
>
> 

# 五、数组高级

## 1、冒泡排序

> 原理图解
>
> ![108、冒泡排序_原理图解](F:\01、java基础\笔记的截图图片\108、冒泡排序_原理图解.png)

> 代码实现
>
> ![108、冒泡排序_代码实现](F:\01、java基础\笔记的截图图片\108、冒泡排序_代码实现.png)

## 2、选择排序

> 原理图解
>
> ![109、选择排序_原理图解](F:\01、java基础\笔记的截图图片\109、选择排序_原理图解.png)

> 代码实现
>
> ![109、选择排序_代码实现png](F:\01、java基础\笔记的截图图片\109、选择排序_代码实现png.png)

> 案例：把字符串进行排序
>
> “adcgebf”--->abcdefg

## 3、二分查找

> 原理图解
>
> ![110、二分查找_原理图解](F:\01、java基础\笔记的截图图片\110、二分查找_原理图解.png)

> 代码实现
>
> ![110、二分查找_代码实现](F:\01、java基础\笔记的截图图片\110、二分查找_代码实现.png)

```
二分查找注意事项：
```



> ```
> 插入排序，归并排序，快速排序，冒泡排序，希尔排序，选择排序，（舞动的排序算法视频）
> ```
>
> ![107、数组排序的种类](F:\01、java基础\笔记的截图图片\107、数组排序的种类.png)

## 4、Arrays工具类

# 六、集合框架

> 数组和集合的区别
>
> ![111、数组和集合的区别](F:\01、java基础\笔记的截图图片\111、数组和集合的区别.png)
>
> 

## 1、Collection

### 1.1、Collection的基本功能

> ![112、Collection的功能](F:\01、java基础\笔记的截图图片\112、Collection的功能.png)

> ```
> add：添加一个元素(可重复添加元素)
> clear：移除所有元素
> remove：移除一个元素
> contains:判断集合中是否包含指定元素
> isEmpty:判断集合是否为空（有元素true，没有元素false）
> size:元素个数
> ```
>
> ![113、Collection的基本功能](F:\01、java基础\笔记的截图图片\113、Collection的基本功能.png)



> ```
> addAll:
> removeAll:只要有一个元素被移除，就返回true
> containsAll:只有包含所有的元素才叫包含，才返回true
> retainAll:如果有交集，就是true，没有就false
> ```
>
> ![113、Collection的基本功能2](F:\01、java基础\笔记的截图图片\113、Collection的基本功能2.png)

### 1.2、集合的遍历

> 
>
> ![113、Collection的遍历](F:\01、java基础\笔记的截图图片\113、Collection的遍历.png)

### 1.3、数组转对象遍历



> Collection自定义对象练习
>
> ```
> Student--age ，name
> ```
>
> ![113、Collection的自定义对象并遍历](F:\01、java基础\笔记的截图图片\113、Collection的自定义对象并遍历.png)

### 1.4、迭代器遍历

> ![113、Collection的迭代器遍历](F:\01、java基础\笔记的截图图片\113、Collection的迭代器遍历.png)

### 1.5、自定义对象迭代器遍历

> ![113、Collection的自定义对象-迭代器遍历](F:\01、java基础\笔记的截图图片\113、Collection的自定义对象-迭代器遍历.png)

### 1.6、迭代器的原理

> ![114、迭代器的原理](F:\01、java基础\笔记的截图图片\114、迭代器的原理.png)

### 1.7、练习

#### 1）、存储字符串并遍历

> ![115、练习-字符串遍历](F:\01、java基础\笔记的截图图片\115、练习-字符串遍历.png)

#### 2）、自定义对象遍历

> ```
> Student ---name,age
> ```
>
> ![115、练习-自定义对象遍历](F:\01、java基础\笔记的截图图片\115、练习-自定义对象遍历.png)

### 2.1、List

> 包含重复元素并且有序

#### 2.1.1、List集合的遍历

> ```
> 1、存储字符串并遍历
> ```
>
> ![116、List存储字符串遍历](F:\01、java基础\笔记的截图图片\116、List存储字符串遍历.png)



> ```
> 2、存储自定义对象并遍历
> ```
>
> ![116、List存储自定义对象遍历](F:\01、java基础\笔记的截图图片\116、List存储自定义对象遍历.png)

#### 2.1.2、List的特点

> 有序（存储和取出的元素一致），可重复

#### 2.1.3、List的特有功能

> ![116、list集合的特有功能](F:\01、java基础\笔记的截图图片\116、list集合的特有功能.png)
>
> 代码：
>
> ![116、list集合的特有功能-代码](F:\01、java基础\笔记的截图图片\116、list集合的特有功能-代码.png)
>
> 特有的遍历功能
>
> ![116、list集合的特有功能迭代-代码](F:\01、java基础\笔记的截图图片\116、list集合的特有功能迭代-代码.png) 

#### 2.1.1、ArrayList

> ![118、ArrayList遍历-字符串](F:\01、java基础\笔记的截图图片\118、ArrayList遍历-字符串.png)

> 自定义对象遍历
>
> ```
> student--age,name
> ```
>
> ![118、ArrayList遍历-自定义对象](F:\01、java基础\笔记的截图图片\118、ArrayList遍历-自定义对象.png)

> 增强for（用来代替迭代器的）
>
> ```
> 遍历字符串
> ```
>
> ![126、增强for遍历ArrayList字符串](F:\01、java基础\笔记的截图图片\126、增强for遍历ArrayList字符串.png)；
>
> ```
> 自定义对象遍历
> ```
>
> ![126、增强for遍历ArrayList-自定义对象](F:\01、java基础\笔记的截图图片\126、增强for遍历ArrayList-自定义对象.png)

#### 2.1.2、Vector

##### 2.1.2.1、Vector特有方法

> ![119、Vector特有方法](F:\01、java基础\笔记的截图图片\119、Vector特有方法.png)
>
> ![119、Vector特有方法-代码](F:\01、java基础\笔记的截图图片\119、Vector特有方法-代码.png)

#### 2.1.3、LinkedList

##### 2.1.3.1、Linkedlist特有功能

> ![120、LinkedList特有功能](F:\01、java基础\笔记的截图图片\120、LinkedList特有功能.png)
>
> ![120、LinkedList特有功能-代码](F:\01、java基础\笔记的截图图片\120、LinkedList特有功能-代码.png)
>
> 

##### 2.1.3.2、LinkedList实现栈结构的集合代码

> ```
> 请用LinkedList模拟栈数据结构的集合，并测试
> ```
>
> ![122、LinkedList模拟栈数据结构的集合](F:\01、java基础\笔记的截图图片\122、LinkedList模拟栈数据结构的集合.png)
>
> 

#### 2.1.4、List三个子类的特点

> ![116、List的子类特点](F:\01、java基础\笔记的截图图片\116、List的子类特点.png)

#### 2.1.5、List练习

##### 1、去除Array集合中的重复字符串元素

> 
>
> 方法1：
>
> ![121、ArrayList去重复值](F:\01、java基础\笔记的截图图片\121、ArrayList去重复值.png)
>
> ```
> 方法2
> ```
>
> ![121、ArrayList去重复值2](F:\01、java基础\笔记的截图图片\121、ArrayList去重复值2.png)
>
> 

##### 2、去除集合中自定义对象的重复值

> ```
> 对象的成员变量值都相同，
> Student --age,name,equels()
> ```
>
> ![121、ArrayList自定义对象去重复值](F:\01、java基础\笔记的截图图片\121、ArrayList自定义对象去重复值.png)

### 2.2、泛型

> ```
> 字符串泛型
> ```
>
> ![123、泛型1](F:\01、java基础\笔记的截图图片\123、泛型1.png)
>
> ```
> 自定义对象泛型
> ```
>
> ![123、泛型2](F:\01、java基础\笔记的截图图片\123、泛型2.png)

#### 2.2.1、Object转型问题引入泛型

> ![124、Object转型问题引入泛型](F:\01、java基础\笔记的截图图片\124、Object转型问题引入泛型.png)

#### 2.2.2、泛型类

> ![125、泛型类](F:\01、java基础\笔记的截图图片\125、泛型类.png)

#### 2.2.3、泛型方法

> ![125、泛型方法](F:\01、java基础\笔记的截图图片\125、泛型方法.png)

#### 2.2.4、泛型接口

> ![125、泛型接口](F:\01、java基础\笔记的截图图片\125、泛型接口.png)

#### 2.2.5、泛型通配符

> ![125、泛型高级之通配符](F:\01、java基础\笔记的截图图片\125、泛型高级之通配符.png)

#### 2.2.5、可变参数

> ![127、可变参数](F:\01、java基础\笔记的截图图片\127、可变参数.png)

##### 2.2.5.1、Arrays工具类

> ```
> 把数组转成集合
> ```
>
> ![128、Arraysd的asList数组转集合](F:\01、java基础\笔记的截图图片\128、Arraysd的asList数组转集合.png)

#### 2.2.6、练习

> ```
> 产生10个1-20之间的随机数
> 	随机数不能重复
> ```
>
> ![129、练习1](F:\01、java基础\笔记的截图图片\129、练习1.png)
>
> ```
> 练习2：键盘录入多个数据，0结束，要求控制台输出这个数据中的最大值
> ```
>
> ![129、练习2](F:\01、java基础\笔记的截图图片\129、练习2.png)

### 2.3、Set

> ```
> 不包含重复元素，无序（存储顺序和取出顺序不一致）
> 虽然set结合的元素无序，但是作为集合来说，他有自己的存储顺序，而你的顺序恰好和它的存储顺序一致，这代表不了有序，
> ```
>
> ![130set集合概述及特点](F:\01、java基础\笔记的截图图片\130set集合概述及特点.png)

#### 2.3.1、HashSet

> ```
> 它不保证set的迭代顺序；特别是它不保证书序恒久不变
> ```

##### 1、存储字符串并遍历

> 
>
> ![131、HashSet存储字符串并遍历](F:\01、java基础\笔记的截图图片\131、HashSet存储字符串并遍历.png)
>
> ```
> 为什么存储字符串的时候，字符串内容相同的只存储一个呢？
> 	查看add方法的源码，知道这个方法底层依赖hashCode和equals方法
> 步骤：
> 	1.首先比较哈希值
> 	2.如果相同，继续走，比较地址值或者走equals()
> 	3.如果不同，直接添加到集合中
> 按照方法的步骤来说：
> 	先看hashCode()值是否相同
> 		相同：继续走equals()方法
> 				返回ture:说明元素重复，就不添加了
> 				返回false：说明元素不重复，就添加到集合
> 		不同：就字节把元素添加到集合
> 如果类没有重写这着两个方法，默认使用Object().一般来说不会相同
> 而String类重写了hashCode（）和equals()方法，所以，他就可以把内容相同的字符串去掉，只留下一个
> ```
>
> 

##### 2、存储自定义对象并遍历

> ```
> student--age,name,重写hashCode（）和equals方法
> ```
>
> 图解
>
> ![131、HashSet保证元素唯一性的图解](F:\01、java基础\笔记的截图图片\131、HashSet保证元素唯一性的图解.png)
>
> 代码
>
> ![131、HashSet存储自定义对象并遍历](F:\01、java基础\笔记的截图图片\131、HashSet存储自定义对象并遍历.png)
>
> 

#### 2.3.2、LinkedSet

> ```
> 底层数据结构有哈希表和链表组成
> 哈希表保证元素的唯一性
> 链表保证元素有序（存储和取出是一致的）
> ```
>
> ![131、LinkedhashSet](F:\01、java基础\笔记的截图图片\131、LinkedhashSet.png)

#### 2.3.3、TreeSet

> ```
> TreeSet：能够对元素按照某种规则进行排序
> 	排序有两种方式
> 		1.自然排序
> 		2.比较器排序
> TreeSet集合的特点：排序和唯一
> ```
>
> ![132、TreeSet的概述](F:\01、java基础\笔记的截图图片\132、TreeSet的概述.png)
>
> 

##### 2.3.3.1、TreeSet保证元素唯一性和自然排序的原理和图解

> ![132、TreeSet保证元素唯一性图解](F:\01、java基础\笔记的截图图片\132、TreeSet保证元素唯一性图解.png)



###### 1、自定义对象遍历

> ```
> Student--compareTo重写
> ```
>
> ![132、compareTo方法重写](F:\01、java基础\笔记的截图图片\132、compareTo方法重写.png)
>
> ![132、TreeSet自定义对象遍历](F:\01、java基础\笔记的截图图片\132、TreeSet自定义对象遍历.png)；
>
> 

##### 2.3.3.2、TreeSet保证元素唯一性和比较器的原理和图解

> ```
> student--age,name
> 比较器
> ```
>
> 1.比较器根据姓名的长度
>
> ![132、TreeSet比较器排序](F:\01、java基础\笔记的截图图片\132、TreeSet比较器排序.png)
>
> 自定义对象
>
> ![132、TreeSet比较器排序自定义对象遍历 ](F:\01、java基础\笔记的截图图片\132、TreeSet比较器排序自定义对象遍历 .png)
>
> 匿名内部类的方式
>
> ![132、TreeSet比较器排序（匿名内部类）自定义对象遍历 ](F:\01、java基础\笔记的截图图片\132、TreeSet比较器排序（匿名内部类）自定义对象遍历 .png)
>
> 



##### 2.3.3.3、总结

> ![133、TreeSet对元素排序的总结](F:\01、java基础\笔记的截图图片\133、TreeSet对元素排序的总结.png)

## 2、Map

### 2.1、Map集合的特点

```
可以存储键值对的元素，将键映射到值得对象，一个映射不能好汉重复值，每个键最多只能映射到一个值。
		键是set（不可重复复）集合，值是list（可重复）集合
```

#### Map集合和Collection集合的区别

```
Map集合：Map是双列的，存储元素是成对出现的，键是唯一的，值是可重复的，数据结构值针对键有效，跟值无关
Collection集合：单列的，存储集合是单独出现的，Collection的子类Set是唯一的，List是可重复的，数据结构是针				对元素有效
```



### 2.2、Map集合的功能(方法)

![134、Map集合功能概述](F:\01、java基础\笔记的截图图片\134、Map集合功能概述.png)

#### 添加功能

` V put(K key,V value)`

```
	public static void main(String[] args) {
		Map<String,String>map=new HashMap<String,String>();
		map.put("文章", "马伊琍");
		map.put("邓超", "孙俪");
		map.put("周杰伦", "昆凌");
		System.out.println("map:"+map);
	}
```

#### 删除功能

` void clear`

`V remove(Object key)`

#### 判断功能

`boolean containsKey(Object key)`

#### 获取功能

`V get(Object key):根据键获取值`

`Set<K>keySet():获取集合中所有键的集合`

`Collection<V>values:获取集合中所有值得集合`

```
public class MapDemo {
	public static void main(String[] args) {
		Map<String,String>map=new HashMap<String,String>();
		map.put("文章", "马伊琍");
		map.put("邓超", "孙俪");
		map.put("周杰伦", "昆凌");
		
		System.out.println("map:"+map.get("周杰伦"));
		System.out.println("map:"+map.get("周杰"));
		
		Set<String>set=map.keySet();
		for(String key:set){
			System.out.println(key+"----"+map.get(key));
			
		}
		Collection<String>con=map.values();
		for(String value:con){
			System.out.println(value);
		}
	}
}
```

`Set<Map.entry<K,V>>entrySet():返回的是键值对对象的集合`

```
	Map<String,String>map=new HashMap<String,String>();
		map.put("文章", "马伊琍");
		map.put("邓超", "孙俪");
		map.put("周杰伦", "昆凌");
		
		Set<Map.Entry<String,String>>set1=map.entrySet();
		for(Map.Entry<String, String> me:set1){
			System.out.println(me.getKey()+"---"+me.getValue());
		}
```



#### 长度功能

`int size():返回集合中的键值对的对数`

#### Map集合遍历图解

![135、Map集合遍历图解](F:\01、java基础\笔记的截图图片\135、Map集合遍历图解.png)



### 2.3、HashMap

> HashMap是基于哈希表的Map接口实现。(唯一，无序)
> 哈希表的作用是用来保证键的唯一性的

![136、HashMap遍历](F:\01、java基础\笔记的截图图片\136、HashMap遍历.png)

#### 2.3.1、LinkedHashMap

> 是Map接口的哈希表和链接列表实现，具有可预知的迭代顺序
>
> ​	由哈希表保证键的唯一性
>
> ​	由链表保证键的有序（存储和取出的顺序一致）

![137、LinkedHashMap](F:\01、java基础\笔记的截图图片\137、LinkedHashMap.png)

### 2.4、TreeMap

> 是基于红黑树的Map接口的实现

![138、TreeMap](F:\01、java基础\笔记的截图图片\138、TreeMap.png)

### 2.5、练习

> 统计字符串中每个字符出现的次数

```
public class MapTest {

	public static void main(String[] args) {
		String s="aabbcceedlajdosfjali";
		HashMap<String,Integer>hm=new HashMap<>();
		
		char[] chs=s.toCharArray();
		for(int i=0;i<chs.length;i++){
			String str=String.valueOf(chs[i]);
			if(!hm.containsKey(str)){
				hm.put(str, 1);
			}else{
				hm.put(str, hm.get(str)+1);
			}
		}
		Set<String>set=hm.keySet();
		for(String ss:set){
			Integer value=hm.get(ss);
			System.out.print(ss+"("+value+")"+" ");
		}

	}
}
```

### 2.6、面试题

> Hashtable和HashMap的区别

```
Hashtable:县城安全，效率低，不允许null键和null值
```



```
HashMap：线程不安全，效率高，允许null键和null值
```





> List，Set，Map等接口是否都继承自Map接口

```
List，Set不是继承自Map接口，他是继承自Collection接口
Map本身就是一个顶层接口
```



> 常见的集合类有哪些，都有什么方法

```
ArrayList，LinkedList，HashMap，TreeSet
添加，删除，遍历，获取，删除等
```

### 2.7、Collections工具类

> 是针对集合进行操作的工具类，都是静态方法

#### 2.7.1、Collection和Collections的区别

> Collection：是单列集合的顶层接口，有子类List和Set
>
> Collections:是针对集合操作的工具类，有对集合进行排序和二分查找的方法

![139、Collections工具类方法](F:\01、java基础\笔记的截图图片\139、Collections工具类方法.png)



## 3、集合总结

### 3.1、集合的特点

![140、集合总结_集合的特点](F:\01、java基础\笔记的截图图片\140、集合总结_集合的特点.png)

### 3.2、如何选择使用哪种集合？

![141、如何选择使用哪种集合](F:\01、java基础\笔记的截图图片\141、如何选择使用哪种集合.png)

### 3.3、集合的常见方法和遍历

![142、集合的常见方法和遍历方式](F:\01、java基础\笔记的截图图片\142、集合的常见方法和遍历方式.png)

# 七、数据结构

> 常见数据结构的优缺点
>
> 

## 1、栈

先进后出

> ![117、栈的原理](F:\01、java基础\笔记的截图图片\117、栈的原理.png)
>
> 

## 2、队列

先进先出

> ![117、队列的原理](F:\01、java基础\笔记的截图图片\117、队列的原理.png)
>
> 

## 3、数组

查询快，增删慢

> ![117、数组的原理](F:\01、java基础\笔记的截图图片\117、数组的原理.png)
>
> 

## 4、链表

> 增删快，查询慢
>
> ![117、链表的原理](F:\01、java基础\笔记的截图图片\117、链表的原理.png)

## 5、树

## 6、哈希表

# 八、IO流

> 用来进行设备间的数据传输问题：上传文件和下载文件
>
> 

```
数据流向：
	输入流(InputStream)	读取数据（读入）
	输出流(OutputStream)	写出数据
数据类型：
	字节流
	字符流（为了方便操作文本数据，java提供了字符流）

以后到底是用哪种类型的流呢？
	如果操作的数据是文本数据，就用字符流，
		把你要操作的文件用windows自带的记事本打开，
			如果你能读懂，就用字符流
			读不懂，就用字节流
	如果你什么都不知道，就用字节流	
```



## 1、异常

> 程序出现了不正常的情况

### 1.1、异常的分类

#### Trowable

> 程序的异常

##### Error

> 严重问题，我们不处理。一般这种都是很严重的，比如说内存溢出

##### Exception

> 问题

###### 不是RuntimeException

> 编译期问题，必须进行处理，因为你不处理，编译就不通过

###### RuntimeException

> 运行期问题，这种问题我们也不处理，因为这个问题出现肯定是我们的代码不够严谨，需要修正代码

#### 图解

![143、异常分类](F:\01、java基础\笔记的截图图片\143、异常分类.png)



#### 代码

```
public class ExceptionDemo {

	public static void main(String[] args) {
		int i =10;
		int j=0;
		System.out.println(i/j);
		System.out.println("over");

	}

}
Exception in thread "main" java.lang.ArithmeticException: / by zero
	at com.javase.exception.ExceptionDemo.main(ExceptionDemo.java:8)
```



### 1.2、处理异常



#### A、try..catch

> try里面的代码越少越好,catch里面必须有内容

```
public class ExceptionDemo {

	public static void main(String[] args) {
	    int i =10;
		int j=0;
		try{			
			System.out.println(i/j);
		}catch(Exception e){
			e.printStackTrace();
		}
		System.out.println("over");
	}

}
java.lang.ArithmeticException: / by zero
over
	at com.javase.exception.ExceptionDemo.main(ExceptionDemo.java:9)

```

#### B、try...catch...finally

> finally的特点及作用
>
> ​	特点：被finally控制的语句体一定会执行，jvm执行到finally之前退出的除外

```
public class ExceptionDemo {

	public static void main(String[] args) {
		try{
			int i =10;
			int j=0;
			System.out.println(i/j);
		}catch(Exception e){
			e.printStackTrace();
		}finally{
			System.out.println("finally");
		}
		System.out.println("over");

	}
}
java.lang.ArithmeticException: / by zero
	at com.javase.exception.ExceptionDemo.main(ExceptionDemo.java:9)
finally
over
```



#### C、throws 抛出

```
public class ExceptionDemo {

	public static void main(String[] args)throws Exception {
		int i =10;
		int j=0;
		System.out.println(i/j);
		System.out.println("over");

	}

}
Exception in thread "main" java.lang.ArithmeticException: / by zero
	at com.javase.exception.ExceptionDemo.main(ExceptionDemo.java:8)
```



### 1.3、面试题

#### A、final，finally和finalize的区别

```
final：最终的意思，可以修饰类，成员变量，成员方法
	修饰类，类不能被继承
	修饰变量，变量是常量
	修饰方法，方法不能被重写
finally：是异常处理的一部分，用于释放资源
finalize：是Object类的一个方法，用于垃圾回收
```



#### B、catch里面有return语句，请问finally里面的代码还会执行吗

```
public class ExceptionDemo {

	public static void main(String[] args) {
		try{
			int i =10;
			int j=0;
			System.out.println(i/j);			
		}catch(Exception e){
			e.printStackTrace();
			return ;
		}finally{
			System.out.println("finally");
		}
		System.out.println("over");

	}
}
java.lang.ArithmeticException: / by zero
finally
	at com.javase.exception.ExceptionDemo.main(ExceptionDemo.java:9)
```

![144、finally面试题2](F:\01、java基础\笔记的截图图片\144、finally面试题2.png)



### 1.4、异常的注意事项

![145、异常的注意事项](F:\01、java基础\笔记的截图图片\145、异常的注意事项.png)



## 2、File类

> 文件和目录(文件夹)路径名的抽象表现形式

### 2.1、构造函数

```
File(String pathname):根据一个路径得到一个File对象
```

```
File(String parent,String child):分局一个目录和一个子文件/目录得到File对象
```

```
File(File parent,String child):根据一个父File对象和一个子文件/目录得到File对象
```

![146、File构造方法](F:\01、java基础\笔记的截图图片\146、File构造方法.png)

### 2.2、File类的功能

#### 2.2.1、创建功能

```
public boolean createNewFile()：创建文件
public boolean mkdir():创建文件夹
public boolean mkdirs():创建多层目录的文件夹
```

![147、File的创建方法](F:\01、java基础\笔记的截图图片\147、File的创建方法.png)

#### 2.2.2、删除功能

```
public boolean delete():删除文件或者文件夹
	要删除一个文件夹，文件夹内不能包含文件或者文件夹
```

```
public class FileDemo {

	public static void main(String[] args)throws Exception {
		File file=new File("files/a.txt");
		file.createNewFile();
		
		file.delete();
	}
}

```



#### 2.2.3、重命名功能

```
public boolean renameTo(File dest)
	如果是同一目录下，就是改名，
	如果不在同一目录下，就是剪切+改名
```

```
public class FileDemo {

	public static void main(String[] args)throws Exception {
		File file=new File("files/a.txt");
		file.createNewFile();
		file.renameTo(new File("files/aa.txt"));
		
	}
}
```



#### 2.2.4、判断功能

```
public boolean isDirectory():判断是否是文件夹
public boolean isFile():判断是否是文件
public boolean exists():判断是否存在
public boolean canRead():判断是否可读
public boolean canWrite():判断是否可写
public boolean isHidden():判断是否隐藏
```

![148、File判断功能](F:\01、java基础\笔记的截图图片\148、File判断功能.png)

#### 2.2.5、基本获取功能

```
public String getAbsolutePath();获取绝对路径
public String getPath();获取相对路径
public String getName();获取名称
public long length();获取长度（字节数）
public long lastModified();获取最新修改时间，毫秒值
```

![149、File基本获取功能](F:\01、java基础\笔记的截图图片\149、File基本获取功能.png)

#### 2.2.6、高级获取功能

```
public String[] list():获取指定目录下的所有文件或者文件夹的名称数组

public Fiile[] listFiles():获取指定目录下的所有文件或者文件夹的File数组
```

![150、File高级获取功能](F:\01、java基础\笔记的截图图片\150、File高级获取功能.png)

##### 文件过滤器

```
public String[] list(FilenameFileter filter)

public Fiile[] listFiles(FilenameFileter filter)
```



### 2.3、File练习

#### A、判断E盘下是否有后缀名为.jpg的文件，如果有，就输出文件名称

方式一：

![151、File练习1](F:\01、java基础\笔记的截图图片\151、File练习1.png)



方式二：

![152、File练习2](F:\01、java基础\笔记的截图图片\152、File练习2.png)

#### B、批量修改文件名

![152、File改名](F:\01、java基础\笔记的截图图片\152、File改名.png)

### 2.4、递归

```
1、递归一定要有出口，否则就是死递归
2、递归的次数不能太多，否则就内存溢出
3、构造方法不能递归使用
```

![153、递归内存图](F:\01、java基础\笔记的截图图片\153、递归内存图.png)

#### A、5的阶层

循环

```
public static void main(String[] args)throws Exception {
		int sum=1;
		for(int i=1;i<=5;i++){
			sum*=i;
		}
		System.out.println(sum);
	}
```

递归

```
public class DiGuiDemo1 {
	public static void main(String[] args)throws Exception {
		
		System.out.println(show(5));
	}
	public static int show(int n){
		if(n==1){
			return 1;
		}
		return n*show(n-1);
	}

```



#### B、E盘下所有的文件，并删除（包括文件夹）

```
public static void main(String[] args)throws Exception {
		showFile(new File("H:\\workspace"));
	}
	public static void showFile(File file){
		File[] files=file.listFiles();
		for(File f:files){
			if(f.isFile()){
				System.out.println(f.getName());
				f.delete();
			}else if(f.isDirectory()){
				showFile(f);
			}
		}
		System.out.println(file.delete());
	}
```



#### D、不死兔问题

```
题目：有一对兔子，从出生后第3个月起每个月都生1对兔子，小兔子第三个月后也可以生一对兔子，假如兔子不死，在指定月	 份时刻一共可以有多少对兔子
 分析：
 * 		第一个月：1
 * 		第二个月：1	2-1+2-2=第一个月=1
 * 		第三个月：2	前两个月之和	3-1+3-2=第一个月+第二个月=1+1
 * 		第四个月：3	前两个月之和	4-1+4-2=第三个月+第二个月=1+2
 * 		第五个月：5
 * 		第六个月：8
 * 		。。。。。
 * 		
 * 		其实指定月份兔子的总数为此月之前两个月兔子总数之和。
 * 
 * 实现3种方法
 * 		1、数组实现
 * 		2、相邻变量实现
 * 		3、递归实现
 
 //递归实现
 public static void main(String[] args)throws Exception {
		System.out.println(diGui(20));
	}
	public static int diGui(int month){
		if(month==2||month==1){
			return 1;
		}
		return diGui(month-1)+diGui(month-2);
	}
	
//数组实现
public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		System.out.println("请输入当前月份");
		int m=sc.nextInt();
		int n1=0;
		int n2=0;
		int n3=0;
		sc.close();
		
		//数组实现
		if(m<=2) {
			n1=1;
			
		}else {
			int []x=new int[m];
			x[0]=1;
			x[1]=1;
			for(int i=2;i<m;i++ ) {
				x[i]=x[i-1]+x[i-2];		
			}	
			n1=x[m-1];
		}
		System.out.println("方法一：数组实现");
		System.out.println("\t"+"第"+m+"月份共有"+n1+"对兔子");
		System.out.println("--------------------------");
		
		
		//相邻变量实现
		if(m<=2) {
			n2=1;
			
		}else {
			int a=1;
			int b=1;
			int temp=0;
			for(int i=0;i<m-2;i++) {
				temp=a;
				a=b;
				b=temp+b;
			}
			n2=b;
		}
		System.out.println("方法二：相邻变量实现");
		System.out.println("\t"+"第"+m+"月份共有"+n2+"对兔子");
		System.out.println("--------------------------");
```



## 3、字节流

> InputStream:读取
>
> ​	--FileInputStream:
>
> OutputStream：写出
>
> ​	--FileOutputStream

### 3.1、FileOutputStream

#### 3.1.1、构造函数

```
FileOutputStream (File file)
FileOutputStream (String name)
FileOutputStream (File file,boolean append):追加数据
FileOutputStream (String name,boolean append)
```

```
public static void main(String[] args)throws Exception {
		File file=new File("files//fos.txt");
		FileOutputStream fos=new FileOutputStream(file);
		fos.write("hello,id".getBytes());
		fos.close();

	}
```

#### 3.1.2、方法

```
public void write(int b):写一个字节
public void write(byte[] b):写一个字节数组
public void write(byte[] b,int off,int len):写一个字节数组的一部分
```

```
public static void main(String[] args)throws Exception {
		File file=new File("files//fos.txt");
		FileOutputStream fos=new FileOutputStream(file);
		fos.write(97);
		
		fos.close();

	}
	
	public static void main(String[] args)throws Exception {
		File file=new File("files//fos.txt");
		FileOutputStream fos=new FileOutputStream(file);
		
		byte[]bys={97,98,99,100};
		fos.write(bys);
		
		fos.close();

	}
	
	
	public static void main(String[] args)throws Exception {
		File file=new File("files//fos.txt");
		FileOutputStream fos=new FileOutputStream(file);
		
		byte[]bys={97,98,99,100};
		fos.write(bys,1,3);
		
		fos.close();

	}
```

#### 3.1.3、实现数据换行

![154、数据实现换行](F:\01、java基础\笔记的截图图片\154、数据实现换行.png)

#### 3.1.4、实现数据的追加

```
用构造方法FileOutputStream(File file,boolean append)即可
	File file=new File("files//fos.txt");
	FileOutputStream fos=new FileOutputStream(file,true);

```



### 3.2、FileInputStream

#### 3.2.1、构造函数

```
FileInputStream (File file)
FileInputStream (String name)
```



#### 3.2.2、方法

```
public void read():一次读一个字节
public void read(byte[] b):一次读一个字节数组
public void read(byte[] b,int off,int len):一次读一个字节数组的一部分
```

![155、FileInputStream一次读一个字节](F:\01、java基础\笔记的截图图片\155、FileInputStream一次读一个字节.png)

#### 3.3.3、练习

##### 1、字节流复制文本文件

![156、字节流复制文本文件](F:\01、java基础\笔记的截图图片\156、字节流复制文本文件.png)

##### 2、字节流复制文本文件2

![157、字节流复制文本文件](F:\01、java基础\笔记的截图图片\157、字节流复制文本文件.png)

##### 3、字节流复制图片

![158、字节流复制图片](F:\01、java基础\笔记的截图图片\158、字节流复制图片.png)

效率高一点的

![158、字节流复制图片2](F:\01、java基础\笔记的截图图片\158、字节流复制图片2.png)

##### 4、字节流复制视频

这种方式复制的很慢，要耐心等待

![159、字节流复制视频](F:\01、java基础\笔记的截图图片\159、字节流复制视频.png)

改进使用效率高一点的

![159、字节流复制视频2](F:\01、java基础\笔记的截图图片\159、字节流复制视频2.png)

## 4、字节缓冲区流

### 4.1、BufferedOutputStream（写入）

#### 4.1.2、构造方法

```
BufferedOutputStream (OutputStream out)
	为什么不传递一个具体的文件或者文件路径，而是传递igeOutputStream对象呢
		字节缓冲流仅仅提供缓冲区流是为了高效而设计，真正的读写操作海得靠基本的流对象实现
```

![160、BufferedOutputStream](F:\01、java基础\笔记的截图图片\160、BufferedOutputStream.png)

### 4.2、BufferedInputStream（读取）

```
BufferedInputStream (InputStream out)
```

![161、BufferedInputStream](F:\01、java基础\笔记的截图图片\161、BufferedInputStream.png)

## 5、字节流复制视频练习（四种方式）

### 5.1、基本字节流一次读写一个字节

![162、基本字节流一次读写一个字节1](F:\01、java基础\笔记的截图图片\162、基本字节流一次读写一个字节1.png)

### 5.2、基本字节流一次读写一个字节数组

![162、基本字节流一次读写一个字节数组2](F:\01、java基础\笔记的截图图片\162、基本字节流一次读写一个字节数组2.png)

### 5.3、高效字节流一次读写一个字节

![162、高效字节流一次读写一个字节3](F:\01、java基础\笔记的截图图片\162、高效字节流一次读写一个字节3.png)

### 5.4、高效字节流一次读写一个字节数组

![162、高效字节流一次读写一个字节数组4](F:\01、java基础\笔记的截图图片\162、高效字节流一次读写一个字节数组4.png)

## 6、字符流（转换流）

> 字节流读取中文在控制台，会出现小问题（可能会乱码），不是特变方便，java就提供了转换流
>
> 字符流=字节流+编码表

![163、转换流1](F:\01、java基础\笔记的截图图片\163、转换流1.png)

### 4.1、编码表

![164、编码表](F:\01、java基础\笔记的截图图片\164、编码表.png)



### 4.2、String类中的编码和解码问题

```
String (byte[] bytes,String charsetName):通过制定的字符集解码字节数组
byte[] getBytes(String charsetName):使用制定的字符集合把字符串编码为字节数组

String---byte[]:编码(把看懂的字变成看不懂的)
byte[]---String:解码(把看不懂的变成看得懂的)
```

![165、String类中的编码和解码问题](F:\01、java基础\笔记的截图图片\165、String类中的编码和解码问题.png)

### 4.3、字符流流的构造方法

```
Writer
    OutPutStreamWriter(写入)
        OutPutStreamWriter(OutputStream out):根据默认编码把字节流转换成字符流
        OutPutStreamWriter(OutputStream out,String charsetName)：根据指定编码把字节流转换成字符																	流

Reader        
    InputStreamRead(读取)、
        InputStreamRead(InputStream is):用默认的编码读取数据
        InputStreamRead(InputStream is ,String charsetName用指定的编码读取数据
	
```

### 4.4、字符流写数据的方法

```
OutputStreamWriter的方法
    public void write(int c):写一个字符
    public void write(char[] cbuf):写一个字符数组
    public void write(char[] cbuf,int off,int len):写一个字符数组的一部分
    public void write(String str):写一个字符串
    public void write(String str,int off,int len):写一个字符串的一部分
    void flush();
```



### 4.5、字符流读取数据的方法

```
InputStreamReader
	public void read():一次读取一个字符
	public void read(char[] chs):一次读取一个字符数组
```

![166、字符流复制文本文件1](F:\01、java基础\笔记的截图图片\166、字符流复制文本文件1.png)



### 4.6、练习

#### 1、字符流复制文本文件1

![166、字符流复制文本文件2](F:\01、java基础\笔记的截图图片\166、字符流复制文本文件2.png)

#### 2、字符流的子类复制文本文件

![166、字符流复制文本文件3](F:\01、java基础\笔记的截图图片\166、字符流复制文本文件3.png)



一次一个字符数组

![166、字符流复制文本文件4](F:\01、java基础\笔记的截图图片\166、字符流复制文本文件4.png)



### 4.7、字符缓冲流

> 字符流为了高效读写，提供了对应的字符缓冲流

#### 4.7.1、构造函数

```
BufferedWriter:字符缓冲输出流
	
BufferedReader(Reader in):字符缓冲输入流
	
```

#### ![167、字符缓冲流复制文本文件](F:\01、java基础\笔记的截图图片\167、字符缓冲流复制文本文件.png)

#### 4.7.2、方法

```
BufferedWriter:
	public void newLine():写入一个行分隔符,根据系统来决定换行符
BufferedReader：
	public String readLine():一次读取一行数据
```

![167、字符缓冲流复制文本文件2](F:\01、java基础\笔记的截图图片\167、字符缓冲流复制文本文件2.png)

### 4.8、IO流小结

![168、IO流小结图解](F:\01、java基础\笔记的截图图片\168、IO流小结图解.png)

## 7、练习

### 1、复制文本文件

![169、复制文本文件1](F:\01、java基础\笔记的截图图片\169、复制文本文件1.png)

### 2、复制图片

### ![169、复制图片](F:\01、java基础\笔记的截图图片\169、复制图片.png)3、把集合中的数据存到文本文件

![169、把集合中的数据存到文本文件](F:\01、java基础\笔记的截图图片\169、把集合中的数据存到文本文件.png)

### 4、把文本文件的数据存到集合

![169、把集合中的数据存到文本文件](F:\01、java基础\笔记的截图图片\169、把集合中的数据存到文本文件.png)

### 5、随机获取文本中的姓名

![169、把集合中的数据存到文本文件](F:\01、java基础\笔记的截图图片\169、随机获取文本中的姓名.png)

### 6、复制单级文件夹

![169、复制单级文件夹](F:\01、java基础\笔记的截图图片\169、复制单级文件夹.png)

### 7、复制指定目录下指定文件并修改文件名称

![169、复制指定目录下指定文件并修改文件名称](F:\01、java基础\笔记的截图图片\169、复制指定目录下指定文件并修改文件名称.bmp)

### 8、复制多级文件夹

![169、复制多级文件夹](F:\01、java基础\笔记的截图图片\169、复制多级文件夹.bmp)

### 9、把一个文件中的字符串排序后在写入里那个一个文件

![169、把一个文件中的字符串排序后在写入里那个一个文件](F:\01、java基础\笔记的截图图片\169、把一个文件中的字符串排序后在写入里那个一个文件.png)

## 8、面试题

### 1、close和flush的区别

```
close()关闭流对象，但是先刷新一次缓冲区，关闭之后流对象不可以继续使用
flush()刷新换乘功能区，流对象可以继续使用
如果数据没有那么大得时候就使用close()，数据大得时候就是用flush()
```



# 九、多线程



# 十、网络编程

# 十一、反射









































