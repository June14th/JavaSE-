# 注释
//为单行注释
/*  */为多行注释
/**    */为文档注释
#关键字
关键字的字母全部*小写*，关键字会*变色*
#常量
字符串常量(双引号，可直接输出)，
整数常量(可直接输出)，
小数常量(可直接输出)，
字符常量(单引号，可直接输出)，
布尔常量(true，false，是关键字，可直接输出)，
空常量(null，是关键字，不可直接输出)
#数据类型
整数:byte short int long 
浮点数:float double 
字符:char 
布尔:boolean
#变量
- 数据类型 变量名 = 变量值
- 整数都默认为int类型，若想创建long类型的变量即使创建时指定数据类型，除非在后面加L，ex: long a = 1234567890L;
- 浮点数默认都是double，防止不兼容的类型，要在数字后面加F指定为float类型。
#标识符
常见约定:
- 小驼峰(针对方法，变量):一个单词，小写；两个单词，第一个首字母小写其余大写。
- 大驼峰(针对类):一个单词，首字母大写；两个单词，首字母大写。
#类型转换
- 自动类型转换:范围小的转换为范围大的
- 强制类型转换:范围大的转换为范围小的(需要明文说明，会有数据丢失)
#算术运算符
- + - * / %
除法得到的是商，取余得到余数
整数相除只能得到整数，想得到小数，必须有浮点数的参与
#字符的+操作
字符‘A’的值是65，‘a’是97，‘0’是48
算术表达式中包含多个数据类型时，整个类型会得到自动提升
#字符串的+操作
当+操作两边有字符串时，其作用为字符串拼接
从左到右的顺序 ex: 1+99+“years” 其输出为 100years
#赋值运算符
= 赋值    += -= *= /= %=  为扩展赋值运算符
注意，扩展的赋值运算符底层隐含了强制类型转换
#自增自减运算符
++ --
参与操作时:
放在后面，则先拿变量参与操作，再做++/--；
放在前面，则先做++/--，再拿变量做操作。
#关系运算符
== != > >= < <=
结果一定为true或false
#逻辑运算符
&与 两个都真才真
|或 有一真则真 
^异或 两个不同为真 
!非 取反
#短路逻辑运算符
&&  左边为false，右边不执行
||  左边为true，右边不执行
#三元运算符
a>b?a:b;
#数据输入
Scanner
导包:import java.util.Scanner;
创建对象:Scanner sc = new Scanner(System.in);
接收数据:int i = sc.nextInt();
#流程控制
顺序，分支(if，switch)，循环(for，while，do...while)
#if语句
if...elseif...elseif...else...
测试正确数据，边界数据，错误数据
#switch语句
switch(表达式){
    case 值:
        语句体；
        break；
    ...
    default:
        语句体；
        break；
}
注意case穿透，直到遇到break才会停止。
#for循环
#while语句
#do...while语句
do{}while();(至少执行一次)
#跳转控制语句
continue基于条件控制，跳过某次循环体的执行，继续下一次的执行
break基于条件控制，终止整个循环
#循环嵌套
#Random
产生一个随机数
- 导包:import java.util.Random;
- 创建对象:Random r = new Random():
- 获取随机数:int number = r.nextInt(10);//获取[0，10)，不包括10
#IDEA中的项目结构
1. 创建一个空项目(project)
2. 创建一个新模块(module)
3. 在模块下的src下创建一个包(packet)
4. 在包下创建一个类(Class)
5. 在类中编写代码(code)
#IDEA中的内容辅助键
- 快速生成语句
快速生成main()方法:psvm，回车
快速生成输出语句: sout，回车
- 内容辅助键
Crtl+Alt+space(内容提示，代码补全)
#IDEA中的快捷键
- 注释: 单行:选中代码，Ctrl+/，再来一次取消
        多行，选中代码，Ctrl+Shift+/，再来一次取消
- 格式化: Ctrl+Alt+L
#数组
array 多个类型相同的变量
int [] arr
#数组动态初始化
动态初始化: int[] arr = new int[3];
初始化时会给出默认值
#内存分配
栈内存:局部变量
堆内存:new出来的内容
#多个数组指向相同
int[] arr2 = arr;
#数组静态初始化
int[] arr = {1,2,3};
#数组常见问题
索引越界，空指针异常(null)
#数组常见操作
遍历: 循环
获取元素数量: arr.length
#方法(method)
注意事项:方法不能嵌套定义
方法参数传递(基本类型):形参的改变不会影响实参值
方法参数传递(引用类型):传入地址，会影响实参的值
#Debug
断点调试
#导包
- 手动导包
- 快捷键导包 Alt + Enter
- 自动导包
#类和对象
类由属性(成员变量)和行为(成员方法)构成
构建对象: 类名 对象名 = new 类名();
#多个对象指向相同
Student s2 = s1;
传递地址，共用空间
#成员变量(类中的变量，在堆内存，有默认值)
#局部变量(类的方法中的变量，在栈内存，没有默认值)
#private
private修饰的成员只能在本类中才能访问
通常要提供getxx()，setxx方法和show()方法
public是公用的，类内外均可访问
#this关键字
用this修饰指定为成员变量(解决局部变量隐藏成员变量)
#this内存原理
#封装
面向对象三大特征:封装，继承，多态
#构造方法
用来创建对象的特殊的方法，主要完成对象数据的初始化
修饰符<一般是public> 类名(参数){}
建议都手动给出无参构造方法
#API
应用程序编程接口
#Crtl+Alt+V
对象调用方法返回变量时的快捷键，自动给出返回的变量
#String
在java.lang下，故不需要导包
字符串不可变，但可以被共享
字符串效果上相当于字符数组char[]，底层时字节数组byte[]
#String构造方法
- String s = new String() 空字符串
- String(char[] chs)
- String(byte[] bys) 使用字节数组构造字符串
- String s = "abc"
#String对象特点
用new出来的会单独创建对象
用“”给出的字符串，只要字符串相同，则只会建立一个String对象放于堆内存的常量池中，String s1 = "abc";String s2 = "abc";此处s1和s2的地址相同。
#比较
==
基本类型:比较的是数据值是否相同
引用类型:比较的是地址值是否相同
#字符串的比较
直接 == 比较的是地址
s1.equals(s2)用于比较内容是否相同
public boolean equals(Object anObject)
#charAt方法
public char charAt(int index)返回索引处的char值
#length()方法
public int length()获取字符串的长度
#StringBuilder
String进行拼接的时候，是在常量池中额外创建一个新的字符串，然后将该字符串的地址传递给原字符串
String内容是不可变的，StringBuilder内容是可变的
#StringBuilder构造方法
public StringBuilder()
public StringBuilder(String str)
#StringBuilder的添加和反转方法
public StringBuilder append(任意类型) 添加数据，并返回对象本身
链式编程:strb.append("hello").append("world").append("java");
public StringBuilder reverse() 返回相反的字符串系列
#String和StringBuilder相互转换
- StringBuilder转换为String
public String toString()
ex: String s = sb.toString();
- String转换为StringBuilder
public StringBuilder(String s)
ex: StringBuilder sb = new StringBuilder(s);
#集合基础
集合类提供一种大小可变的存储模型，容量可变
#ArrayList<E>
可调整大小的数组实现
<E>: 是一种特殊的数据类型，泛型
ex: ArrayList<String>,ArrayList<Student>;
#ArrayList构造方法和添加方法
public ArrayList() 创建一个空的集合对象[]
public boolean add(E e) 将指定的元素追加到此集合的末尾
public void add (int index, E element) 在此集合的指定位置插入指定元素
#ArrayList常用方法
public boolean remove(Object o)删除指定元素，返回删除是否成功
public E remove(int index)删除指定索引出的元素并返回该元素
public E set(int index, E element)修改指定索引处的元素，并返回被修改的元素
public E get(int index)返回指定索引处的元素
public int size()返回集合中的元素个数
#Alt+INSERT
在进行类的说明时，自动补全构造函数和get()set()等函数
#System.exit(0) JVM退出
#\t 相当于tab键
#return;相当于提示方法不再向下执行
#继承
子类继承父类的属性和方法，子类还可以有自己的属性和方法
public class 子类名 extends 父类名{}
#继承的好处和弊端
好处:提高了代码的复用性，维护性。
坏处:类与类产生了耦合，削弱了子类的独立性
#继承中变量的访问特点
在子类中访问一个变量:
- 子类局部范围找
- 子类成员范围找
- 父类成员范围找
- 如果没有就报错(不考虑父亲的父亲)
#super
与this相似，super表示父类存储空间的标识
this.成员变量   this(...)构造方法   this.成员方法
super.成员变量   super(...)构造方法   super.成员方法
#继承中构造方法的访问特点
子类所有构造方法默认都会访问父类中无参的构造方法
(每一个子类构造方法的第一条语句默认都是:super())
#继承中成员变量的访问特点
通过子类对象访问一个方法
- 子类成员范围找
- 父类成员范围找
- 如果没有就报错(不考虑父亲的父亲)
#super内存图
...
#方法重写
子类中出现了和父类中一模一样的方法声明
沿袭父类的方法，同时具有自己的功能
#@Override
是一个注解，可以帮助我们检查重写方法的方法声明的正确性
#方法重写的注意事项
- 父类中的私有方法子类不能重写
- 子类访问权限不能更低(piblic>默认>私有)
#Java中集成的注意事项
- java中类只支持单继承，不支持多继承
- java中类支持多层继承
#package
- **包就是文件夹，方便对类进行分类管理**
- **包的定义格式:**
package 包名;(多级包用.分开)
ex: package com.it;
- **带包的java类编译和执行:**
手动建包:
* 先编译:javac HelloWorld.java
* 手动创建包: 在当前目录下建立文件夹com，之后在com文件夹下建立it文件夹
* 把class文件放入包的最里面
* 带包执行 java com.it.HelloWorld
自动建包 
* 编译:javac -d . HelloWorld.java 
* 运行:java com.it.HelloWorld
#导包
import 包名;(同一模块下)
#权限修饰符
|  修饰符   | 同一个类中  | 同一个包中子类/无关类 | 不同包中的子类 | 不同包中的无关类 |
|  ---- | ----  | ---- |  ----  | ----  |
| private | √ |  |  |  |
| 默认  | √ | √ |  |  |
| protected  | √ | √ | √ |  |
| public  | √ | √ | √ | √ |
#状态修饰符
##final 
最终，可以修饰成员方法，成员变量，类
- 修饰方法:表明该方法是最终方法，不能被重写
- 修饰变量:表明该变量是常量，不能再次被赋值
- 修饰类:表明该类是最终类，不能被继承
###final修饰局部变量
- 修饰基本类型:数据值不能发生改变
- 修饰引用类型:引用类型的地址值不能发生改变，但地址内的内容是可以改变的
##static
静态，可以修饰成员方法，成员变量
- 被类的所有对象共享(这也是判断是否使用静态关键字的条件)
- 可以通过类名调用，也可以通过对象名调用(推荐用类名调用)
###static访问特点
静态成员方法只能访问静态成员(方法和变量)
#多态
同一对象，在不同时刻表现出来的不同形态
##多态的前提和体现
- 有继承/实现关系
- 有方法重写
- 有父类引用指向子类对象
#多态中成员的访问特点
- 成员变量:编译看左边，执行看左边
- 成员方法:编译看左边，执行看右边
为什么成员变量和成员方法的访问不一样呢？
因为成员方法有重写，而成员变量没有
#多态的好处和弊端
- 好处:定义方法的时候，使用父类型作为参数，将来使用的时候，使用具体的子类型参与操作
- 坏处:不能使用子类的特有功能
#多态的转型
- 向上转型:从子到父，父类引用指向子类对象
- 向下转型:从父到子，父类引用转为子类对象
#抽象类
在java中，一个没有方法体的方法应该定义为抽象方法，而类中如果有抽象方法，该类必须定义为抽象类。
#抽象类的特点
- 抽象类和抽象方法要用abstract标识
- 抽象类中不一定有抽象方法，但有抽象方法的一定是抽象类
- 抽象类不能实例化，只能参照多态的方法，由子类对象实例化，这叫抽象类多态
- 抽象类的子类:要么重写抽象类中的所有抽象方法，要么是抽象类
#抽象类的成员特点
- 成员变量:
可以是变量，也可以是常量
- 构造方法:
有构造方法，但是不能实例化
构造方法的作用是用于子类访问父类数据的初始化
- 成员方法:
可以有抽象方法:限定子类必须完成某些动作
也可以有非抽象方法:提高代码的复用性
#接口
接口就是一种公共的规范标准，java接口更多体现在对行为的抽象
#接口的特点
- 接口用interface修饰
public interface 接口名{}
- 类实现接口用implements表示
public class 类名 implements 接口名{}
- 接口不能实例化
参照多态的方式，通过实现类对象实例化，这叫接口多态
多态的形式:具体类多态，抽象类多态，接口多态
多态的前提:有继承或者实现关系；有方法重写；有父(类/接口)引用指向(子/实现)类对象
- 接口的实现类
要么重写接口中的所有抽象方法，要么是抽象类
#接口的成员特点
- 成员变量
只能是常量，默认修饰符:public static final
- 构造方法
接口没有构造方法，因为接口主要是对行为进行抽象的，是没有具体存在
**一个类如果没有父类，默认继承自Object类**
- 成员方法
只能是抽象方法，默认修饰符public static
#类和接口的关系
- 类和类的关系
继承关系，只能单继承，但是可以多层继承
- 类和接口的关系
实现关系，可以单实现，也可以多实现，还可以在继承一个类的同时实现多个接口
- 接口和接口的关系
继承关系，可以单继承，也可以多继承
#抽象类和接口的设计区别
抽象类是对事物的抽象，而接口是对行为的抽象
#分析、实现和使用
分析:从具体到抽象
实现:从抽象到具体
使用:使用的是具体类的对象
#抽象类名作为形参和返回值
- 方法的形参是抽象类名，其实需要的是该抽象类的子类对象
- 方法的返回值是抽象类名，其实返回的是该抽象类的子类对象
#接口名作为形参和返回值
- 方法的形参是接口名，其实需要的是该接口的实现对象
- 方法的返回值是接口名，其实返回的是该接口的实现对象
#内部类
在一个类中定义另一个类
public class 类名{
    修饰符 class 类名{
    }
}
内部类的访问特点:
- 内部类可以直接访问外部类的成员，包括私有
- 外部类要访问内部类的成员，必须创建对象
#成员内部类
内部类在类的成员位置
成员的内部类，外界如何创建对象使用呢？
外部类名.内部类名 对象名 = 外部类对象.内部类对象
ex: Outer.Inner oi = new Outer().new Inner();
但一般内部类定义为私有的，不让外界直接访问到
#局部内部类
内部类在成员方法的内部，外界无法直接使用，需要在方法内部创建对象并使用
该类可以直接访问外部类的成员，也可以访问方法内的局部变量
#匿名内部类
前提:存在一个类或者接口(类可以是具体类或者抽象类)
格式:
new 类名或者接口名(){
    重写方法;
};
本质:是一个继承了该类或者实现了该接口的子类匿名对象
#匿名内部类在开发中的使用
根据匿名内部类的本质是一个对象，可以省去构造多态的过程
#常用API
##Math类
private无参构造
抽象成员方法:
abs()绝对值
ceil()向上取整，返回double
floor()向下取整，返回double
round()四舍五入，返回int
max()最大
min()最小
pow(a，b) a的b次幂
random() [0.0，1.0)随机数
##System类
private无参构造
抽象成员方法:
exit(0)正常退出
currentTimeMills()返回当前时间(以毫秒为单位，自1970.01.01)(常用于计算程序的运行时间)
##Object类
Object是类层次结构的根，每个类都可以将Object类作为超类，所有类都直接或者间接的继承自该类
构造方法:public Object()
**看方法的源码，选中方法，按下Ctrl+B**
###Object的toString()方法
建议所有子类重写toString()方法，可自动重写
###Object的equals()方法
对象的默认equals()方法是比较地址值，建议重写为比较内容。
可自动重写(先比较地址，之后比较两个对象是否来自同一个类，之后在依次比较内容是否相同，亦可自己规定)
##Arrays类
###冒泡排序
将相邻数据两两比较，将较大的数据放到后面，直至完成排序
如有n个数据，则需要比较n-1次，每一次比较完毕，下一次的比较都会少一个数据参与
for (int j = 0; j < arr.length - 1; j++) {
  for (int i = 0; i < arr.length - 1 - j; i++) {
       if (arr[i] > arr[i + 1]) {
            int temp = arr[i];
            arr[i] = arr[i + 1];
            arr[i + 1] = temp;
        }
    }
 }
###Arrays类包含用于操作数组的各种方法
private无参构造
都为static，只能指定类名进行访问，不能实例化
public static String toString(int[]a)   返回指定数组的内容的字符串表示形式
public static void sort(int[]a) 按照数字顺序排列指定的数组
#工具类的设计思想:
- 构造方法用private修饰
- 成员用public static修饰
#基本类型包装类
int能取到的最值:
- Integer.MIN_VALUE
- Integer.MAX_VALUE
其他的基本类型包装类对应关系

| 基本数据类型 | 包装类 |
| ---- | ---- |
| byte | Byte |
| short | Short |
| int | Integer |
| long | Long |
| float | Float |
| double | Double |
| char | Character |
| boolean | Boolean |
#Integer类
包装一个对象中的原始类型int的值
public Integer (int value) 根据int值创建Integer对象(已过时，但还可用)
public Integer (String s) 根据String值创建Integer对象(已过时，但还可用)
public static Integer valueOf(int i) 返回表示指定的int值的Integer实例
public static Integer valueOf(String s) 返回一个保存指定值的Integer对象String
#int和String的相互转换
- int转为String
public static String valueOf(int i)
返回int参数的字符串形式，该方法是String类中的方法
- String转为int
public static int parseInt(String s)
将字符串解析为int类型，该方法是Integer类中的方法
#public String[] split (String regex)
将此字符串拆分为给定的regular expression匹配
regex为分割正则表达式
#自动装箱和拆箱
- 装箱:把基本数据类型转换为对应的包装类类型
- 拆箱:把包装类类型转换为对应的基本数据类型
装箱example:
Integer i = Integer.valueOf(100);   //装箱
Integer i = 100;    //自动装箱
拆箱example:
i = i.intValue() + 200; //先拆箱再自动装箱
i += 200;   //自动拆箱并自动装箱
**引用类型使用之前最好判断其是否为空null**
#日期类
##Date类(util包下的)
构造方法:
public Date():分配一个Date对象，精确到毫秒
public Date(long date):分配一个Date对象，将其初始化为从标准基准时间起指定的毫秒数
常用方法:
public long getTime():获取从1970.01.01.00:00到现在的毫秒数
public void setTime(long time):设置时间，给的是毫秒数
##SimpleDateFormat类
日期格式化和解析
y年M月d日
H时m分s秒
- 构造方法:
无参:public SimpleDateFormat()
带参:public SimpleDateFormat(String pattern)使用给定的模式
- 格式化(从Date到String)
public final String format(Date date)
- 解析(从String到Date)
public Date parse(String source)
#Calendar类
为某一时刻和一组日历字段之间的转换提供了一些方法，并为操作日历字段提供了一些方法
Calendar类提供了一个类方法getInstance用于获取Calendar对象，其日历字段已使用当前日期和时间初始化:
Calendar c = Calendar.getInstance()；
#Calendar的常用方法
public int get(int field)
ex: int year = c.get(Calendar.YEAR)//获取指定字段
public abstract void add(int field, int amount)
根据日历的规则，将指定的时间量加上或减去给定的日历字段
public final void set(int year，int mouth，int date)设置当前日历的年月日
#异常
程序出现了不正常的情况
异常体系:
Throwable分为Error和Exception
Exception分为RuntimeException和非RuntimeException
Error:严重问题，不需要处理
Exception:异常类，表示程序可以处理的问题
RuntimeException:在编译期不检查，出现问题后，需要修改代码
非RuntimeException:编译期就必须处理，否则程序不能通过编译
#JVM的默认处理方案
- 把异常的名称，异常原因和异常出现的位置等信息输出在控制台
- 程序停止运行
#异常处理
##try...catch...
##throws
throws 异常类名；
注意:这个格式时跟在方法的括号后面的
#Throwable的成员方法
public String getMessage()返回此throwable的详细消息字符串
public String toString()返回此可抛出的简短描述
public void printStackTrace()把异常的错误消息输出在控制台
#编译时异常(受检异常)
有可能有问题，但是必须进行处理，否则无法通过编译
两种处理方案，如采用throws，将来谁调用谁处理
#运行时异常(非受检异常)RuntimeException类及其子类
可以不处理，出现问题后，需要回来修改代码
#自定义异常
格式:
public class 异常类名 extends Exception{
    无参构造
    带参构造
}
#throws和throw的区别
throws
- 用在方法声明后面，跟的是异常类名
- 表示抛出异常，由该方法的调用者来处理
- 表示出现异常的一种可能性，并不会一定出现异常
throw
- 用在方法体内，跟的是异常对象名
- 表示抛出异常，由方法体内的语句处理
- 执行throw一定抛出了某种异常
#集合类的体系结构
集合可分为Collection(单列)与Map(双列)
Collection又分为List(可重复)与Set(不可重复)
以上均为接口
List的具体实现类有ArrayList，LinkedList...
Set的具体实现类有HashSet,treeSet...
Map的具体实现类有HashMap...
#Collection
- 是单列集合的顶层接口，表示一组对象，这些对象也被称为是collection的元素
- 不提供该接口的直接实现，提供更具体的子接口(Set，List)实现
#创建Collection集合的对象
- 多态的方式
- 用具体的实现类，如ArrayList...
#Collection常用方法

| 方法名 | 说明 |
| --- | --- |
| boolean add(E e) | 添加元素 |
| boolean remove(Object o) | 从集合中移除指定的元素 |
| void clear() | 清空集合中的元素 |
| boolean contains(Object o) | 判断集合中是否存在指定的元素 |
| boolean isEmpty() | 判断集合是否为空 |
| int size() | 集合中的元素个数 |
#集合的迭代Iterator迭代器，集合专用的遍历方式
Iterator <E> iterator()；返回该集合中元素的迭代器，通过集合的iterator()方法得到，依赖于集合存在的
ex: Iterator<E> it = c.iterator();
#Iterator中常用方法
E next():返回迭代的下一个元素
boolean hasNext():如果迭代具有更多元素，返回true
#List集合
- 有序集合(序列)，用户可以精确控制列表中每个元素的插入位置，可以通过索引访问元素，并搜索列表中的元素
- 与Set不同，列表允许重复的元素
#List集合特点
- 有序:存储和取初的元素顺序一致
- 可重复:存储的元素可以重复
#List集合特有方法

|方法名|说明|
|---|---|
|void add(int index,E element)|在集合的指定位置插入元素|
|E remove(int index)|删除指定索引元素，返回被删除元素|
|E set(int index,E element)|修改指定索引的元素，返回被修改的元素|
|E get(int index)|返回索引处的元素|
#并发修改异常
ConcurrentModificationException
产生原因:
迭代器遍历的过程中，通过集合对象修改了集合中元素的长度，造成了迭代器获取元素中判断预期修改值和实际修改值不一致
解决方案:
用for循环遍历，然后用集合对象做相应的操作即可
#ListIterator列表迭代器
- 通过List集合的listIterator()方法得到，是List集合特有的迭代器
- 用于允许程序员眼任一方向遍历列表的列表迭代器，在迭代期间修改列表，并获取列表中迭代器的当前位置
#ListIterator的常用方法
- E next()
- boolean hasnext()
- E previous()
- boolean hasPrevious() 
- void add(E e) 将指定的元素插入列表(不会产生并发修改异常，因为它在内部将预期修改值=实际修改值)
#增强for循环
简化数组和Collection集合的遍历
- 实现Iterable接口的类允许其对象成为增强型for语句的目标
- 内部原理是一个Iterator迭代器
格式:
for(元素数据类型 变量名:数组或这Collection集合){
    //在此处使用变量即可，该变量就是元素
}
#数据结构
计算机存储、组织数据的方式
#栈(Stack)
FILO先进后出
#队列(Queue)
FIFO先进先出
#数组(Array)
查询效率高，删除效率低，添加效率低
#链表(linklist)
查询慢，增删快
#List子类的特点
两个子类:ArrayList(底层是数组)LinkedList(底层是链表)
#LinkedList集合的特有功能

|方法名|说明|
|---|---|
|public void addFirst(E e)|将指定元素插入链表头|
|public void addLast(E e)|将指定元素追加到链表尾|
|public E getFirst()|返回第一个元素|
|public E getLast()|返回最后元素|
|public E removeFirst()|删除并返回第一个元素|
|public E removeLast()|删除并返回最后一个元素|
#Set集合(接口)
- 不包含重复元素的集合
- 没有带索引的方法
具体实现类:HashSet:对集合的迭代顺序不做保证
#哈希值
- 是JDK根据对象的地址或者字符串或者数字算出来的int类型的数值
- Object类中有一个方法可以获取对象的哈希值:public int hashCode()
对象的哈希值特点
- 同一个对象的hashCode()方法返回的哈希值是相同的
- 默认情况下，不同对象的哈希值是不同的(可通过重写，使不同对象的哈希值相同)
#HashSet集合概述和特点(Set的具体实现类)
- 底层数据结构是哈希表
- 对集合的迭代顺序不做任何保证，不保证存储和取出的元素顺序一致
- 没有带索引的方法，不能用普通的for循环遍历，可用增强for循环
- 由于是Set集合，所以不包含重复元素
#HashSet集合如何保证元素的唯一性
根据对象的哈希值计算对象的存储位置，如果该位置没有元素，就存储该元素
    存入的元素和以前的元素比较哈希值
        如果哈希值不同，会继续向下执行，把元素添加到集合
        如果哈希值相同，调用对象的equals()方法比较
            如返回false，向下执行，把元素添加到集合
            如返回true，说明元素重复，不存储
#哈希表
- 底层用数组+链表实现，可以说是一个元素为链表的数组，在长度比较长的时候底层实现了优化。
- 默认长度为16，元素的哈希值%16得到元素对象的存储位置，位置相同的，再继续比较对象是否equals()，如不同，以链表的形式将元素添加到该存储位置的后面。
#重写hashCode()和equals() (可自动生成)
在用自己生成的类时，使用哈希表时需重写hashCode()和equals()否则可能加入重复元素
#LinkedHashSet集合概述和特点
- 哈希表和链表实现的Set接口，具有可预测的迭代次序
- 由链表保证元素有序，元素存储和取出的顺序一致
- 由哈希表保证元素唯一，没有重复的元素
#TreeSet集合
- 元素有序，这里的顺序不是指存储和取出的顺序，而是按照一定的规则进行排序，具体排序方法取决于构造方法
TreeSet():根据元素的自然排序进行排序
TreeSet(Comparator comparator):根据指定的比较器进行排序
- 没有带索引的方法，不能用普通for循环遍历，但可以使用增强型的for循环和迭代器
- 是Set集合，所以不包含重复的元素
#自然排序Comparable的使用
- 用TreeSet集合存储自定义对象，无参构造方法使用的是自然排序对元素进行排序的
- 自然排序，就是让元素所属的类实现Comparable接口，重写compareTo(To)方法
- 重写方法时，一定要注意排序规则必须按照要求的主条件和次要条件来写
#比较器Comparator的使用
- 用TreeSet集合存储自定义对象，带参构造方法使用的是比较器排序对元素进行排序的
- 比较器排序，就是让集合构造方法接受Comparator的实现类对象，重写compara(T o1,T o2)方法
- 重写方法时，一定要注意排序规则必须按照要求的主要条件和次要条件来写
#泛型
- 本质是参数化类型，就是将所操作的数据类型指定为一个参数
- 参数化类型就是将类型原来的具体的类型参数化，然后在使用/调用时传入具体的类型
- 可以用在类，方法，接口中
#泛型定义格式
- <类型>:指定一种类型的格式，可以看成是形参
- <类型1，类型2，...>:指定多种类型的格式，这里的类型可以看成是形参
- 将来具体调用时候给定的类型可以看成是实参，并且实参的类型只能是引用类型
#泛型的好处
- 把运行时间的问题提前到了编译期间
- 避免了强制类型转换
#泛型类
格式:public class 类名<T>{}
此处的T为任意标识，常见的T,E,K,V等常用于表示泛型
#泛型方法
格式:修饰符 <类型> 返回值类型 方法名(类型 变量名){}
ex: public <T> void show(T t){}
#泛型接口
格式:修饰符 interface 接口名<类型>{}
ex: public interface Genetic<T>{}
#类型通配符
为了表示各种泛型List的父类，可以使用类型通配符
- 类型通配符:<？>
- List<？>:表示元素类型位置的List，它的元素可以匹配任何的类型
- 这种带通配符的List仅表示它是各种泛型List的父类，并不能把元素添加到其中
##如果不希望List<？>是任何泛型的父类，只希望它代表某一类泛型List的父类，可以使用通配符的上限
- < ？extend 类型>
- List< ?extends Number>:表示的类型是Number或者其子类型
##指定类型通配符的下限
- < ？super 类型>
- List< ?super Number>:表示的类型是Number或者其父类型
#可变参数
可变参数又称参数个数可变，用作方法的形参出现，那么方法参数个数就是可变的了
- 格式: 修饰符 返回值类型 方法名(数据类型...变量名){}
- ex: 
public static int sum(int... a){    //a在这里其实是个数组
    int sum = 0;
    for(int i=0:a){
        sum += a;
    }
}
可变参数的注意事项:
- 这里的可变参数其实是一个数组
- 如果一个方法有多个参数，包含可变参数，可变参数要放在最后
#可变参数的使用
Array工具类中有一个静态方法:
- public static <T> List<T> asList(T...a):返回由数组支持的固定大小的列表
- 不可以增加和删除，但可以修改
List接口中有一个静态方法:
- public static <E> List<E> of(E...elements):返回包含任意数量元素的不可变列表
- 不可增删改
Set接口中有一个静态方法:
- public static<E> Set<E> of(E...elements):返回一个包含任意元素的不可变集合
- 在给元素的时候，不可以给重复的元素
- 返回的集合不能做增删操作，没有修改的方法
#Map集合
- Interface Map<K,V> K键的类型 V值的类型
- 将键映射到值的对象；不能包含重复的键；每个键可以映射到最多一个值
- 创建Map对象用多态的方式，具体实现类HashMap
#Map集合的基本功能

|方法名|说明|
|---|---|
|V put(K key,V value)|添加元素|
|V remove(Object key)|根据键值删除键值对元素|
|void clear()|移除所有的键值对元素|
|boolean containskey(Object key)|判断集合是否包含指定的键|
|boolean containValue(Object value)|判断集合是否包含某值|
|boolean isEmpty()|判断集合是否为空|
|int size()|集合的长度，键值对的个数|
注意:键相同时，后一个put的对象会覆盖前一个
#Map集合的获取功能

|方法名|说明|
|---|---|
|V get(Object key)|根据键获取值|
|Set<K> keySet()|获取所有键的集合|
|Collection<V>values()|获取所有值的在集合|
|Set<Map.Entry<K,V>>entrySet()|获取所有键值对对象的集合|
#Map集合的遍历
ex1:
for(String i:map.keySet()){
       System.out.println(i + ", " +map.get(i));
        }
ex2:
Set<Map.Entry<String, String>> entries = map.entrySet();
for(Map.Entry<String, String> me : entries){
    System.out.println(me.getKey()+", "+me.getValue());
        }
#Collections类(工具类)
针对集合操作的工具类
常用方法:
- public static <T extends Compareable<?super T>> void sort(List<T> list):将指定的列表按升序排序
- public static void reverse(List<?> list):反转指定列表中元素的顺序
- public static void shuffle(List<?> list):使用默认的随机源随机排列指定的列表
#File类
它是文件和目录路径名的抽象表示
- 文件和目录是可以通过File封装成对象的
- 对于File而言，其封装的并不是一个真正存在的文件，仅仅是一个路径而已。它可以是存在的也可以是不存在的。将来是要通过具体的操作把这个路径的内容转换为具体存在的。

|方法名|说明|
|---|---|
|File(String pathname)|通过将给定的路径名字符串转换为抽象路径名来创建新的File实例|
|File(String parent,String child)|从父路径名字符串和子路径名字符串创建新的File实例|
|File(File parent,String child)|从父抽象路径名和子路径名字符串创建新的File实例|
#File类创建功能

|方法名|说明|
|---|---|
|public boolean createNewFile()|当具有该名称的文件不存在时，创建一个由该抽象路径名命名的新空文件|
|public boolean mkdir()|创建由此抽象路径名命名的目录(创建单级目录)|
|public boolean mkdirs()|创建由此抽象路径名命名的目录，包括任何需要但不存在的父目录(即创建多级目录)|
如文件或目录不存在，则创建，并返回true；如已经存在，则返回false
#File类判断和获取功能

|方法名|说明|
|---|---|
|public boolean isDirectory()|测试此抽象路径名表示的File是否为目录|
|public boolean isFile()|测试此抽象路径名表示的File是否为文件|
|public boolean exists()|测试此抽象路径名表示的File是否存在|
|public String getAbsolutePath()|返回此抽象路径名的绝对路径名字符串|
|public String getPath()|将此抽象路径名转换为路径名字字符串|
|public String getName()|返回由此抽象路径名表示的文件或目录名称|
|public String[] list|返回此抽象路径名表示的目录中的文件和目录的名称字符串数组|
|public File[]listFiles()|返回此抽象路径名表示的目录中的文件和目录的File对象数组|
#File类删除功能
public boolean delete() 删除由此抽象路径名表示的文件或目录
绝对路径和相对路径的区别
- 绝对路径:完整的路径名，不需要任何其他信息就可以定位文件，ex: C:java/bin/java.exe
- 相对路径:必须使用取自其他路径名的信息进行解释，ex: mymodule\\java.txt
删除目录的注意事项:
- 如果一个目录中有内容(目录或文件)，不能直接删除，应先删除目录中的内容，最后才能删除目录。
#递归
递归概述:从编程的角度来看，递归指的是方法定义中调用方法本身的现象
**递归出口+递归规则**
#字节流
##I/O流  输入/输出
流:一种抽象概念，对数据传输的总称。
I/O流分类:
按数据流向:输入流-读数据，输出流-写数据
按数据类型:字节输入/输出流，字符输入/输出流
这两种流在什么情况下使用呢？
如打开后可以读懂里面的内容，用字符流，否则用字节流，如不知道用哪种类型的流，就用字节流。
#字节流写数据
字节流抽象基类:
- InputStream:该抽象类是表示字节输入流的所有类的超累类
- OutputStream:该抽象类是表示字节输出流的所有类的超累类
- 子类名特点:子类名称都是以其父类名作为子类名的后缀
FileOutputStream:文件输出流用于将数据写入File
- FileOutputStream(String name):创建文件输出流以指定的名称写入文件
#使用字节输出流对象写数据的步骤:
- 创建字节输出流对象(调用系统功能创建文件，创建字节输出流对象，让字节输出流对象指向文件)
- 调用字节输出流对象的写数据方法
- 释放资源(关闭此文件输出流并释放于此流相关联的任何系统资源)
#字节流写数据的3种方式
|方法名|说明|
|---|---|
|void write(int b)|将指定的字节写入此文件输出流，依次写一个字节数据|
|void write(byte[]b)|将b.length字节从指定的字节数组写入此文件输出流一次写一个字节数组数据|
|void write(byte[]b,int off,int len)|将len字节从指定的字节数组开始，从偏移量off开始写入此文件输出流一次写一个字节数组的部分数据|
#byte[] getBytes():返回字符串对应的字节数组
#字节流写数据的两个问题
如何实现换行？
windows:\r\n
linux:\n
mac:\r
如何实现追加写入？
public FileOutputStream(String name,boolean append)如果第二个参数为true，则字节将写入文件的末尾而不是开头
#字节流写数据加异常处理
finally:在异常处理时提供finally块来执行所有的清除操作，如I/O流释放资源
特点:被finally控制的语句一定会执行，除非JVM退出
try{}catch(){}finally{}
#字节流读数据
FileInputStream:从文件系统中的文件获取输入字节
- FileInputStream(String name):通过打开与实际文件的连接来创建一个FileInputStream，该文件由文件系统中的路径名name命名
使用字节输入流读数据的步骤:
- 创建字节输入流对象
- 调用字节输入流对象的读数据方法
- 释放资源
注:文件的结尾为-1
```
int by;
while((by = fis.read()) != -1){
    System.out.print((char) by);
}
```
一次读一个字符数组的数据:
```
byte[] bys = new byte[1024];    //通常为1024的整数倍
int len;
while((len = fis.read(bys)) != -1){
     System.out.print(new String(bys,0,len));
        }
```
#字节缓冲流
- BufferOutputStream:该类实现缓冲输出流，通过设置这样的输出流，应用程序可以向底层输出流写入字节，而不必为写入的每个字节导致系统的调用。
- BufferInputStream:创建BufferInputStream将创建一个内部缓冲区数组，当从流中读取或跳过字节时，内部缓冲区将根据需要从所包含的输入流中重新填充，一次很多字节。
构造方法:
- BufferOutputStream(OutputStream out)
- BufferInputStream(InputStream in)
因为字节缓冲流仅仅提供缓冲区，而真正的读写数据还得靠基本的字节流对象进行操作
#汉字存储
- GBK编码:占用2个字节
- UTF-8编码:占用3个字节
#字符流
由于字节流操作中文不是特别方便，故Java提供字符流
- 字符流 = 字节流 + 编码表
用字节流复制文本文件时，文本文件中也有中文，但却没有问题，原因是最终的底层操作会自动进行字节拼接成中文，如何识别是中文？
- 汉字存储的时候，无论是选择哪一种编码存储，第一个字节都是负数
#编码表
ASCII，GBK，Unicode
采用何种类型编码，就要采用何种类型解码
#字符串中的编码解码问题
##编码:
- byte[] getBytes()使用默认的字符集编码为一系列的字节
- byte[] getBytes(String charsetName):使用指定的字符集编码为一系列的字节
##解码
- String(byte[] bytes)使用默认的字符集编码将字节构造为String
- String(byte[] bytes,String charsetname)使用指定的字符集编码将字节构造为String
#字符流中的编码解码问题
字符流抽象基类
- Reader:字符输入流的基类
- Writer:字符输出流的基类
字符流中和编码解码问题相关的两个类
- InputStreamReader
- OutputStreamWriter
#字符流写数据的方式
|方法名|说明|
|---|---|
|void write(int c)|写入一个字符|
|void write(char[] cbuf)|写入一个字符数组|
|void write(char[] cbuf,int off,int len)|写入字符数组的一部分|
|void write(String str)|写入一个字符串|
|void write(String str,int off,int len)|写入一个字符串的一部分|
注意:
void flush() 刷新流
void close() 关闭流，先刷新
#字符流读数据的两种方式
int read() 一次读一个字符数据
int read(char[] cbuf) 一次读一个字符数组数据
#读或写
- FileReader:用于读取字符文件的便捷类
FileReader(String fileName)
- FileWriter:用于写入字符文件的便捷类
FileWriter(String fileName)
#字符缓冲流
- BufferedReader(Reader in)
- BufferedWriter(Writer out)
字符缓冲流的特有功能:
BufferedWriter:
- void newLine()写一行行分隔符，行分隔符字符串由系统属性定义
BufferedReader:
- public String readLine():读一行文字。结果包含行的内容的字符串，不包含任何行终止符，如果流的结尾已经到达，则为null
#复制文件异常的处理方法
- 用try...catch...finally
- JDK7的改进方案
```
try(定义流对象){
    可能出现异常的代码
}catch(异常类名 变量名){
    异常的处理代码
}
自动释放资源
```
- JDK9的改进方案
```
定义输入流对象;定义输出流对象;
try(输入流对象;输出流对象){
    可能出现异常的代码
}catch(异常类名 变量名){
    异常的处理代码
}
自动释放资源
```
#特殊操作流
System类中有两个静态的成员变量:
- public static final InputStream in:标准输入流。通常该流对应于键盘输入或由主机环境或用户指定的另一个输入源
- public static final PrintStream out:标准输出流。永昌该流对应于显示输出或由主机环境或用户指定的另一个输出目标
自己实现键盘录入数据:
BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
写起来太麻烦了，Java提供了一个类实现键盘录入:
Scanner sc = new Scanner(System.in);
输出语句的本质:是一个标准的输出流
- PrintStream ps = System.out;
- PrintStream类有的方法，System.out都可以使用
#打印流
打印类分类:
- 字节打印流:PrintSteam
- 字符打印流:PrintWriter
打印流的特点:
- 只负责输出数据，不负责读取数据
- 有自己的特有方法
字节打印流:
- PrintStream(String fileName):使用指定的文件名创建新的打印流
字符打印流:
- PrintWriter(String fileName):使用指定的文件名创建新的字符打印流，不需要自动执行刷新
- PrintWriter(Write out,boolean autoflush):创建一个新的字符打印流，out:字符打印流，autoflush:一个布尔值，其为真时，则println，printf或format方法将刷新输出缓冲区
#对象序列化流
对象序列化:就是将对象保存到磁盘中，或者在网络种传输对象
这种机制就是使用一个字节序列表示一个对象，该字节序列包括:对象的类型，对象的数据和对象中存储的属性等信息
字节序列写到文件后，相当于文件中持久保存了一个对象的信息
反之，该字节序列还可以从文件中读取回来，重构对象，对它进行反序列化
要实现序列化和反序列化就要使用对象序列化流和对象反序列化流:
- 对象序列化流:ObjectOutputStream
- 对象反序列化流:ObjectInputStream
#对象序列化流ObjectOutputStream
- 将Java对象的原始数据类型和图形写入OutputStream。可以使用ObjectInputStream读取(重构)对象，可以通过使用流的文件来实现对象的持久存储。如果流时网络套接字流，则可以在另一个主机上或另一个进程中重构对象。
构造方法:
- ObjectOutputStream(OutputStream out):创建一个写入指定的OutputStream的ObjectOutputStream
序列化对象的方法:
- void writeObject(Object obj) : 将指定的对象写入ObjectOutputStream
注意:
- 一个对象要想被序列化，该对象所属的类必须实现Serializable接口
- Serializable接口是一个标记接口，实现该接口，不需要重写任何方法
#对象反序列化ObjectInputStream
- ObjectInputStream反序列化先前使用ObjectInputStream编写的原始数据和对象
构造方法:
- ObjectInputStream(InputStream in):创建从指定的InputStream读取的ObjectInputStream
反序列化对象的方法:
- Object readObject():从ObjectInputStream读取一个对象
#对象序列化流
Q:用对象序列化流序列化了一个对象后，加入我们修改了对象所述的类文件，读取数据会不会出问题呢？
A:会出问题，抛出InvalidClassException异常
Q:如果出问题了，如何解决呢？
A:给对象所属的类加一个serialVersionUID
private static final long serialVersionUID = 42L;
Q:如果一个对象中的某个成员变量的值不想被序列化，又该如何实现呢？
A:给该变量加transient关键字修饰，该关键字修饰的成员变量不参与序列化过程
#Properties
- 是一个Map体系的集合类
- Properties可以保存到流中或从流中加载
#Properties特有方法
|方法名|说明|
|---|---|
|Object setProperty(String key,String value)|设置集合的键和值，都是string类型，底层调用Hashtable方法的put|
|String getProperty(String key)|使用此属性列表中指定的键搜索属性|
|Set<String>stringPropertyNames()|从该属性列表中返回一个不可修改的键集，其中键及其对应的值时字符串|
#Properties与I/O有关的操作方法
|方法名|说明|
|---|---|
|void load(InputStream inStream)|从输入字节流读取属性列表(键和元素对)|
|void load(Reader reader)|从输入字符流读取属性列表(键和元素对)|
|void store(OutputStream out, String comments)|将此属性列表(键和元素对)写入此Properties表中。以适合使用load(InputStream)方法的格式写入输出字符流|
|void store(Writre,String comnmnets)|将此属性列表(键和元素对)写入此Properties表中。以适合使用load(Reader)方法的格式写入输出字符流|
#进程和线程
##进程
正在运行的程序
- 是系统进行资源分配和调用的独立单位
- 每一个进程都有自己的内存空间和系统资源
##线程
是进程中的单个顺序控制流，是一条执行路径
- 单线程:一个进程只有一条执行路径
- 多线程:一个进程有多条执行路径
#多线程的实现方式
##方式一:继承Thread类
- 定义一个类MyThread继承Thread类
- 在MyThread类中重写run()方法
- 创建MyThread类的对象
- 启动线程(用start())
Q:为什么重写run()？
A:因为run()是用来封装被线程执行的代码
Q:run()和start()有什么不同？
A:run():封装线程执行的代码，直接调用，相当于普通方法的调用
start():启动线程，然后由JVM调用此线程的run()方法
#设置和获取线程名称
Thread类中设置和获取线程名称的方法:
- void setName(String name):将此线程的名称更改等于参数name
- String getName():返回此线程的名称
- 通过构造方法也可以设置线程名称
- 获取当前正在执行的线程对象的引用: System.out.println(Thread.currentThread().getName());
#线程优先级
线程调度模型:分时调度，抢占式调度
Java使用的是抢占式调度模型
多线程程序的执行有随机性
Thread类中设置和获取线程优先级的方法:
- public final int getPriority():返回此线程的优先级
- public final void setPriority(int newPriority):更改此线程的优先级
线程的默认优先级是5；线程的优先级范围是1-10；
线程的优先级高仅表示该线程获取cpu时间片的几率高
#线程控制
|方法名|说明|
|---|---|
|static void sleep(long mills)|使当前正在执行的线程停留(暂定执行)指定的毫秒数|
|void join()|等待这个线程死亡|
|void setDaemon(boolean on)|将此线程标记为守护线程，当运行的线程都是守护线程时，JVM退出|
#线程的生命周期
新建，就绪，运行，阻塞，死亡
#多线程的实现方式
##方式二:实现Runnable接口
- 定义一个类MyRunnable实现Runnable接口
- 在MyRunnable类中重写run()方法
- 创建MyRunnable类的对象
- 创建Thread类的对象，把MyRunnable对象作为构造方法的参数
- 启动线程
相比于继承Thread类，实现Runnable接口的好处:
- 避免了Java单继承的局限性
- 适合多个相同程序的代码去处理同一个资源的情况，把线程和程序的代码，数据有效分离，较好的体现了面向对象的设计思想
#线程同步
多线程程序是否有数据安全问题的标准
- 是否是多线程环境
- 是否有共享数据
- 是否有多条语句操作共享数据
如何解决多线程安全问题:
基本思想:让程序没有安全问题的环境
如何实现？
把多条语句操作共享数据的代码给锁起来，让任意时刻只能有一个线程执行即可，Java提供了同步代码块的方式进行解决
#同步代码块
格式:
synchronized(任意对象){
    多条语句操作共享数据的代码
}
synchronized(任意对象):就相当于给代码加锁了，任意对象就可以看成是一把锁
同步的好处和弊端:
- 好处:解决了多线程的数据安全问题
- 弊端:当线程很多时，因为每个线程都会去判断同步上的锁，这是很耗费资源的，无形中会降低程序的运行效率
#同步方法:
同步方法:就是把synchronized关键字加到方法上
格式:
- 修饰符 synchronized 返回值类型 方法名(方法参数){}
同步方法的锁对象是什么呢？
- this
同步静态方法:就是把synchronized关键字加到静态方法上
格式:
- 修饰符 static synchronized 返回值类型 方法名(方法参数){}
同步静态方法的锁对象是什么呢？
- 类名.class
#线程安全的类
StringBufer
- 线程安全，可变的字符序列
- 从JDK5开始，被StringBuilder替代，通常应该使用StringBuilder类，因为它支持所有的操作，但它更快，因为它不执行同步
Vector
- 该类改进了List接口，使其成为JavaCollectionFramework的成员，与新的集合实现不同，Vector被同步。如果不需要线程安全的实现，建议使用ArrayList代替Vector
Hashtable:
- 该类实现了一个哈希表，它将键映射到值，任何非null对象都可以用作键或值
- 该类实现了Map接口，使其成为JavaCollectionFramework的成员，与新的集合实现不同，Hashtable被同步。如果不需要线程安全的实现，建议使用HashMap代替Hashtable
##但一般也不使用Vector或Hashtable
而是使用Collections类中的静态方法:
- public static <T> List <T> synchronizedList(List<T> list) 返回由指定列表支持的同步(线程安全)列表
- public static <K,V> Map<K,V> synchronizedMap(Map<K,V> m) 返回由指定Map支持的同步(线程安全)Map
#Lock锁(接口)
Lock实现提供比使用synchronized方法和语句可以获得更广泛的锁定操作
- void lock(): 获得锁
- void unlock(): 释放锁
Lock是接口，不能实例化，这里采用它的实现类ReentrantLock来实例化
- 构造方法:ReentrantLock():创建一个ReentrantLock的实例
*一般使用try{lock.lock();...}final{lock.unlock();}*
#生产者消费者模式
- 生产者线程用于制造数据
- 消费者线程用于消费数据
Object类中的等待和唤醒方法
|方法名|说明|
|---|---|
|void wait()|导致当前线程等待，直到另一个线程调用该对象的notify()方法或notifyAll()方法|
|void notify()|唤醒正在等待对象监视器的单个线程|
|void notifyAll()|唤醒正在等待对象监视器的所有线程|
#网络编程
在网络通信协议下，实现网络互连的不同计算机运行的程序间可以进行数据交换
#网络编程三要素
IP:标识计算机
端口:设备中的应用程序
协议:规则
#IP地址
常用命令:
- ipconfig:查看本机IP地址
- ping IP地址:检查网络是否连通
特殊IP地址:
- 127.0.0.1:是回送地址，可以代表本机地址，一般用来测试使用
#InetAddress的使用
InetAddress:此类表示Internet协议(IP)地址

|方法名|说明|
|---|---|
|static InetAddress getByName(String host)|确定主机名称的IP地址。主机名称可以是机器名称，也可以是IP地址|
|String getHostName()|获取次IP地址的主机名|
|String getHostAddress()|返回文本显示中的IP地址字符串|
#端口
端口:设备上应用程序的唯一标识
端口号:用两个字节表示的整数，0-65535，其中0-1023用于一些知名的网络服务和应用，普通的应用程序使用1024以上的端口号。如端口号被另外一个服务或应用占用，会导致当前程序启动失败。
#协议
UDP，TCP
#UDP通信程序
Java提供了DatagramSocket类作为基于UDP协议的Socket
#UDP发送数据
1. 创建发送端的Socket对象(DatagramSocket)
    DatagramSocket()
2. 创建数据，并把数据打包
    DatagramPacket(byte[] buf, int length, InetAddress address, int port)
3. 调用DatagramSocket对象的方法发送数据
    void send(DatagramPacket p)
4. 关闭发送端
    void close()
#UDP接收数据
1. 创建接收端的Socket对象(DatagramSocket)
    DatagramSocket(int port,InetAddress address)
2. 创建一个数据包，用于接收数据
    DatagramPacket(byte[] buf, int length)
3. 调用DatagramSocket对象的方法接收数据
    void receive(DatagramPacket p)
4. 解析数据包，并把数据在控制台上显示
    byte[] getData()
    int getLength()
5. 关闭接收端
    void close()
#TCP通信
Java对基于TCP协议的网络提供了良好的封装，使用Socket对象来代表两端的通信端口，并通过Socket产生的IO流来进行网络通信
Java为客户端提供了Socket类，为服务器端提供了SreverSocket类
#TCP发送数据
1. 创建客户端的Socket对象(Socket)
    Socket(String host, int port)
2. 获取输出流，写数据
    OutputStream getOutputStream()
3. 释放资源
    void close()
#TCP接收数据
1. 创建服务器端的Socket对象(ServerSocket)
    ServerSocket(int port)
2. 监听客户端连接，返回一个Socket对象
    Socket accept()
3. 获取输入流，读数据，并把数据显示在控制台
    InputStream getInputStream()
4. 释放资源
    void close()
#服务器读数据是阻塞式的，可能出现一直等待的情况
解决方法:自定义结束标记或使用shutdownOutput()方法(在客户端)(推荐)
#Lambda表达式
#函数式编程思想
强调做什么，而不是以什么形式去做
面向对象思想强调“必须通过对象的形式来做事情”
#Lambda表达式的标准形式
三要素:形式参数，箭头，代码块
格式:(形式参数)->{代码块}
形式参数:如果有多个参数，用逗号隔开
代码块:具体要做的事情
#Lambda表达式的使用前提
- 有一个接口
- 接口中有且只有一个抽象方法
#lambda表达式的省略格式
- 参数类型可以省略，有多个参数的情况下，不能只省略一个
- 如果参数有且只有一个，那么小括号可以省略
- 如果代码块的语句只有一条，可以省略大括号和分号，甚至是return
#Lambda的注意事项
1. 使用Lambda必须要有接口，并且要求接口中有且只有一个抽象方法
2. 必须要有上下文环境，才能推导出Lambda对应的接口
- 可以根据局部变量的复制得知Lambda对应的接口:
Runnable r = () -> System.out.println("hello world"));
- 根据调用方法的参数得知Lambda对应的接口:
new Thread(() -> System.out.println("hello world")).start();
#Lambda表达式和匿名内部类的区别
所属类型不同:
- 匿名内部类:可以是接口，抽象类，具体类
- Lambda表达式:只能是接口
使用限制不同:
- 如果接口中有且只有一个抽象方法，可以使用Lambda表达式，也可以使用匿名内部类
- 如果接口中多于一个抽象方法，只能使用匿名内部类，而不能用Lambda表达式
实现原理不同:
- 匿名内部类:编译之后，产生一个单独的.class字节码文件
- Lambda表达式:编译之后，没有一个单独的.class字节码文件，对应的字节码会在运行的时候动态生成
#接口组成更新
接口的组成:
- 常量: public static final
- 抽象方法: public abstract
- 默认方法(Java 8)
- 静态方法(Java 8)
- 私有方法(Java 9)
#接口中的默认方法
接口中默认方法的定义格式:
- 格式: public defailt 返回值类型 方法名(参数列表){}
- 例: public default void show(){}
接口中默认方法的注意事项:
- 默认方法不是抽象方法，所以不强制重写，但是也可以被重写，重写的时候去掉default关键字
- public可以省略，default不能省略
#接口中的静态方法
- 格式: public static 返回值类型 方法名(参数列表){}
- 例: public static void show(){}
接口中的静态方法注意事项
- 静态方法只能通过接口名调用，不能通过实现类名或者对象名调用
- public 可以省略，static 不能省略
#接口中私有方法
格式:
- private 返回值类型 方法名(参数列表){}
- private static 返回值类型 方法名(参数列表){}
接口中私有方法的注意事项:
- 默认方法可以调用私有的静态方法和非静态方法
- 静态方法只能调用私有的静态方法
#方法引用
使用已经存在的方案
#方法引用符
- ::该符号为方法引用符，它所在的表达式为方法引用
- Lambda表达式:usePrintable(s->System.out.println(s);
分析:拿到参数s之后通过Lambda表达式，传递给System.out.println方法去处理
- 方法引用:usePrintable(System.out::println);
分析:直接使用System.out中的println方法来取代Lambda，代码更加的简洁
#推导与省略
- 如果使用Lambda，那么根据“可推导就是可省略的原则，无需指定参数类型，也无需指定重载形式，他们都将被自动推导
- 如果使用方法引用，也是同样可以根据上下文进行推导
- 方法引用是Lambda的孪生兄弟
#Lambda表达式支持的方法引用
常见的引用方式:
- 引用类方法
- 引用对象的实例方法
- 引用类的实例方法
- 引用构造器
#引用类方法
就是引用类的静态方法
格式: 类名::静态方法
例子: Integer::parseInt
    Integer类的方法: public static int parseInt(String s)将此字符串转换为int类
Lambda表达式被类方法替代的时候，它的形式参数全部传递给静态方法作为参数
#引用对象的实例方法
就是引用类的实例方法
格式: 对象::成员方法
Lambda表达式被对象的实例方法替代的时候，它的形式参数全部传递给该方法作为参数
#引用类的实例方法
就是引用类中的成员方法
格式: 类名::成员方法
Lambda表达式被类的实例方法替代的时候，它的形式参数第一个参数作为调用者，其余参数全部传递给该方法作为参数
#引用构造器
就是引用构造方法
格式: 类名::new
Lambda表达式被构造器替代的时候，它的形式参数全部传递给构造器作为参数
#函数式接口
有且只有一个抽象方法的接口
Java中函数式编程体现就是Lambda表达式，所以函数式接口就是可以适应于Lambda使用的接口
如何检测一个接口是否是函数式接口呢？
加上@FunctionalInterface，看是否报错
注意:在自己写函数式接口的时候建议加上@FunctionalInterface注解
#函数式接口作为方法的参数
如果方法的参数是一个函数式接口，可以使用Lambda表达式作为参数传递
#函数式接口作为方法的返回值
如果方法的返回值是一个函数式接口，可以使用Lambda表达式作为结果返回
ex: arr.sort((s1,s2)->s1.length()-s2.length());
#常用的函数式接口
- Supplier接口
- Consumer接口
- Predicate接口
- Function接口
#Supplier接口
Supplier<T>:包含一个无参的方法
- T get():获得结果
- 该方法不需要参数，它会按照某种实现逻辑(由Lambda表达式实现)返回一个数据
Supplier<T>接口被称为生产型接口，如果我们指定了接口的泛型是什么类型，那么接口中的get方法就会产生什么类型的数据供我们使用
#Consumer接口
- void accept(T t): 对给定的参数执行此操作
- default Consumer<T> andThen(Consumer after): 返回一个组合的Consumer，依次进行此操作，然后执行after操作
Consumer<T>接口也被称为消费型接口，它消费的数据的数据类型由泛型指定
#Predicate接口
常用方法:
- boolean test(T t):对给定的参数进行判断(判断逻辑由lambda表达式实现)，返回一个布尔值
- default Predicate<T> negate():返回一个逻辑的否定，对应逻辑非
- default Predicate<T> and(Predicate other):返回一个组合判断，对应短路与
- default Predicate<T> or(Predicate other):返回一个组合判断，对应短路或
Predicate<T>接口通常用于判断参数是否满足指定的条件
#Function接口
Function<T,R>:
- R apply(T t):将此函数应用于给定的参数
- default <V> Function andThen(Function after):返回一个组合函数，首先将此函数应用于输入，然后将after函数应用于结果
Function<T,R>接口通常用于对参数进行处理，转换(处理和转换逻辑由lambda表达式实现)，然后返回一个新的值
#Stream流
使用Stream流的方式进行过滤操作
```
list.stream()filter(s->s.startWith("张")).filter(s->s.length()==3).forEach(System.out::println);
```
- 直接阅读代码的字面意思即可完美展示无关逻辑方式的语义
- Stream流把真正的函数式编程风格引入到Java中
#Stream流的生成方式
- 生成流
    通过数据源(集合，数组等)生成流 list.stream()
- 中间操作
    一个流后面可以跟随零个或多个中间操作，其目的主要是打开流，做出某种程度的数据过滤/映射，然后返回一个新的流，交给下一个操作使用 filter()
- 终结操作
    一个流只能有一个终结操作，当这个操作执行后，流就被使用“光”了，无法再被操作，所以这必定为流的最后操作 forEach()
#Stream流的生成方式
- Collection体系的集合可以使用默认方法的stream()生成流
    default Stream<E> stream()
- Map体系的集合间接的生成流
- 数组可以通过Stream接口的静态方法of(T...values)生成流
#Stream流的常见中间操作方法
- Stream<T> filter(Predicate predicate):用于对流中的数据进行过滤
    Predicate接口中的方法:boolean test(T t):对给定的参数进行判断，返回一个布尔值
- Stream<T> limit(long maxsize):返回此流中的元素组成的流，截取前指定参数个数的数据
- Stream<T>skip(long n):跳过指定参数个数的数据，返回由该流的剩余元素组成的流
- static <T> Stream <T> concat(Stream a,Stream b):合并a和b两个流为一个流
- Stream <T> distinct():返回由该流的不同元素(根据Object.equals(Object))组成的流
- Stream<T> sorted():返回由该流的元素组成的流，根据自然顺序排序
- Stream<T>sorted(Comparator comparator):返回由该流的元素组成的流，根据提供的比较器进行排序
- <R> Stream <R> map(Function mapper):返回由指定函数应用于此流的元素的结果组成的流
    Function接口中的方法  R apply(T t)
- IntStream mapToInt(ToIntFunction mapper):返回一个IntStream其中包含将给定函数应用于此流的元素的结果
    IntStream:表示原始流
    ToIntFunction接口中的方法 int applyAsInt(T value)
    注:IntStream中有sum()方法，用于求和
#Stream流的常见终结操作方法
- void forEach(Consumer action):对此流的每个元素执行操作
    Consumer接口中的方法  void accept(T t):对给定的参数执行此操作
- long count():返回此流中的元素数
#Stream流的收集操作
- R collect(Collector collector)
- 但是这个收集方法的参数是一个Collector接口
工具类Collectors提供了具体的收集方式:
- public static <T> Collector toList():把元素收集到List集合中
- public static <T> Collector toSet():把元素收集到Set集合中
- public statoc Collector toMap(Function keyMapper,Function valueMapper):把元素收集到Map集合中
#反射
#类加载器
程序要使用某个类时，如该类还未加载到内存，则系统会通过类的加载，类的连接，类的初始化三个步骤来对类进行初始化，有时将这三个步骤统称为类加载或类初始化。
类的加载:
- 就是将Class文件读入内存，并为之创建一个java.lang.Class对象
- 任何类使用时，系统都会为之建立一个java.lang.Class对象
类的连接:
- 验证阶段:用于检验被加载的类是否有正确的内部结构，并和其他类协调一致
- 准备阶段:负责为类的类变量分配内存，并设置默认初始值
- 解析阶段:将类的二进制数据中的符号引用替换为直接引用
类的初始化:
- 在该阶段，主要就是对类的变量进行初始化
类的初始化步骤:
* 假如类还未被加载和连接，则程序先加载连接该类
* 假如该类的直接父类还未被初始化，则先初始化其直接父类
* 加入类中有初始化语句，则系统依次执行这些初始化语句
类的初始化时机:
* 创建类的实例
* 调用类的类方法
* 访问类或者接口的类变量，或者为该类变量赋值
* 使用反射方式来强制创建某个类或接口对应的java.lang.Class对象
* 初始化某个类的子类
* 直接使用java.exe命令来运行某个主类
#类加载器
类加载器的作用:
- 负责将.class文件加载到内存中，并为之生成对应的java.lang.Class对象
- 虽然不用过分关心类加载机制，但了解这个机制就能更好地李杰程序地运行
JVM地类加载机制:
- 全盘负责: 就是当一个类加载器负责加载某个Class时，该Class所依赖的和引用的其他Class也将由该类加载器负责载入，除非显示使用另一个类加载器来载入
- 父类委托:就是当一个类加载器负责加载某个Class时，先让父类加载器试图加载该Class，只有在父类加载器无法加载该类时才尝试从自己的类路径中加载该类
- 缓存机制:保证所有加载过的Class都会被缓存，当程序需要使用某个Class对象时，类加载器先从缓存区搜索该Class，只有当缓存区不存在该Class对象时，系统才会读取该类对应的二进制数据，并将其转换为Class对象，存储到缓存区
#类加载器
ClassLoader:是负责加载类的对象
- Bootstrap class loader:它是虚拟机的内置类加载器，通常表示为null，并且没有父null
- Platform class loader:平台类加载器可以看到所有平台类，平台类包括平台类加载器或其祖先定义的JavaSE平台API，其实现类和JDK特定的运行时类
- System class loader:它被称为应用程序类加载器，与平台加载器不同。系统类加载器通常用于定义应用程序类路径，模块路径和JDK特定工具上的类
- -类加载器的继承关系:System的父加载器为Platform，Platform的父加载器是Bootstrap
ClassLoader中的两个方法:
- static ClassLoader getSystemClassLoader():返回用于委派的系统类加载器
- ClassLoader getParent():返回父类加载器进行委派
#反射
Java反射机制:是指在运行时去获取一个类的变量和方法信息。然后通过获取到的信息来创建对象，调用方法的一种机制。由于这种动态性，可以极大地增强程序的灵活性，程序不用在编译期就完成确定，在运行期仍然可以扩展
#获取Class类的对象
想要反射去使用一个类，首先要获得到该类的字节码文件对象，也就是为Class类型的随想，三种方式获取Clas
类型的对象:
- 使用类的class属性来获取该类对应的Class对象。ex:Student.class
- 调用对象的getClass()方法，返回该对象所述类对应的Class对象
    该方法时Object类中的方法，所有的Java对象都可以调用该方法
- 使用Class类中的静态方法forName(String classname),该方法需要传入字符串参数，该字符串参数值是某个类的全路径，也就是完整包名的路径
#反射获取构造方法并使用
Class类中用于获取构造方法的方法
- Constructor<?>[] getConstructors() 返回所有公共构造方法对象的数组
- Constructor<?>[] getDeclaredConstructor() 返回所有构造方法对象的数组
- Constructor<T> getConstructor(类<?>... parameterTypes) 返回单个公共构造方法对象
- Constructor<T> getDeclaredConstructor(类<?>... parameterTypes) 返回单个构造方法对象
Constructor类中用于创建对象的方法:
- T newInstance(Object... initargs) 根据指定的构造方法创建对象
注:
- 基本数据类型也可以通过.class得到对应的Class类型
- public void setAccessible(boolean flag):值为true，取消访问检查(暴力反射)
#反射获取成员变量并使用
获取成员变量的方法
- Field[] getFields() 返回所有公共成员变量对象的数组
- Field[] getDeclaredFields() 返回所有成员变量对象的数组
- Field getField(String name) 返回单个公共成员变量对象
- Field getDeclaredField(String name) 返回单个成员变量对象
Field类中用于给成员变量复制的方法
- void set(Object obj, Object value) 给obj对象的成员变量赋值为value
#反射获取成员方法并使用
Class类中获取成员变量的方法
- Method[] getMethods() 返回所有公共成员方法对象的数组，包括继承的
- Method[] getDeclaredMethods() 返回所有成员方法对象的数组，不包括继承的
- Method getMethod(String name, Class<?>... parameterTypes) 返回单个公共成员方法对象
- Method getDeclaredMethod(String name, Class<?>... parameterTypes) 返回单个成员方法对象
Method类中用于调用成员方法的方法
- Object invoke(Object obj, Object... args) 调用obj对象的成员方法，参数是args，返回值是Object类型
#模块化(Java 9)
- 在模块的src目录下新建一个名为module-info.java的描述性文件，该文件专门定义模块名，访问权限，模块依赖等信息
描述性文件中使用模块导出和模块依赖来进行配置并使用
- 模块中所有未导出的包都是模块私有的，他们是不能在模块之外被访问的
模块导出格式:exports 包名;