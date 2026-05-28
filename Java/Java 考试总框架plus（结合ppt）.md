可以，我给你整理成一份**考前速成版 Java 知识框架**。
我会严格按你的提纲顺序走：**第1章 → 第2章 → 第3章 → 第4章 → 第5章 → 第6章 → 第7章**。你的提纲里明确说第3、4、5章是“重点中的重点”，第6章异常会考程序填空，第7章文件流也会考程序填空，所以这几章我会重点标出来。

------

# Java 考试总框架

你可以把 Java 这门课理解成一条线：

```text
Java特点
  ↓
基础语法：变量、数据类型、运算符、流程控制
  ↓
类和对象：用类描述现实事物
  ↓
继承和多态：让类之间产生关系
  ↓
高级特征：abstract、static、final、this、接口、参数传递
  ↓
常用工具：数组、字符串、ArrayList、Vector
  ↓
异常处理：程序出错时怎么处理
  ↓
文件与数据流：程序怎么读写文件
```

你的考试不是考算法竞赛，而是考你能不能看懂和写出**标准 Java 代码模板**。

------

# 第一章 绪论

## 1. Java 语言的特点

**通俗理解：**
Java 是一种面向对象语言，程序的核心单位是“类”。它不像 C 那样主要围绕函数写，而是围绕“类和对象”组织代码。

第一章 PPT 介绍 Java 是由 Sun 公司推出的面向对象程序设计语言，课程内容包括 Java 基础、面向对象、高级特征、数组字符串集合、异常处理和输入输出等。

### 重点

Java 常见特点：

| 特点       | 通俗解释                     |
| ---------- | ---------------------------- |
| 面向对象   | 用“类”和“对象”组织程序       |
| 跨平台     | 一次编写，可以在不同系统运行 |
| 安全性较高 | 没有 C 那种直接指针操作      |
| 健壮性     | 有异常处理机制               |
| 多线程     | 支持多个任务同时执行         |

### 必考点

最容易出选择、判断、简答：

```text
Java 是面向对象的程序设计语言。
Java 程序的基本单位是类。
Java 具有跨平台性。
```

### 极简代码示例

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello Java");
    }
}
```

### 易错点

`main` 方法格式要记死：

```java
public static void main(String[] args)
```

不要写成：

```java
public void main()
```

------

# 第二章 Java 语言基础

第二章提纲要求重点掌握：标识符、数据类型、变量声明、运算符、if/switch、循环、break 和 continue。

------

## 1. 标识符

**通俗理解：**
标识符就是你给变量、类、方法起的名字。

PPT 中说明，Java 标识符可以用来标识文件名、变量名、类名、方法名等；标识符区分大小写，不能使用关键字、`false`、`true` 和 `null`。

### 重点

合法标识符：

```java
age
studentName
_myName
$abc
HelloWorld
```

非法标识符：

```java
123abc      // 不能数字开头
class       // 关键字不能用
a+b         // 不能有 +
my name     // 不能有空格
```

### 必考点

判断是否合法：

```text
1. 可以由字母、数字、_、$ 组成
2. 不能以数字开头
3. 不能是关键字
4. 区分大小写
```

### 极简代码示例

```java
int age = 20;
int Age = 30;
System.out.println(age); // 20
System.out.println(Age); // 30
```

### 易错点

`age` 和 `Age` 是两个不同变量。

------

## 2. 数据类型

**通俗理解：**
Java 变量必须先说明“里面放什么类型的数据”。

PPT 中强调 Java 基本数据类型一共 8 种，并且每种类型占用位数固定，不依赖具体计算机。

### 重点：8 种基本数据类型

| 类型    | 位数             | 说明                     |
| ------- | ---------------- | ------------------------ |
| byte    | 8                | 字节整数                 |
| short   | 16               | 短整数                   |
| int     | 32               | 整数，最常用             |
| long    | 64               | 长整数                   |
| float   | 32               | 单精度小数               |
| double  | 64               | 双精度小数，默认小数类型 |
| char    | 16               | 字符                     |
| boolean | 通常不考具体位数 | true / false             |

### 必考点

```java
int a = 10;
double b = 3.14;
char c = 'A';
boolean flag = true;
String s = "Java";
```

### 极简代码示例

```java
int age = 18;
double score = 95.5;
char grade = 'A';
boolean pass = true;
```

### 易错点

`char` 用单引号：

```java
char c = 'A';
```

`String` 用双引号：

```java
String s = "A";
```

`float` 后面要加 `f`：

```java
float x = 3.14f;
```

`long` 后面最好加 `L`：

```java
long n = 10000000000L;
```

------

## 3. 基本数据类型和引用数据类型

**通俗理解：**

基本数据类型：变量里直接放值。
引用数据类型：变量里放的是对象地址。

PPT 中说，引用数据类型声明后不直接开空间，只有通过实例化，才能给数据开辟空间。

### 重点

```java
int a = 10;              // 基本数据类型
String s = new String("hi"); // 引用数据类型
```

### 必考点

```text
基本数据类型：byte、short、int、long、float、double、char、boolean
引用数据类型：类、数组、接口、String 等
```

### 极简代码示例

```java
int a = 10;
String s = new String("hello");
```

### 易错点

数组、String、对象都属于引用数据类型。

------

## 4. 运算符

### 4.1 算术运算符

```java
+  -  *  /  %
```

### 极简示例

```java
int a = 10;
int b = 3;
System.out.println(a / b); // 3
System.out.println(a % b); // 1
```

### 易错点

两个 `int` 相除，结果还是 `int`。

```java
System.out.println(5 / 2); // 2
```

不是 `2.5`。

------

### 4.2 关系运算符

```java
>  <  >=  <=  ==  !=
```

结果一定是 `boolean`。

```java
int a = 10;
System.out.println(a > 5); // true
```

------

### 4.3 布尔逻辑运算符和短路规则

```java
&&   ||   !
```

**通俗理解：**

`&&`：两个都真才真。
`||`：有一个真就真。
`!`：取反。

### 必考点：短路规则

```java
int a = 5;
if (a > 10 && a++ > 0) {
}
System.out.println(a); // 5
```

因为 `a > 10` 已经是 false，后面的 `a++ > 0` 不执行。

### 易错点

`&&` 和 `||` 可能不会执行右边表达式。

------

## 5. if / if-else

### 极简代码

```java
int score = 80;

if (score >= 60) {
    System.out.println("及格");
} else {
    System.out.println("不及格");
}
```

### 必考点

会和数组、字符串、类综合出题。

------

## 6. switch

### 极简代码

```java
int day = 2;

switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    default:
        System.out.println("Other");
}
```

### 易错点

忘记 `break` 会继续执行后面的 `case`。

------

## 7. for / while / do-while

### for

```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

### while

```java
int i = 0;
while (i < 5) {
    System.out.println(i);
    i++;
}
```

### do-while

```java
int i = 0;
do {
    System.out.println(i);
    i++;
} while (i < 5);
```

### 易错点

`do-while` 至少执行一次。

------

## 8. break 和 continue

### break：结束整个循环

```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) break;
    System.out.println(i);
}
```

输出：

```text
1
2
```

### continue：跳过本次循环

```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) continue;
    System.out.println(i);
}
```

输出：

```text
1
2
4
5
```

### 易错点

`break` 是“彻底结束循环”。
`continue` 是“跳过这一次，继续下一次”。

------

# 第三章 面向对象程序设计基础【重点中的重点】

提纲明确说第三章是重点中的重点，要求掌握类、对象、变量、方法、构造方法，以及继承性和多态性，继承和多态会考概念题和程序题。

------

## 1. 类和对象

**通俗理解：**

类：模板。
对象：根据模板造出来的具体东西。

第三章 PPT 中说，类是一种模板或原型，定义了某种类型所有对象都具有的变量和方法；对象是在类模型基础上构造出的具体实例。

### 重点

```java
class Student {
    String name;
    int age;

    void show() {
        System.out.println(name + " " + age);
    }
}
```

### 极简代码示例

```java
class Student {
    String name;
    int age;
}

public class Main {
    public static void main(String[] args) {
        Student s = new Student();
        s.name = "Tom";
        s.age = 20;
        System.out.println(s.name);
    }
}
```

### 必考点

```text
类 = 属性 + 方法 + 构造方法
对象 = 类的实例
new = 创建对象
```

### 易错点

```java
Student s;
```

这只是声明引用，还没有创建对象。

必须：

```java
Student s = new Student();
```

------

## 2. 成员变量和局部变量

**通俗理解：**

成员变量：写在类里，属于对象。
局部变量：写在方法里，只在方法内部有效。

PPT 中说，在一个 Java 源文件或类中定义的变量称为全局变量；在成员方法或代码块内定义的是局部变量，局部变量使用前必须初始化。

### 极简代码示例

```java
class Student {
    int age; // 成员变量

    void show() {
        int score = 90; // 局部变量
        System.out.println(score);
    }
}
```

### 易错点

局部变量必须先赋值才能使用。

```java
void test() {
    int a;
    System.out.println(a); // 错
}
```

------

## 3. 成员方法

**通俗理解：**
方法就是对象能做的事情。

### 极简代码示例

```java
class Dog {
    void bark() {
        System.out.println("汪汪");
    }
}
```

调用：

```java
Dog d = new Dog();
d.bark();
```

### 必考点

方法格式：

```java
返回类型 方法名(参数列表) {
    方法体
}
```

------

## 4. 构造方法

**通俗理解：**
构造方法是创建对象时自动调用的方法，通常用来初始化对象。

PPT 中说明，构造方法与类同名，用于创建类的实例对象，通常用来初始化实例对象；构造方法没有返回类型，连 `void` 也不能写。

### 极简代码示例

```java
class Student {
    String name;

    Student(String n) {
        name = n;
    }
}
```

使用：

```java
Student s = new Student("Tom");
```

### 必考点

构造方法三大特点：

```text
1. 方法名和类名相同
2. 没有返回值，不能写 void
3. 创建对象时自动调用
```

### 易错点

错误写法：

```java
void Student(String n) {
}
```

这不是构造方法，这是普通方法。

------

## 5. 面向对象三大特性

```text
封装性
继承性
多态性
```

提纲说：封装性具体知识点不考，只要知道它是三大特性之一即可；重点掌握继承性和多态性。

------

## 6. 继承性【必考】

**通俗理解：**
子类可以继承父类已有的属性和方法，减少重复代码。

### 极简代码示例

```java
class Animal {
    void eat() {
        System.out.println("eat");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("bark");
    }
}
```

使用：

```java
Dog d = new Dog();
d.eat();
d.bark();
```

### 必考点

```java
class 子类 extends 父类
```

### 易错点

Java 类只能单继承：

```java
class A extends B { }
```

不能：

```java
class A extends B, C { } // 错
```

------

## 7. 方法重写

**通俗理解：**
子类觉得父类的方法不好用，于是重新写一遍。

### 极简代码示例

```java
class Animal {
    void speak() {
        System.out.println("Animal");
    }
}

class Dog extends Animal {
    void speak() {
        System.out.println("Dog");
    }
}
```

### 必考点

重写要求：

```text
方法名相同
参数列表相同
返回类型兼容
发生在父子类之间
```

------

## 8. 多态性【必考】

**通俗理解：**
同一个父类引用，指向不同子类对象，执行结果不同。

### 极简代码示例

```java
class Animal {
    void speak() {
        System.out.println("Animal");
    }
}

class Dog extends Animal {
    void speak() {
        System.out.println("Dog");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal a = new Dog();
        a.speak();
    }
}
```

输出：

```text
Dog
```

### 必考点

```java
父类引用 = new 子类对象();
```

### 易错点

记住一句话：

```text
编译看左边，运行看右边。
```

例如：

```java
Animal a = new Dog();
a.speak();
```

能不能调用 `speak()`，看左边 `Animal`。
真正执行谁的 `speak()`，看右边 `Dog`。

------

# 第四章 Java 高级特征【重点中的重点】

提纲要求重点掌握 `abstract`、`static`、`final`、`this`、接口、方法参数传递和面向对象程序设计；其中包的知识点不考。

------

## 1. abstract 抽象类和抽象方法【重点】

**通俗理解：**
抽象类像“半成品模板”，规定子类必须完成某些方法。

### 极简代码示例

```java
abstract class Animal {
    abstract void speak();
}

class Dog extends Animal {
    void speak() {
        System.out.println("Dog");
    }
}
```

### 必考点

```text
1. 抽象类用 abstract class
2. 抽象方法没有方法体
3. 有抽象方法的类必须是抽象类
4. 抽象类不能 new 对象
5. 子类必须实现抽象方法，否则子类也要 abstract
```

### 易错点

错误：

```java
abstract void speak() {
    System.out.println("hi");
}
```

抽象方法不能有方法体。

------

## 2. static

**通俗理解：**
`static` 修饰的东西属于“类”，不属于某一个对象，所有对象共享。

第三章 PPT 中也提到，`static` 修饰静态变量，静态变量属于类，在内存中只保存一份，所有类对象共享，可以用类名直接访问。

### 极简代码示例

```java
class Student {
    static int count = 0;

    Student() {
        count++;
    }
}
```

使用：

```java
Student s1 = new Student();
Student s2 = new Student();
System.out.println(Student.count); // 2
```

### 必考点

```text
static 变量：类变量，所有对象共享
static 方法：类方法，可以用类名调用
```

### 易错点

推荐：

```java
Student.count
```

不要依赖：

```java
s1.count
```

虽然有时能用，但考试理解上要知道它属于类。

------

## 3. final

**通俗理解：**
`final` 表示“最终的，不能改”。

PPT 中说明，`final` 通常要求成员域在首次赋值以后不能再修改。

### 极简代码示例

```java
final int MAX = 100;
```

### 必考点

| final 修饰 | 含义         |
| ---------- | ------------ |
| final 变量 | 不能再次赋值 |
| final 方法 | 不能被重写   |
| final 类   | 不能被继承   |

### 易错点

```java
final int a = 10;
a = 20; // 错
```

------

## 4. this

**通俗理解：**
`this` 表示“当前对象”。

### 极简代码示例

```java
class Student {
    String name;

    Student(String name) {
        this.name = name;
    }
}
```

### 必考点

当成员变量和参数同名时，用 `this` 区分。

```java
this.name = name;
```

左边是成员变量，右边是参数。

### 易错点

不写 `this` 时：

```java
name = name;
```

这句很可能只是参数给参数赋值，成员变量没有被正确赋值。

------

## 5. 接口 interface【重点】

**通俗理解：**
接口是一种“规则”。类实现接口，就必须完成接口中规定的方法。

### 极简代码示例

```java
interface Flyable {
    void fly();
}

class Bird implements Flyable {
    public void fly() {
        System.out.println("fly");
    }
}
```

### 必考点

```text
接口用 interface 定义
类用 implements 实现接口
接口中的方法默认是 public abstract
接口中的变量默认是 public static final
一个类可以实现多个接口
```

### 易错点

实现接口方法时，必须写 `public`：

```java
public void fly() {
}
```

不能写成：

```java
void fly() {
}
```

因为接口方法默认是 `public`，实现时权限不能变小。

------

## 6. 方法的参数传递【必考/易错】

提纲明确说，方法参数传递会出选择题或程序填空题，而且要画图理解 PPT 例题。

**通俗理解：**
Java 参数传递本质上都是“值传递”。

### 情况一：基本数据类型

```java
public class Main {
    static void change(int x) {
        x = 100;
    }

    public static void main(String[] args) {
        int a = 10;
        change(a);
        System.out.println(a);
    }
}
```

输出：

```text
10
```

因为传进去的是 `a` 的值的副本。

------

### 情况二：引用数据类型

```java
class Student {
    int age = 18;
}

public class Main {
    static void change(Student s) {
        s.age = 20;
    }

    public static void main(String[] args) {
        Student stu = new Student();
        change(stu);
        System.out.println(stu.age);
    }
}
```

输出：

```text
20
```

因为传进去的是对象地址的副本，两个引用指向同一个对象。

### 易错点

Java 不是引用传递，而是：

```text
基本类型：传值的副本
引用类型：传地址值的副本
```

------

# 第五章 数组、字符串、泛型和集合类【重点中的重点】

提纲要求重点掌握数组、字符串、ArrayList 和 Vector；数组、字符串会考程序设计题，ArrayList 或 Vector 会出程序填空题。泛型和 LinkedList 不考。

------

## 1. 数组

**通俗理解：**
数组就是一组相同类型的数据。

PPT 中说，数组是具有相同数据类型的一组数据集合；数组创建后长度固定，下标从 0 开始，数组长度用 `length` 表示。

### 一维数组

```java
int[] a = {1, 2, 3};
System.out.println(a[0]);
```

### 必考点

```java
int[] a = new int[5];
```

默认值：

```text
int 默认 0
double 默认 0.0
boolean 默认 false
引用类型默认 null
```

### 易错点

数组下标从 0 开始。

```java
int[] a = {1, 2, 3};
System.out.println(a[3]); // 错，越界
```

PPT 中也强调，下标不能低于 0，也必须小于 `length`，否则会产生 `ArrayIndexOutOfBoundsException`。

------

## 2. 数组遍历【程序设计题常用】

### 极简代码示例

```java
int[] a = {1, 2, 3, 4};
int sum = 0;

for (int i = 0; i < a.length; i++) {
    sum += a[i];
}

System.out.println(sum);
```

### 必考点

数组长度：

```java
a.length
```

不是：

```java
a.length()
```

------

## 3. 二维数组

**通俗理解：**
二维数组像表格，有行有列。

### 极简代码示例

```java
int[][] a = {
    {1, 2},
    {3, 4}
};

System.out.println(a[0][1]); // 2
```

### 遍历

```java
for (int i = 0; i < a.length; i++) {
    for (int j = 0; j < a[i].length; j++) {
        System.out.println(a[i][j]);
    }
}
```

### 易错点

```java
a.length       // 行数
a[i].length    // 第 i 行的列数
```

------

## 4. 字符串 String

**通俗理解：**
字符串就是一串字符，比如 `"hello"`。

提纲规定字符串方法范围包括：`concat`、`replace`、`trim`、`substring`、`length`、`charAt`、`indexOf`、`lastIndexOf`、`compareTo`、`equals`。

------

## 5. String 常用方法【必考】

### 5.1 length

```java
String s = "hello";
System.out.println(s.length()); // 5
```

易错点：

```java
字符串：s.length()
数组：a.length
```

------

### 5.2 charAt

```java
String s = "hello";
System.out.println(s.charAt(1)); // e
```

------

### 5.3 substring

```java
String s = "hello";
System.out.println(s.substring(1, 4)); // ell
```

易错点：

```text
substring(1, 4) 包含下标1，不包含下标4
```

------

### 5.4 indexOf / lastIndexOf

PPT 中说明，`indexOf` 返回指定字符或子字符串第一次出现的位置，`lastIndexOf` 返回最后一次出现的位置。

```java
String s = "banana";
System.out.println(s.indexOf("a"));     // 1
System.out.println(s.lastIndexOf("a")); // 5
```

------

### 5.5 trim

```java
String s = "  Java  ";
System.out.println(s.trim()); // Java
```

作用：去掉首尾空格。

------

### 5.6 replace

```java
String s = "java";
System.out.println(s.replace("a", "o")); // jovo
```

------

### 5.7 concat

```java
String s1 = "hello";
String s2 = s1.concat(" java");
System.out.println(s2); // hello java
```

------

### 5.8 compareTo

PPT 中说明，`compareTo` 比较两个字符串内容，区分大小写；相等返回 0，当前字符串较小返回小于 0 的值，较大返回大于 0 的值。

```java
System.out.println("b".compareTo("a")); // 正数
System.out.println("a".compareTo("b")); // 负数
System.out.println("a".compareTo("a")); // 0
```

------

### 5.9 equals【易错/必考】

PPT 中说明，`equals` 比较字符串字符序列是否相同，区分大小写。

```java
String s1 = new String("abc");
String s2 = new String("abc");

System.out.println(s1.equals(s2)); // true
```

### 易错点

不要用 `==` 比较字符串内容。

```java
System.out.println(s1 == s2); // false，比较的是地址
```

------

## 6. 集合框架：ArrayList 和 Vector

**通俗理解：**
数组长度固定，集合长度可以变化。ArrayList 就像“可变长数组”。

PPT 中说，ArrayList 是 List 接口的具体实现，是可调整大小的数组，底层采用数组实现，适合频繁访问元素，以及只在末尾添加删除。

------

## 7. ArrayList【程序填空重点】

### 极简代码示例

```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList list = new ArrayList();

        list.add("Tom");
        list.add("Jack");

        System.out.println(list.size());
        System.out.println(list.get(0));

        list.set(0, "Lucy");
        list.remove(1);
    }
}
```

### 必考方法

| 方法        | 作用             |
| ----------- | ---------------- |
| add         | 添加元素         |
| size        | 获取元素个数     |
| get         | 获取指定位置元素 |
| set         | 修改指定位置元素 |
| remove      | 删除元素         |
| indexOf     | 第一次出现位置   |
| lastIndexOf | 最后一次出现位置 |

### 易错点

```java
list.size()
```

有括号。

数组是：

```java
arr.length
```

没括号。

------

## 8. Vector【程序填空重点】

PPT 中说，Vector 和 ArrayList 的区别之一是 Vector 允许多线程，ArrayList 只允许单线程；Vector 可通过 `add`、`addElement`、`insertElementAt` 增加元素，通过 `set`、`setElementAt` 修改元素。

### 极简代码示例

```java
import java.util.Vector;

public class Main {
    public static void main(String[] args) {
        Vector v = new Vector();

        v.add("Tom");
        v.add("Jack");

        System.out.println(v.get(0));

        v.set(0, "Lucy");
        v.remove(1);
    }
}
```

### 必考方法

```text
add
size
get
set
setElement
remove
setSize
indexOf
lastIndexOf
```

### 易错点

你的提纲里写的是 `setElement`，PPT 里 Vector 示例常见写法是：

```java
setElementAt("Lily", 1)
```

考试按老师 PPT 来，一定注意题目给的是哪个方法名。

------

# 第六章 异常处理【程序填空重点】

提纲明确说异常处理会考程序填空题，要掌握异常分类、常见异常、`try`、`catch`、`finally`、`throw`、`throws`，并注意 `throw` 和 `throws` 的区别。

------

## 1. 什么是异常

**通俗理解：**
异常就是程序运行中出现了“不正常情况”，比如数组越界、除数为 0、文件不存在。

PPT 中举例：数组下标越界、打开不存在的文件、网络无法连接、除数为 0、参数类型不匹配等都会导致异常。

### 常见异常

| 异常                           | 含义               |
| ------------------------------ | ------------------ |
| ArithmeticException            | 算术异常，如除以 0 |
| ArrayIndexOutOfBoundsException | 数组下标越界       |
| NullPointerException           | 空指针异常         |
| IOException                    | 输入输出异常       |
| FileNotFoundException          | 文件找不到         |

### 极简代码示例

```java
int a = 10 / 0; // ArithmeticException
```

------

## 2. 异常分类

PPT 中按编译时是否被检测，将异常分为受检异常和非受检异常；受检异常必须处理才能通过编译，非受检异常包括运行时异常和错误。

### 重点

```text
Throwable
 ├── Error
 └── Exception
      ├── RuntimeException
      └── 其他受检异常
```

### 必考点

```text
Exception：程序可以处理
RuntimeException：运行时异常
Error：严重错误，一般不处理
```

------

## 3. try-catch-finally【必考】

### 极简代码示例

```java
try {
    int a = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("除数不能为0");
} finally {
    System.out.println("一定执行");
}
```

### 必考点

```text
try：放可能出错的代码
catch：捕获并处理异常
finally：一般都会执行
```

PPT 中的异常处理示例说明：当 `try` 中抛出异常时，`try` 中剩余语句不执行；`finally` 一般都会执行；如果当前 `catch` 捕捉不到异常，异常会继续向外抛。

### 易错点

```java
try {
    int a = 10 / 0;
    System.out.println("hello");
}
```

`hello` 不会输出，因为前面已经抛异常。

------

## 4. throw 和 throws【必考易错】

### throw

**通俗理解：**
`throw` 是“真的把异常扔出去”。

```java
throw new ArithmeticException();
```

### throws

**通俗理解：**
`throws` 是“提前声明这个方法可能会出错”。

```java
void test() throws Exception {
    throw new Exception();
}
```

### 对比表

| 关键字 | 位置       | 作用                 |
| ------ | ---------- | -------------------- |
| throw  | 方法体里面 | 抛出一个异常对象     |
| throws | 方法声明处 | 声明方法可能抛出异常 |

### 极简代码示例

```java
static void test() throws Exception {
    throw new Exception("出错了");
}
```

------

## 5. 自定义异常

PPT 中给出了自定义异常类示例：自定义异常类继承 `Exception`，可以重写 `toString()` 方法，然后通过 `throw new 自定义异常()` 抛出。

### 极简代码示例

```java
class MyException extends Exception {
}

public class Main {
    public static void main(String[] args) {
        try {
            throw new MyException();
        } catch (MyException e) {
            System.out.println("捕获自定义异常");
        }
    }
}
```

### 易错点

自定义异常通常：

```java
class MyException extends Exception
```

不是：

```java
class MyException
```

------

# 第七章 文件与数据流【程序填空重点】

提纲要求掌握输入流、输出流的概念，认识 `InputStream`、`OutputStream`、`FileInputStream`、`FileOutputStream`、`DataInputStream`、`DataOutputStream`、`BufferedInputStream`、`BufferedOutputStream`、`RandomAccessFile`，尤其是 `RandomAccessFile` 的相关方法。

------

## 1. 文件和内存

**通俗理解：**

内存：程序运行时临时保存数据。
文件：程序结束后还能长期保存数据。

PPT 中说，文件可以长期保存大量数据，程序结束后仍能存在；内存中的变量或数组数据是临时性的。

### 极简理解

```text
文件 → 内存：输入
内存 → 文件：输出
```

------

## 2. 输入流和输出流【必考】

PPT 中说明，输入流是将数据从文件、标准输入或外部设备加载到内存；输出流是将内存中的数据保存到文件或输出设备。`InputStream` 是所有字节输入流的父类，`OutputStream` 是所有字节输出流的父类。

### 重点

```text
InputStream：字节输入流父类
OutputStream：字节输出流父类
FileInputStream：文件字节输入流
FileOutputStream：文件字节输出流
```

### 极简代码示例：读文件

```java
import java.io.*;

public class Main {
    public static void main(String[] args) throws IOException {
        FileInputStream f = new FileInputStream("test.txt");
        int b = f.read();
        f.close();
    }
}
```

### 极简代码示例：写文件

```java
import java.io.*;

public class Main {
    public static void main(String[] args) throws IOException {
        FileOutputStream f = new FileOutputStream("out.txt");
        f.write(65);
        f.close();
    }
}
```

### 易错点

`read()` 返回 `int`，如果读到文件末尾，返回 `-1`。PPT 中也说明 `InputStream.read()` 正常返回 0 到 255，遇到数据流结束返回 -1。

------

## 3. 文件读写基本步骤

PPT 中总结文件读写操作步骤：创建输入/输出流对象，进行读/写操作，最后调用 `close()` 关闭文件释放资源。

### 必背模板

```java
try {
    // 1. 创建流
    // 2. 读或写
    // 3. close关闭
} catch (IOException e) {
    e.printStackTrace();
}
```

------

## 4. BufferedInputStream / BufferedOutputStream

**通俗理解：**
带缓冲区的流，读写效率更高。

### 极简代码示例

```java
import java.io.*;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedInputStream bis =
            new BufferedInputStream(new FileInputStream("test.txt"));

        int b = bis.read();

        bis.close();
    }
}
```

### 必考点

提纲规定：

```text
BufferedInputStream：构造方法、read
BufferedOutputStream：构造方法、write
```

------

## 5. RandomAccessFile【必考】

**通俗理解：**
普通输入输出流一般按顺序读写，`RandomAccessFile` 可以跳到文件指定位置读写。

PPT 中说，`RandomAccessFile` 允许使用同一个实例对象对同一个文件交替读/写，并且可以指定读写位置；构造方法中 `mode = "r"` 表示只读，`mode = "rw"` 表示可读写。

### 极简代码示例

```java
import java.io.*;

public class Main {
    public static void main(String[] args) throws IOException {
        RandomAccessFile f = new RandomAccessFile("test.txt", "rw");

        f.writeInt(100);
        f.seek(0);
        int x = f.readInt();

        System.out.println(x);
        f.close();
    }
}
```

### 必考方法

| 方法      | 作用         |
| --------- | ------------ |
| read      | 读一个字节   |
| write     | 写一个字节   |
| readInt   | 读 int       |
| writeInt  | 写 int       |
| seek      | 移动文件指针 |
| skipBytes | 跳过若干字节 |

PPT 中列出了 `RandomAccessFile` 的 `seek`、`skipBytes`、`read`、`readInt`、`write`、`writeInt` 等常用方法，并强调文件指针以字节为单位移动。

### 易错点：字节数

PPT 中列出 `RandomAccessFile` 读取不同基本类型时的字节数，如 `readInt()` 读取 4 字节，`readDouble()` 读取 8 字节，`readChar()` 读取 2 字节。

你要记：

| 类型    | 字节数 |
| ------- | ------ |
| byte    | 1      |
| boolean | 1      |
| short   | 2      |
| char    | 2      |
| int     | 4      |
| float   | 4      |
| long    | 8      |
| double  | 8      |

### 经典例题思路

PPT 的随机访问文件例题中，先连续写入 10 个 `double`，每个 `double` 占 8 字节，然后用 `seek(16)` 移动到第 3 个 double 的位置，把它改成 0。因为第 1 个 double 起始位置是 0，第 2 个是 8，第 3 个是 16。

你要会算：

```text
第 n 个 int 的起始位置 = (n - 1) × 4
第 n 个 double 的起始位置 = (n - 1) × 8
```

------

# 最后：考前真正该抓的重点

## 第一梯队：最可能拿大分

```text
类、对象、构造方法
继承
方法重写
多态
abstract
interface
this
static
final
数组
String 方法
ArrayList / Vector
异常处理
RandomAccessFile
```

## 第二梯队：选择/填空/判断常考

```text
Java 特点
标识符规则
基本数据类型和位数
运算符短路规则
if / switch / for / while
break / continue
输入流 / 输出流概念
```

## 可以少花时间

你的提纲明确说：

```text
包不考
泛型不考
LinkedList 不考
封装性具体知识点不考
子类与父类类型转换不考
```

所以你不要被 PPT 里大量内容吓到，按提纲砍掉。

------

# 一句话知识主线

你可以这样背：

```text
Java 用类组织程序；
类创建对象；
对象有变量和方法；
构造方法负责初始化对象；
继承让子类复用父类；
重写让子类改写父类方法；
多态让父类引用指向子类对象；
abstract 和 interface 规定子类必须实现什么；
数组和集合存一组数据；
String 处理字符串；
异常处理程序出错；
文件流负责读写文件。
```

这就是你这门 Java 考试的主干。