可以。我先给你出 **2 套 100 分模拟卷**，题型严格按你提纲：单选 10 分、填空 15 分、判断 10 分、简答 10 分、程序填空 22 分、程序设计 33 分。你的提纲里明确写了这个题型和分值，并且第 3、4、5 章是重点中的重点，第 6 章异常、第 7 章文件流会考程序填空。

我没有找到可靠公开的 FAFU Java 原卷，所以这不是“真题复刻”，而是按你的 **FAFU 复习提纲 + 老师 PPT + 常见高校 Java 期末卷风格**出的应试模拟卷。公开能查到的其他学校 Java 期末复习资料普遍也集中在 Java 基础、面向对象、继承多态、抽象类接口、异常、输入输出等内容。([CSDN](https://blog.csdn.net/fancywxq/article/details/140149042?utm_source=chatgpt.com))

------

# Java 模拟试卷 A 卷

## 一、单选题：每题 1 分，共 10 分

### 1. 下列哪个是合法的 Java 标识符？

A. `3abc`
B. `class`
C. `_name`
D. `a+b`

### 2. Java 中 `int` 类型占多少位？

A. 8
B. 16
C. 32
D. 64

### 3. 下列关于构造方法的说法正确的是？

A. 构造方法必须写返回值类型
B. 构造方法名称必须和类名相同
C. 构造方法只能有一个
D. 构造方法不能有参数

### 4. 下列哪个关键字用于继承父类？

A. `implements`
B. `extends`
C. `interface`
D. `import`

### 5. 下列代码输出结果是？

```java
int a = 5;
if (a > 10 && a++ > 0) {
}
System.out.println(a);
```

A. 5
B. 6
C. 0
D. 编译错误

### 6. 下列关于 `static` 的说法正确的是？

A. static 成员属于对象
B. static 成员属于类
C. static 方法只能通过对象调用
D. static 变量每个对象都有一份独立副本

### 7. 下列哪个方法用于比较字符串内容是否相等？

A. `==`
B. `equals()`
C. `compare()`
D. `same()`

### 8. 下列哪个异常表示数组下标越界？

A. `ArithmeticException`
B. `IOException`
C. `ArrayIndexOutOfBoundsException`
D. `FileNotFoundException`

### 9. `ArrayList` 中获取元素个数的方法是？

A. `length`
B. `length()`
C. `size()`
D. `count()`

### 10. `RandomAccessFile` 中移动文件指针的方法是？

A. `move()`
B. `skip()`
C. `seek()`
D. `go()`

------

## 二、填空题：每题 3 分，共 15 分

### 1. Java 中基本数据类型共有 ______ 种。

### 2. 数组 `arr` 的长度用 ______ 表示。

### 3. 字符串 `s` 的长度用 ______ 表示。

### 4. 抽象类使用关键字 ______ 修饰。

### 5. Java 异常处理中，______ 语句块通常无论是否发生异常都会执行。

------

## 三、判断题：每题 1 分，共 10 分

### 1. Java 标识符可以以数字开头。

### 2. Java 中 `char` 类型占 16 位。

### 3. 构造方法可以写 `void` 返回值。

### 4. 子类可以继承父类的部分成员。

### 5. Java 支持一个类同时继承多个普通父类。

### 6. 抽象类不能直接创建对象。

### 7. 接口中的方法默认是 `public abstract`。

### 8. `String` 比较内容时应该使用 `equals()`。

### 9. `break` 只能跳过本次循环，不能结束循环。

### 10. `InputStream.read()` 读到文件末尾时返回 `-1`。

------

## 四、简答题：每题 5 分，共 10 分

### 1. 简述类和对象的关系。

### 2. 简述 `throw` 和 `throws` 的区别。

------

## 五、程序填空题：每空 2 分，共 22 分

### 1. 补全继承和多态程序

```java
class Animal {
    void speak() {
        System.out.println("Animal");
    }
}

class Dog ______ Animal {
    void speak() {
        System.out.println("Dog");
    }
}

public class Test {
    public static void main(String[] args) {
        Animal a = ______ Dog();
        a.______;
    }
}
```

### 2. 补全 ArrayList 程序

```java
import java.util.______;

public class TestList {
    public static void main(String[] args) {
        ArrayList list = new ArrayList();
        list.______("Java");
        list.______("Python");
        System.out.println(list.______());
        System.out.println(list.______(0));
    }
}
```

### 3. 补全异常处理程序

```java
public class TestException {
    public static void main(String[] args) {
        try {
            int a = 10 / 0;
        } ______ (ArithmeticException e) {
            System.out.println("除数不能为0");
        } ______ {
            System.out.println("程序结束");
        }
    }
}
```

### 4. 补全文件输入程序

```java
import java.io.*;

public class ReadFile {
    public static void main(String[] args) throws IOException {
        FileInputStream f = new ______("test.txt");
        int b = f.______();
        f.______();
    }
}
```

------

## 六、程序设计题：共 33 分

### 1. 设计一个 `Student` 类，包含姓名 `name` 和成绩 `score`，提供构造方法和 `show()` 方法输出学生信息。主方法中创建一个学生对象并调用 `show()`。

11 分

### 2. 设计父类 `Shape`，包含方法 `area()`；设计子类 `Circle`，重写 `area()` 方法计算圆面积。主方法中使用多态创建 `Shape s = new Circle(2);` 并输出面积。

11 分

### 3. 定义一个字符串数组，保存 `"Java"`、`"C"`、`"Python"`、`"Java"`，统计 `"Java"` 出现的次数并输出。

11 分

------

# A 卷答案与解析

## 一、单选题答案

| 题号 | 答案 | 解析                                         |
| ---- | ---- | -------------------------------------------- |
| 1    | C    | 标识符不能数字开头，不能是关键字，不能有 `+` |
| 2    | C    | `int` 占 32 位                               |
| 3    | B    | 构造方法名必须和类名相同，不能写返回值       |
| 4    | B    | 继承使用 `extends`                           |
| 5    | A    | `&&` 短路，右边 `a++` 不执行                 |
| 6    | B    | `static` 属于类，所有对象共享                |
| 7    | B    | 字符串内容比较用 `equals()`                  |
| 8    | C    | 数组越界异常                                 |
| 9    | C    | `ArrayList` 元素个数用 `size()`              |
| 10   | C    | `RandomAccessFile` 移动文件指针用 `seek()`   |

------

## 二、填空题答案

### 1. `8`

Java 基本数据类型：`byte`、`short`、`int`、`long`、`float`、`double`、`char`、`boolean`。

### 2. `arr.length`

数组长度是属性，没有括号。

### 3. `s.length()`

字符串长度是方法，有括号。

### 4. `abstract`

抽象类：

```java
abstract class A {
}
```

### 5. `finally`

`finally` 通常都会执行。

------

## 三、判断题答案

| 题号 | 答案 | 解析                           |
| ---- | ---- | ------------------------------ |
| 1    | 错   | 标识符不能数字开头             |
| 2    | 对   | `char` 占 16 位                |
| 3    | 错   | 构造方法不能写 `void`          |
| 4    | 对   | 子类可以继承父类成员           |
| 5    | 错   | Java 普通类只能单继承          |
| 6    | 对   | 抽象类不能直接 `new`           |
| 7    | 对   | 接口方法默认 `public abstract` |
| 8    | 对   | 字符串内容比较用 `equals()`    |
| 9    | 错   | `break` 是结束整个循环         |
| 10   | 对   | 文件末尾返回 `-1`              |

------

## 四、简答题答案

### 1. 类和对象的关系

类是对象的模板，对象是类的具体实例。
类描述一类事物共同具有的属性和行为，对象是根据类创建出来的具体个体。

例如：

```java
class Student {
    String name;
    int age;
}

Student s = new Student();
```

其中 `Student` 是类，`s` 指向的就是 `Student` 类的对象。

------

### 2. `throw` 和 `throws` 的区别

`throw` 用在方法体内部，表示真正抛出一个异常对象。

```java
throw new Exception("出错了");
```

`throws` 用在方法声明处，表示这个方法可能抛出异常。

```java
void test() throws Exception {
}
```

简单记：

```text
throw：方法体内，抛出异常
throws：方法声明处，声明异常
```

------

## 五、程序填空题答案

### 1.

```java
class Dog extends Animal {
Animal a = new Dog();
a.speak();
```

完整程序：

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

public class Test {
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

解析：父类引用指向子类对象，调用被重写的方法，运行时看右边真实对象。

------

### 2.

```java
import java.util.ArrayList;
list.add("Java");
list.add("Python");
list.size()
list.get(0)
```

完整程序：

```java
import java.util.ArrayList;

public class TestList {
    public static void main(String[] args) {
        ArrayList list = new ArrayList();
        list.add("Java");
        list.add("Python");
        System.out.println(list.size());
        System.out.println(list.get(0));
    }
}
```

输出：

```text
2
Java
```

------

### 3.

```java
catch
finally
```

完整程序：

```java
public class TestException {
    public static void main(String[] args) {
        try {
            int a = 10 / 0;
        } catch (ArithmeticException e) {
            System.out.println("除数不能为0");
        } finally {
            System.out.println("程序结束");
        }
    }
}
```

输出：

```text
除数不能为0
程序结束
```

------

### 4.

```java
FileInputStream
read
close
```

完整程序：

```java
import java.io.*;

public class ReadFile {
    public static void main(String[] args) throws IOException {
        FileInputStream f = new FileInputStream("test.txt");
        int b = f.read();
        f.close();
    }
}
```

------

## 六、程序设计题参考答案

### 1. Student 类

```java
class Student {
    String name;
    double score;

    Student(String name, double score) {
        this.name = name;
        this.score = score;
    }

    void show() {
        System.out.println("姓名：" + name);
        System.out.println("成绩：" + score);
    }
}

public class Main {
    public static void main(String[] args) {
        Student s = new Student("Tom", 90);
        s.show();
    }
}
```

评分点：

```text
定义 Student 类：2 分
定义 name 和 score：2 分
构造方法正确：3 分
show 方法正确：2 分
main 中创建对象并调用：2 分
```

------

### 2. 继承和多态

```java
class Shape {
    double area() {
        return 0;
    }
}

class Circle extends Shape {
    double r;

    Circle(double r) {
        this.r = r;
    }

    double area() {
        return 3.14 * r * r;
    }
}

public class Main {
    public static void main(String[] args) {
        Shape s = new Circle(2);
        System.out.println(s.area());
    }
}
```

输出：

```text
12.56
```

评分点：

```text
定义父类 Shape：2 分
定义子类 Circle 并继承：2 分
构造方法正确：2 分
重写 area 方法：3 分
使用多态创建对象并输出：2 分
```

------

### 3. 字符串数组统计

```java
public class Main {
    public static void main(String[] args) {
        String[] arr = {"Java", "C", "Python", "Java"};
        int count = 0;

        for (int i = 0; i < arr.length; i++) {
            if (arr[i].equals("Java")) {
                count++;
            }
        }

        System.out.println(count);
    }
}
```

输出：

```text
2
```

评分点：

```text
定义字符串数组：2 分
定义计数变量：2 分
正确遍历数组：3 分
使用 equals 比较字符串：3 分
正确输出结果：1 分
```

------

# Java 模拟试卷 B 卷

## 一、单选题：每题 1 分，共 10 分

### 1. 下列哪个不是 Java 基本数据类型？

A. `int`
B. `double`
C. `String`
D. `boolean`

### 2. 下列关于数组的说法错误的是？

A. 数组下标从 0 开始
B. 数组创建后长度固定
C. 数组长度用 `length()` 获取
D. 数组元素类型必须一致

### 3. 下列代码输出结果是？

```java
System.out.println(5 / 2);
```

A. 2
B. 2.5
C. 3
D. 编译错误

### 4. 下列哪个关键字用于实现接口？

A. `extends`
B. `implements`
C. `interface`
D. `abstract`

### 5. 下列关于 `final` 的说法错误的是？

A. final 变量不能再次赋值
B. final 方法不能被重写
C. final 类不能被继承
D. final 类必须是抽象类

### 6. 下列哪个是抽象方法的正确写法？

A. `abstract void show();`
B. `abstract void show(){}`
C. `void abstract show();`
D. `abstract show();`

### 7. `String s = "abcdef"; s.substring(1, 4)` 的结果是？

A. `abc`
B. `bcd`
C. `bcde`
D. `cde`

### 8. 下列哪个关键字用于捕获异常？

A. `try`
B. `catch`
C. `throw`
D. `throws`

### 9. `FileOutputStream("out.txt", true)` 中 `true` 表示？

A. 覆盖原文件
B. 追加到文件末尾
C. 只读文件
D. 删除文件

### 10. 下列哪个方法用于向 `ArrayList` 中添加元素？

A. `put()`
B. `insert()`
C. `add()`
D. `append()`

------

## 二、填空题：每题 3 分，共 15 分

### 1. Java 中继承父类使用关键字 ______。

### 2. 实现接口使用关键字 ______。

### 3. 创建对象使用关键字 ______。

### 4. `ArrayList` 中获取指定下标元素的方法是 ______。

### 5. `RandomAccessFile` 中读取一个 `int` 类型数据的方法是 ______。

------

## 三、判断题：每题 1 分，共 10 分

### 1. `String` 是基本数据类型。

### 2. `do-while` 循环至少执行一次。

### 3. `continue` 表示结束整个循环。

### 4. 抽象方法可以有方法体。

### 5. 一个类可以实现多个接口。

### 6. `this` 表示当前对象。

### 7. `static` 变量所有对象共享。

### 8. 局部变量可以不初始化就使用。

### 9. `catch` 可以有多个。

### 10. 文件输出流可以把内存中的数据写入文件。

------

## 四、简答题：每题 5 分，共 10 分

### 1. 简述继承和多态的含义。

### 2. 简述输入流和输出流的区别。

------

## 五、程序填空题：每空 2 分，共 22 分

### 1. 补全抽象类程序

```java
abstract class Shape {
    abstract double ______();
}

class Rectangle ______ Shape {
    double width;
    double height;

    Rectangle(double width, double height) {
        this.width = width;
        this.height = height;
    }

    double area() {
        return width * height;
    }
}
```

### 2. 补全接口程序

```java
interface Speakable {
    void speak();
}

class Student ______ Speakable {
    public void ______() {
        System.out.println("Student speak");
    }
}
```

### 3. 补全字符串程序

```java
public class TestString {
    public static void main(String[] args) {
        String s = "  Java Study  ";
        s = s.______();
        System.out.println(s.______());
        System.out.println(s.______(0));
        System.out.println(s.______("Study"));
    }
}
```

### 4. 补全 RandomAccessFile 程序

```java
import java.io.*;

public class TestRAF {
    public static void main(String[] args) throws IOException {
        RandomAccessFile f = new ______("test.dat", "rw");
        f.______(100);
        f.______(0);
        int x = f.______();
        f.close();
    }
}
```

------

## 六、程序设计题：共 33 分

### 1. 定义一个 `Book` 类，包含书名 `name` 和价格 `price`，使用构造方法初始化，定义 `show()` 方法输出信息。主方法创建对象并输出。

11 分

### 2. 定义接口 `Flyable`，包含方法 `fly()`；定义类 `Bird` 实现接口，并在 `fly()` 中输出 `"Bird can fly"`。主方法中创建对象并调用方法。

11 分

### 3. 使用 `ArrayList` 保存 `"Tom"`、`"Jack"`、`"Lucy"`，输出集合大小和第 2 个元素，然后把第 2 个元素修改为 `"Rose"`，再次输出。

11 分

------

# B 卷答案与解析

## 一、单选题答案

| 题号 | 答案 | 解析                                         |
| ---- | ---- | -------------------------------------------- |
| 1    | C    | `String` 是引用数据类型                      |
| 2    | C    | 数组长度是 `length`，不是 `length()`         |
| 3    | A    | 两个整数相除结果仍是整数                     |
| 4    | B    | 类实现接口用 `implements`                    |
| 5    | D    | final 类不能被继承，和 abstract 没有必然关系 |
| 6    | A    | 抽象方法没有方法体                           |
| 7    | B    | `substring(1,4)` 取下标 1 到 3               |
| 8    | B    | `catch` 用于捕获异常                         |
| 9    | B    | `append=true` 表示追加                       |
| 10   | C    | `ArrayList.add()` 添加元素                   |

------

## 二、填空题答案

### 1. `extends`

```java
class Dog extends Animal {
}
```

### 2. `implements`

```java
class Bird implements Flyable {
}
```

### 3. `new`

```java
Student s = new Student();
```

### 4. `get`

```java
list.get(0);
```

### 5. `readInt`

```java
int x = f.readInt();
```

------

## 三、判断题答案

| 题号 | 答案 | 解析                                      |
| ---- | ---- | ----------------------------------------- |
| 1    | 错   | `String` 是引用数据类型                   |
| 2    | 对   | `do-while` 先执行再判断                   |
| 3    | 错   | `continue` 跳过本次循环，`break` 结束循环 |
| 4    | 错   | 抽象方法不能有方法体                      |
| 5    | 对   | 一个类可以实现多个接口                    |
| 6    | 对   | `this` 表示当前对象                       |
| 7    | 对   | `static` 属于类，所有对象共享             |
| 8    | 错   | 局部变量必须初始化才能使用                |
| 9    | 对   | 可以有多个 `catch`                        |
| 10   | 对   | 输出流用于把数据写出                      |

------

## 四、简答题答案

### 1. 继承和多态

继承是指子类通过 `extends` 继承父类的属性和方法，从而复用父类代码。

```java
class Dog extends Animal {
}
```

多态是指父类引用可以指向子类对象，调用被子类重写的方法时，执行的是子类版本。

```java
Animal a = new Dog();
a.speak();
```

口诀：

```text
继承：子类拥有父类内容
多态：父类引用指向子类对象
```

------

### 2. 输入流和输出流的区别

输入流是把文件、键盘或外部设备中的数据读入程序内存。

```java
FileInputStream f = new FileInputStream("test.txt");
```

输出流是把程序内存中的数据写到文件或外部设备。

```java
FileOutputStream f = new FileOutputStream("out.txt");
```

简单记：

```text
输入流：外部 → 程序
输出流：程序 → 外部
```

------

## 五、程序填空题答案

### 1. 抽象类

```java
area
extends
```

完整程序：

```java
abstract class Shape {
    abstract double area();
}

class Rectangle extends Shape {
    double width;
    double height;

    Rectangle(double width, double height) {
        this.width = width;
        this.height = height;
    }

    double area() {
        return width * height;
    }
}
```

------

### 2. 接口

```java
implements
speak
```

完整程序：

```java
interface Speakable {
    void speak();
}

class Student implements Speakable {
    public void speak() {
        System.out.println("Student speak");
    }
}
```

注意：实现接口方法时必须写 `public`。

------

### 3. 字符串

```java
trim
length
charAt
indexOf
```

完整程序：

```java
public class TestString {
    public static void main(String[] args) {
        String s = "  Java Study  ";
        s = s.trim();
        System.out.println(s.length());
        System.out.println(s.charAt(0));
        System.out.println(s.indexOf("Study"));
    }
}
```

输出：

```text
10
J
5
```

解析：`trim()` 去掉前后空格后字符串是 `"Java Study"`，长度为 10。

------

### 4. RandomAccessFile

```java
RandomAccessFile
writeInt
seek
readInt
```

完整程序：

```java
import java.io.*;

public class TestRAF {
    public static void main(String[] args) throws IOException {
        RandomAccessFile f = new RandomAccessFile("test.dat", "rw");
        f.writeInt(100);
        f.seek(0);
        int x = f.readInt();
        f.close();
    }
}
```

解析：`writeInt(100)` 写入 4 个字节，`seek(0)` 回到文件开头，`readInt()` 读出刚写入的整数。

------

## 六、程序设计题参考答案

### 1. Book 类

```java
class Book {
    String name;
    double price;

    Book(String name, double price) {
        this.name = name;
        this.price = price;
    }

    void show() {
        System.out.println("书名：" + name);
        System.out.println("价格：" + price);
    }
}

public class Main {
    public static void main(String[] args) {
        Book b = new Book("Java程序设计", 59.8);
        b.show();
    }
}
```

评分点：

```text
定义 Book 类：2 分
定义 name 和 price：2 分
构造方法初始化：3 分
show 方法输出：2 分
main 中创建对象调用方法：2 分
```

------

### 2. 接口 Flyable

```java
interface Flyable {
    void fly();
}

class Bird implements Flyable {
    public void fly() {
        System.out.println("Bird can fly");
    }
}

public class Main {
    public static void main(String[] args) {
        Bird b = new Bird();
        b.fly();
    }
}
```

评分点：

```text
定义接口 Flyable：3 分
定义 fly 方法：2 分
Bird 实现接口：2 分
正确重写 fly 方法：2 分
main 中创建对象并调用：2 分
```

------

### 3. ArrayList 程序

```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList list = new ArrayList();

        list.add("Tom");
        list.add("Jack");
        list.add("Lucy");

        System.out.println(list.size());
        System.out.println(list.get(1));

        list.set(1, "Rose");

        System.out.println(list.get(1));
    }
}
```

输出：

```text
3
Jack
Rose
```

评分点：

```text
导入 ArrayList：1 分
创建集合对象：2 分
正确 add 三个元素：2 分
输出 size 和 get(1)：3 分
正确使用 set 修改：2 分
再次输出：1 分
```

------

# 你现在怎么用这两套卷

第一遍不要直接看答案，先做 A 卷，限时 90 分钟。
第二遍对答案，把错题对应回 PPT 页数。
第三遍做 B 卷，重点看程序填空和程序设计题。

最关键的提分点是这些：

```text
1. 构造方法别写 void
2. 字符串比较用 equals
3. 数组 length 没括号，字符串 length() 有括号
4. 继承 extends，接口 implements
5. 抽象方法没有方法体
6. 接口方法实现时要 public
7. 多态：父类引用 = new 子类对象
8. try-catch-finally 结构必须会补
9. throw 和 throws 区分
10. FileInputStream / FileOutputStream / RandomAccessFile 模板要背
```