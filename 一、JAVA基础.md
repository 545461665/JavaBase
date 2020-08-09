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

> 类：是一组相关的属性和行为的集合
>
> 对象：是该类事物的具体体现
>
> ```
> 类：学生类
> 对象：班长就是一个对象
> ```
>
> 0



### 2.2.2、作用

## 2.3、对象的内存图

## 2.4、成员变量和局部变量的区别

## 2.5、匿名对象

## 2.6、封装

## 2.7、this关键字

## 2.8、构造方法

## 2.9、static关键字