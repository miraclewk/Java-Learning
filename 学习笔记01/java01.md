# Java基础语法

## 基础知识
一个 Java 程序可以认为是一系列对象的集合，而这些对象通过调用彼此的方法来协同工作。下面简要介绍下类、对象、方法和实例变量的概念。

<font color=Yellow size=3 face="微软雅黑">对象：</font>
对象是类的一个实例，有状态和行为。例如，一条狗是一个对象，它的状态有：颜色、名字、品种；行为有：摇尾巴、叫、吃等。

<font color=Yellow size=3 face="微软雅黑">类：</font>
类是一个模板，它描述一类对象的行为和状态。

<font color=Yellow size=3 face="微软雅黑">方法：</font>
方法就是行为，一个类可以有很多方法。逻辑运算、数据修改以及所有动作都是在方法中完成的。

<font color=Yellow size=3 face="微软雅黑">实例变量：</font>
每个对象都有独特的实例变量，对象的状态由这些实例变量的值决定。

## 注意事项
编写Java程序应注意以下几点：

<font color=Gree size=3 face="微软雅黑">大小写敏感：</font>
Java 是大小写敏感的，这就意味着标识符 Hello 与 hello 是不同的。

<font color=Gree size=3 face="微软雅黑">类名：</font>
对于所有的类来说，类名的首字母应该大写。如果类名由若干单词组成，那么每个单词的首字母应该大写，例如 MyFirstJavaClass 。

<font color=Gree size=3 face="微软雅黑">方法名：</font>
所有的方法名都应该以小写字母开头。如果方法名含有若干单词，则后面的每个单词首字母大写。例如myFirstWay.

<font color=Gree size=3 face="微软雅黑">源文件名：</font> 
源文件名必须和类名相同。当保存文件的时候，你应该使用类名作为文件名保存（切记 Java 是大小写敏感的），文件名的后缀为 .java。（如果文件名和类名不相同则会导致编译错误）。（*这个的意思是说当我们编写Java程序进行保存的时候文件名应与代码的最外面的类名保持一致*）

<font color=Gree size=3 face="微软雅黑">主方法入口：</font> 
所有的 Java 程序由 public static void main(String []args) 方法开始执行。（*类似于C语言的main函数*）

## 第一个程序HelloWorld
```
public class HelloWorld{ //这个类名应与保存的文件名一致，在此应保存为HelloWorld.Java
    public static void main(string[] args){
        System.out.println("Hello World")
    }
}
```
写完程序之后再命令窗口进入当前程序所在位置输入`javac HelloWorld.java`进行编译，代码没有错误的话，再输入`java HelloWorld`即可运行输出结果。

# Java对象和类

基本的概念由上述内容已知，再举个简单的例子来说明类和对象，例如：男生是一个类（Class），具体到每个人则是对象（Object）。

## 变量

类中的变量介绍如下：

<font color=Yellow size=3 face="微软雅黑">局部变量：</font>
局部变量的声明和初始化都是定义在方法中。方法结束，变量就会自动销毁。

<font color=Yellow size=3 face="微软雅黑">成员变量：</font>
成员变量则是定义在方法外，类中的变量。可以被类中的方法引用。

<font color=Yellow size=3 face="微软雅黑">类变量：</font>
类变量也声明在类中，方法外，但必须声明为static类型。

## 构造方法

每个类都有构造方法。如果没有显式地为类定义构造方法，Java编译器将会为该类提供一个默认构造方法。构造方法是为了new一个对象时能够赋值。

## 创建对象

创建对象的语法为```Dog xiaoh = new Dog()```，假设存在一个Dog类了。

如果假设要声明一个int数组变量，因为在Java中数组变量也是数组对象，语法为```int[] nums = new int[6]```，然后直接进行赋值操作即可，如```nums[0]=1```。

但如果是对象如创建Dog数组，语法则为```Dog[] pets = new Dog[7]```,具体引用的时候略有不同，应该为```pet[0] = new Dog()```。每个都应该重新new一下，因为之前只是生命了这个数组。

# Java基本数据类型

byte--8位，默认值：0；short--16位，默认值：0；int--32位，默认值：0；long--64位，默认值：0L；float--32位，默认值：0.0f；double--64位，默认值：0.0d；
