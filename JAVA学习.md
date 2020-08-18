# JAVA学习

##### 待补充知识

![image-20200727114845083](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200727114845083.png)



推荐书籍：

《高性能MySQL》

for-each循环：for(int i : index)的意思就是说，遍历index数组，每次遍历的对象用i 这个对象去接收。
相当于：
int i=0; //用于接收index数组中的某一个对象
for(int j = 0;j<index.length;j++){
        i = index[j];
    }

foreach的语句格式：
for(元素类型t 元素变量x : 遍历对象obj){
引用了x的java语句;
}



时间复杂度o（logn^n^）

索引下推

最左匹配

覆盖索引

倒排索引

es（ElasticSearch）全文检索

##### 数据库优化：

看官网，学习优化

RBO（Rule-Based Optimization ）基于规则优化

CBO（Cost-Based Optimization）基于成本优化

wal：write ahead log 预写日志

MySQL的复制延迟是一直被诟病的问题之一，在MySQL 5.7版本已经支持“真正”的并行复制功能，官方称为为enhanced multi-threaded slave（简称MTS），因此复制延迟问题已经得到了极大的改进。总之，MySQL 5.7版本后，复制延迟问题永不存在。



MyCat  ：



Linux安装软件

​	1、编译

​	2、RPM：RedHat Package Management

3、yum:Yum(全称为 Yellow dogUpdater, Modified)是一个在Fedora和RedHat以及CentOS中的Shell前端软件包管理器。基于RPM包管理，能够从指定的服务器自动下载RPM包并且安装，可以自动处理依赖性关系，并且一次安装所有依赖的软件包，无须繁琐地一次次下载、安装。



ASM（assemble	汇编） 是一个 Java 字节码操控框架。它能被用来动态生成类或者增强既有类的功能。ASM 可以直接产生二进制 class 文件，也可以在类被加载入 Java 虚拟机之前动态改变类行为。Java class 被存储在严格格式定义的 .class 文件里，这些类文件拥有足够的元数据来解析类中的所有元素：类名称、方法、属性以及 Java 字节码（指令）。ASM 从类文件中读入信息后，能够改变类行为，分析类信息，甚至能够根据用户要求生成新类。说白了asm是直接通过字节码来修改class文件。



匿名内部类

红黑树

多个线程如何抢占同一个资源的，代码中的输出结果不理解？

什么叫原子操作

sql注入

#### Apache Calcite简介

Apache Calcite是一款开源SQL解析工具, 可以将各种SQL语句解析成抽象语法术AST(Abstract Syntax Tree), 之后通过操作AST就可以把SQL中所要表达的算法与关系体现在具体代码之中。

###### 主要功能

- SQL 解析
- SQL 校验
- 查询优化
- SQL 生成器
- 数据连接



### 专业名词

```
volatile   不稳定的；易变的
release  发行
Radix  基数
jdk  java开发工具
JRE  Java运行环境
OOP,Object Oriented Programming 面向对象编程
concurrent 并发的；并存的
encapsulation 封装
polymorphism 多态
inheritance 继承
override   覆盖/重写
native   本地
iterator 迭代器，循环
ceil     向上取整
floor    向下取整
enumerate  枚举
scheduled  可调度的
cas     compare and swap
abort    中止
grant    同意；授权
deprecated 过时的；已被弃用的
RDD：  弹性分布式数据集 (Resilient Distributed DataSet)
E-R图也称实体-联系图(Entity Relationship Diagram)
replication 副本
proxy 代理
dispatcher 调度员
XML 指可扩展标记语言(eXtensible Markup Language)
EJB Enterprise Java Bean
PO Persistent object
VO Value Object
SSH struts+spring+hibernate SSH框架，从职责上分为四层：表示层、业务逻辑层、数据持久层和域模块层，帮助开发人员在短期内搭建结构清晰、可复用性好、维护方便的Web应用程序
SSM Spring+SpringMVC+MyBatis 框架集由Spring、MyBatis两个开源框架整合而成（SpringMVC是Spring中的部分内容）
DI Dependency Injection，即“依赖注入”
hierarchical 等级制度的
scope 范围
prototype 原型
xmlns xml name space xml命名空间
attribute 属性
properties 属性
qualifier 限定符
POM Project Object Model项目对象模型
```



##### java既是编译型语言，也是解释型语言：

​			java编译成.class，再解释成机器语言

注意：
	1、java文件的名称必须和public class的名称包是一致
	2、一个java文件可以包含多个class，凡是public class只能有一个

##### 命名规定：

​	1、标识符必须是字母、下划线货这$符号开头
​	2、其它字母、数字、下划线或$，但不能是特殊符号
​	3、标识符大小写敏感，不可以是java关键字

常规建议：
	1、驼峰标识：接口名称在命名时要首字母大写
	2、方法，变量名的时候首字母要小写
	3、多个单词拼接表示一个表示负的时候，小驼峰命名法
	4、见名知义

##### 运算符

instanceof

![image-20200715230554645](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715230554645.png)

&&，||，！：逻辑运算符一般两边不是具体值而是表达式

​		&&：短路与，两边表达式从左开始对比，如果左边是						false，右边不再判断

​		||：短路或，同上

&，|，^,~,>>,<<,>>>:位运算符，只能操作数值，操作时会转成				二进制进行运算

​		&：与位运算，两边都参与运算

​		|：或位运算，两边都运算

​		<<:2变成8最快的方法：2<<3,左移乘2，右移除2

​		条件运算或三目运算符：（3>2?3:2）表达式为true，则返回？后的结果，若为false，则返回：后的结果

##### switch分支特点

![image-20200714141420425](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200714141420425.png)

![image-20200714143729510](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200714143729510.png)

i++步进器

##### break和continue

break用亍强行退出循环，丌执行循环中剩余的诧句。(break诧句还可用亍多支诧句switch中)，多层循环时，只能跳出内层循环，无法跳出外层循环。

continue 诧句用在循环诧句体中，用亍终止**某次**循环过程，即跳过循环体中尚未执行的诧句，接着迚行下一次是否执行循环的判定。

return两个用途：

1. 返回方法的返回值到调用处
2. 终止当前方法



##### 递归

什么是递归（recursion），尽量少用，比较消耗资源
–程序调用自身的编程技巧称为递归。
–一个过程或函数在其定义或说明中有直接或间接调用自身的一种方法

递归问题的特点
–一个问题可被分解为若干层简单的子问题
–子问题和其上层问题的解决方案一致
–外层问题的解决依赖亍子问题的解决



##### 数组

▪ 数组是相同类型数据的有序集合.
– 相同类型的若干个数据,按照一定先后次序排列组合而成。
– 其中,每一个数据称作一个数组元素
– 每个数组元素可以通过一个下标来访问它们.
▪ 数组特点:
– 其长度是确定的。数组一旦被创建，它的大小就是不可以改变的。
– 其元素必须是相同类型,不允许出现混合类型。
– 数组中的元素可以是任何数据类型，包括基本类型和引用类型。
▪ 数组属引用类型
– length, elements of the array

![image-20200714171523155](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200714171523155.png)

![image-20200714172422565](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200714172422565.png)

二维数组定义

![image-20200714210410236](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200714210410236.png)

![image-20200714210624983](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200714210624983.png)



**声明一个变量就是在内存空间划出一块合适的空间**
**声明一个数组就是在内存空间划出一串连续的空间**





##### 栈和堆

常量池在1.7之后放置在了堆空间里 

![image-20200716163645021](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200716163645021.png)

栈：存放局部变量，先进后出，自下而上存储，方法执行完毕自动释放空间

堆：存放new出来的对象和成员变量，要垃圾回收器来回收：System.gc()

方法区：存放类的信息（代码），static变量，字符串常量







##### 排序算法

数据结构：

​	线性表

​	非线性表

​	树

​	图

​	队列

​	栈



面试需求：

1. 写出某种排序算法

   冒泡排序

   选择排序

   插入排序

   快速排序

2. 排序算法的时间复杂度（空间复杂度）

   衡量一个算法是否合适的标准

3. 排序算法的稳定性

   排序先后值的位置是否发生变化



## 类

创建一个类：

​		1、属性

​		2、构造方法：无参构造方法：new实例时，无参数；带参构造方法：new实例，带参数（即可以给属性赋初始值）；

​		3、set/get方法：new完实例后，set用于给属性赋值，get用于获取属性值（**当类有私有属性时，需要此方法，供其它类调用**）

​		4、普通方法



### 内部类

#### 内部类定义

内部类可以访问外部类的私有属性

![image-20200716101153204](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200716101153204.png)

![image-20200716101123172](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200716101123172.png)



#### 成员内部类

在一个类的方法外部的

1、创建成员内部类

![image-20200807004724789](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200807004724789.png)

#### 局部内部类

**定义在方法内部的类就是局部内部类**：

1、创建局部内部类

![image-20200807002934120](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200807002934120.png)

![image-20200807002906685](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200807002906685.png)

2、调用局部内部类

![image-20200807002948536](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200807002948536.png)





![image-20200716103539989](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200716103539989.png)





###### 匿名内部类

1、一个普通类实现了一个接口：

![image-20200807000334709](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200807000334709.png)

![image-20200807000640969](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200807000640969.png)

​	2、局部内部类中的匿名内部类（Anonymous）：匿名内部类就不用new实现类的实例，改为实现的接口的名字，里面的方法体和实现类完全一样，｛｝里面的内容才叫匿名内部类（它在main方法的内部）

![image-20200807001145756](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200807001145756.png)

![image-20200716102346192](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200716102346192.png)



#### 类对象

![image-20200803173751980](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803173751980.png)



##### 字符串比较

== 比较的是地址

equals  比较的值





##### 变量

在类加载或对象创建时，会根据变量的数据类型分配相应存储空间，用于存放数据，就是变量值；

局部变量：定义在方法中的变量

​	作用域：从定义的位置的开始到整个方法结束

成员变量：定义在方法外，类内的变量叫成员变量（全局变量）

​	作用域：整个类体内

静态（static）变量：被所有对象共享，公共变量，一般使用类来调用，在创建对象之前，会被初始化

![image-20200715135823920](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715135823920.png)



内存存放位置：局部变量放在栈中，成员变量放在堆中

注意：局部变量无默认值，要是使用必须赋予初始值成员变量有初始值





super代表直接父类对象的引用

this代表当前对象的引用

this用法：

​	1、构造方法的参数与类的成员变量名称一样时，使用this代替当前对象

​	2、普通方法中：多个普通方法之间要调用时，可以用this，指当前对象的其它方法

​	3、成员变量中使用：当方法中的参数名称与成员变量一致时，使用 this.变量名称  表示对象的值

​	注意：

​			当构造方法中要调用其它构造方法时，可以只用this（）调用其它构造方法，但必须放在第一行



##### 数据类型

基本数据类型：数值型（整数型，浮点型），字符型，布尔型

引用类型：除基本数据类型外都为引用类型，类，接口，数组



参数传递是值传递



## 面向对象（OOP）

对于具有相同属性的，看作一类

类抽象除对象间的共有属性，具有这些属性的对象就是这类的一个实例

java只有方法，没有函数



### 封装

狭义封装

![image-20200715170222000](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715170222000.png)

广义封装

​	![image-20200715170408134](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715170408134.png)

### static关键字

▪使用static声明的成员变量称为静态变量，
▪使用static声明的方法称为静态方法
▪静态变量不静态方法又称为类变量和类方法



static
–static变量：只有一份，属于类，可以类名. Static变量
–static方法: 类名. Static方法，丌能出现this和super
–static代码块：只执行一次，最早执行的（类第一次调用）



在类中，用static声明的成员变量为静态成员变量 ,戒者叫做： 类属性，类变量.
它为该类的公用变量，属于类，被该类的所有实例共享，在类被载入时被显式初始化，
对于该类的所有对象来说，static成员变量只有一份。被该类的所有对象共享！！
可以使用”对象.类属性”来调用。不过，一般都是用“类名.类属性”
static变量置于方法区中！
用static声明的方法为静态方法
不需要对象，就可以调用(类名.方法名)
在调用该方法时，不会将对象的引用传递给它，所以在static方法中不可访问非static的成员。
静态方法不能以任何方式引用this和super关键字

![image-20200806131041619](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200806131041619.png)



#### 代码块

静态代码块：在创建完实例后，先于构造方法执行，并且只执行一次

![image-20200715150139554](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715150139554.png)

![image-20200715150232151](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715150232151.png)









##### 访问权限

​	public ：公共的，项目访问权限

​	protected：同一个类和包中访问

​	default：默认权限，当前类和当前包访问

​	private：私有权限，只能当前类访问

![image-20200721135712192](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721135712192.png)



成员（成员变量戒成员方法）访问权限共有四种：
–public 公共的
▪可以被项目中所有的类访问。(项目可见性)
–protected 受保护的
▪可以被这个类本身访问；同一个包中的所有其他的类访问；被它的子类（同一个包以及丌同包中的子类）访问
–default／friendly 默认的/友好的（包可见性）
▪被这个类本身访问；被同一个包中的类访问。
–private 私有的
▪只能被这个类本身访问。（类可见性）

​	类的访问权限只有两种
–public 公共的
▪可被同一项目中所有的类访问。 (必须不文件名同名)
–default／friendly 默认的/友好的
▪可被同一个包中的类访问。





### 继承（java是单继承）

![image-20200715184004320](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715184004320.png)

![image-20200715193453373](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715193453373.png)

![image-20200715193730001](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715193730001.png)



##### 重写

1、重写表示子类覆盖父类的方法，覆盖后会优先调用子类的方法

2、重写的方法名称，返回值类型，参数列表必须和父类也一致，

3、子类重写的权限不能低于父类的权限



##### 抽象类



![image-20200715202715417](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715202715417.png)

##### 创建抽象类及抽象方法

![image-20200803201829897](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803201829897.png)

创建一个子类并继承父类

![image-20200803201956969](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803201956969.png)



![image-20200803201259014](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803201259014.png)

![image-20200715211839574](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715211839574.png)





### 多态（polymorphic）

多态目的：提高代码的可扩展性和维护性；方便代码逻辑的编写

![image-20200715224312918](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715224312918.png)

![image-20200715224908820](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715224908820.png)



###### 多态应用

​	1、使用父类作为方法形参实现多态，使方法参数的类型更为宽泛；

​	2、使用父类方法作为返回值实现多态，使方法可以返回不同子类对象；



多态三要素：

![](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715223931657.png)

![image-20200715234003912](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200715234003912.png)



​	父类引用，指向子类对象

![image-20200803215624069](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803215624069.png)

访问成员变量

![image-20200803220142806](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803220142806.png)







### 接口

特征：

​	1、接口中所有方法都是抽象方法，不能包含方法实现

​	2、接口中所有方法的访问修饰权限都是public，可以不写

​	3、接口不能被实例化

​	4、接口的子类必须实现接口中的所有方法，抽象类的方法必须被子类实现

​	5、子类可以实现多个接口

​	6、接口中的变量都是静态常量（编译时会自动加static和final关键字）

#### 接口声明

![image-20200803180223733](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803180223733.png)

![image-20200803180415218](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803180415218.png)

#### 接口的使用

接口的实现类

![image-20200803180727209](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803180727209.png)

接口创建一个变量，创建的实现类实例赋值给这个变量

![image-20200803180946465](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803180946465.png)



案例

![image-20200803200116091](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803200116091.png)







###### 接口抽象方法

如果子类没有完全实现接口的所有方法，那么子类必须加abstract关键字，变为抽象类，或者未实现的方法加default关键字(默认方法)

抽象方法所在的类必须是抽象类

![image-20200803210053659](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803210053659.png)





###### 接口默认方法

​	java 8开始，接口允许定义默认方法

![image-20200803210927228](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803210927228.png)



###### 接口静态方法

java 8开始，接口允许定义静态方法

接口静态方法：实现类共享改接口的方法，并且该方法只与接口相关，而与实现类无关。

接口静态方法创建

![image-20200803211627611](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803211627611.png)

接口静态方法实现

​			没有抽象方法，所以无需重写

![image-20200803211743337](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803211743337.png)



接口静态方法使用

![image-20200803210053659](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803210053659.png)



###### 接口私有方法

​		java 9开始，允许接口定义私有方法

​		接口普通私有方法

![image-20200803213011509](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803213011509.png)

![image-20200803212823820](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803212823820.png)



​		接口静态私有方法

![image-20200803213251990](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803213251990.png)



接口静态私有方法调用

![image-20200803213345402](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803213345402.png)





#### 接口和抽象类的区别

![image-20200716095455050](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200716095455050.png)

![image-20200803195735761](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803195735761.png)



##### 异常处理机制

![image-20200716111038005](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200716111038005.png)



finally

![image-20200716113952763](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200716113952763.png)



##### 包装类

包装类是将基本数据类型封装成一个类，包含属性和方法

使用：

​	使用中，会在涉及到自动装箱和自动拆箱

​			1、装箱：基本数据类型转换成包装类，Integer.valueOf()

​			2、拆箱：包装类转换成基本数据类型，i.intValue()

![image-20200716152128680](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200716152128680.png)



##### 可变字符串

StringBuffer：线程安全（synchronize），效率低

Stringbuilder：线程不安全，效率高







##### 日期转换

![image-20200717092900514](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717092900514.png)

设置时间

![image-20200717093341616](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717093341616.png)

### Java集合框架

![image-20200717154239496](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717154239496.png)

##### List接口

![image-20200717163108187](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717163108187.png)

vector

![image-20200717170134407](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717170134407.png)





​	![image-20200717153204282](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717153204282.png)

![image-20200717153608160](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717153608160.png)

##### iteractor：迭代器，增强for循环

![image-20200717171016965](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717171016965.png)

![image-20200717171234087](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717171234087.png)

![image-20200717193148573](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717193148573.png)

![image-20200717170956913](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717170956913.png)

![image-20200717170531457](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717170531457.png)





##### Hash表原理

![image-20200717194729652](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717194729652.png)



Hashset

​	for循环比较好

![image-20200717195112430](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717195112430.png)

##### Map

hashmap跟hashtable的区别：

1、hashmap线程不安全，效率比较高，hashtable线程安全，效率低

2、hashmap中key和value都可以为空,hashtable不允许为空
 ![image-20200718103547137](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718103547137.png)

![image-20200718110715651](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718110715651.png)

hash碰撞

扰动函数，防止hash碰撞

hashmap源码



##### 树

TreeSet，TreeMap，二叉平衡树，AVL树，红黑树实现（特殊的平衡树），

![image-20200717201139456](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717201139456.png)

![image-20200717201754563](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717201754563.png)



1、set中存放的是无序，唯一的数据

2、set不可以通过下标获取对应位置的元素的值，因为无序的特点

3、使用treeset底层的实现是treemap,利用红黑树来进行实现

4、设置元素的时候，如果是自定义对象，会查找对象中的equals和hashcode的方法，如果没有，比较的是地址

5、树中的元素是要默认进行排序操作的，如果是基本数据类型，自动比较，如果是引用类型的话，需要自定义比较器

### 比较器分类

#### 内部比较器

定义在元素的类中，通过实现comparable接口来进行实现

#### 外部比较器

定义在当前类中，通过实现comparator接口来实现，但是要将该比较器传递到集合中

注意：外部比较器可以定义成一个工具类，此时所有需要比较的规则如果一致的话，可以复用，而

内部比较器只有在存储当前对象的时候才可以使用

如果两者同时存在，使用外部比较器

当使用比较器的时候，不会调用equals方法



#### 泛型

**参数化类型**：把类型当作参数传递，是一种引用类型

泛型不能实例化

当做一些集合的统一操作时，需要保证集合的类是统一的，此时就需要泛型来限制

给集合的元素设置相同的数据类型，就是泛型的基本要求

泛型优点：

​	1、提高代码重用性

​	2、防止类型转换异常，提高代码安全性

使用：

​	在创建对象时，在<>设置合理的类型来实现







![image-20200717214208919](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200717214208919.png)



泛型的高阶应用：

1、泛型类

在定义类的时候在类名的后面添加<E,K,V,A,B>,起到占位的作用，类中的方法的返回值类型和属性的类型都可以使用

![image-20200725000940340](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725000940340.png)

![image-20200725001433967](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725001433967.png)



2、泛型接口

在定义接口的时候，在接口的名称后添加<E,K,V,A,B>,

1、子类在进行实现的时候，可以不填写泛型的类型，此时在创建具体的子类对象的时候才决定使用什么类型

2、子类在实现泛型接口的时候，只在实现父类的接口的时候指定父类的泛型类型即可，此时，测试方法中的泛型类型必须要跟子类保持一致

![image-20200725001824661](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725001824661.png)

![image-20200725002324014](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725002324014.png)

![image-20200725002141630](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725002141630.png)

![image-20200725002115962](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725002115962.png)



3、泛型方法

在定义方法的时候，指定方法的返回值和参数是自定义的占位符，可以是类名中的T,也可以是自定义的Q，只不过在使用Q的时候需要使用< Q >定义在返回值的前面

![image-20200725002611114](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725002611114.png)

法二

![image-20200725002859399](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725002859399.png)

![image-20200725002829321](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725002829321.png)



4、泛型的上限（工作中不用）

如果父类确定了，所有的子类都可以直接使用

5、泛型的下限（工作中不用）

如果子类确定了，子类的所有父类都可以直接传递参数使用



泛型集合

![image-20200725003613874](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725003613874.png)



##### Collections工具类

Collections和Collection不同，前者是集合的操作类，后者是集合接口
Collections提供的静态方法
addAll():批量添加
sort():排序
binarySearch()：二分查找，要先排序
fill()：替换
shuffle():随机排序
reverse():逆序



##### IO



![image-20200718224557020](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718224557020.png)

![image-20200718224836975](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718224836975.png)





![image-20200718143752773](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718143752773.png)



![image-20200718144905922](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718144905922.png)

![image-20200718145426707](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718145426707.png)

输入输出流

![image-20200718152204369](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718152204369.png)



##### 字节流和字符流分类

![image-20200718152234807](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718152234807.png)

遍历文件

![image-20200718155237901](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718155237901.png)

传图片用字节流

字符流更快，效率更高



一行一行地读取数据

![image-20200718215825691](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718215825691.png)

遍历，行读取

![image-20200718215949184](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718215949184.png)



把输入输出写在try（）里，可以不用关闭io流

![image-20200718221046966](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200718221046966.png)



##### 死锁

两个线程各占一份资源，且都需要对方资源，而双方都不愿让步，就形成死锁

##### run()方法和start()方法的区别？

　通常，系统通过调用线程类的start()方法来启动一个线程，此时该线程处于就绪状态，而非运行状态，也就意味着这个线程可以被JVM来调度执行；在调度过程中，JVM通过调用线程类的run()方法来完成实际的操作，当run()方法结束后，此线程就会终止。

　如果直接调用run()方法，这会别当做一个普通的函数调用，程序中仍然只有主线程这一个线程；
由此可知，只有通过调用线程类的start()方法才能真正达到多线程的目的。







#### 线程

开销 ：进程间切换，涉及保护现场，恢复现场等，会有较大的开销



实现多线程的时候：

1、需要继承Thread类

2、必须要重写run方法，指的是核心执行的逻辑

3、线程在启动的时候，不要直接调用run方法，而是要通过start()来进行调用

4、每次运行相同的代码，出来的结果可能不一样，原因在于多线程谁先抢占资源无法进行人为控制

此时出现的问题：

1、每次在启动线程对象的时候都会创建自己对象的属性值，相当于每个线程操作自己，没有真正意义上实现			贡献

​	解决方法：将共享对象，共享变量设置成static

2、每次访问共享对象的时候，数据不一致了、

​		解决方法：使用线程同步

![image-20200719100145686](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200719100145686.png)

方法二（推荐）：使用接口的方式，每次只创建了一个共享对象，所有的线程能够实现资源共享

 第二种实现方式：使用了代理设计模式

1、实现Runnable接口

2、重写run方法

3、创建Thread对象，将刚刚创建好的runnable的子类实现作为thread的构造参数

4、通过thread.start()进行启动

![image-20200719104149028](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200719104149028.png)

##### 线程安全问题

![image-20200720180155159](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200720180155159.png)

![image-20200720180214485](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200720180214485.png)

##### 分析同步原理

![image-20200720181112947](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200720181112947.png)

##### 同步的前提:

(1)必须有两个或两个以上的线程
		(2)必须是多个线程使用同一资源
		(3)必须保证同步中只能有一个线程在运行



##### 线程的生命周期：

1、新生状态：

当创建好当前线程对象之后，没有启动之前（调用start方法之前）

ThreadDemo thread = new ThreadDemo()

RunnableDemo run = new RunnableDemo()

2、就绪状态：准备开始执行，并没有执行，表示调用start方法之后

当对应的线程创建完成，且调用start方法之后，所有的线程会添加到一个就绪队列中，所有的线程同时去抢占cpu的资源

3、运行状态：当当前进程获取到cpu资源之后，就绪队列中的所有线程会去抢占cpu的资源，谁先抢占到谁先执行，在执行的过程中就叫做运行状态

抢占到cpu资源，执行代码逻辑开始

4、死亡状态：当运行中的线程正常执行完所有的代码逻辑或者因为异常情况导致程序结束叫做死亡状态

进入的方式：

1、正常运行完成且结束

2、人为中断执行，比如使用stop方法

3、程序抛出未捕获的异常

5、阻塞状态：在程序运行过程中，发生某些异常情况，导致当前线程无法再顺利执行下去，此时会进入阻塞状态，进入阻塞状态的原因消除之后，

所有的阻塞队列会再次进入到就绪状态中，随机抢占cpu的资源，等待执行

进入的方式：

sleep方法

等待io资源

join方法（代码中执行的逻辑）







##### 代理模式



![image-20200719141904212](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200719141904212.png)



##### 线程池

在实际使用中，线程是很占用系统资源的，如果对线程管理不善
很容易导致系统问题。因此，在大多数并发框架中都会使用线程
池来管理线程，使用线程池管理线程主要有如下好处：
–
1 、使用线程池可以重复利用已有的线程继续执行任务，避免线程在创建和
销毁时造成的消耗
–
2 、由于没有线程创建和销毁时的消耗，可以提高系统响应速度
–
3 、通过线程可以对线程进行合理的管理，根据系统的承受能力调整可运行
线程数量的大小等



##### 线程池分类

![image-20200719201518146](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200719201518146.png)

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200719201411654.png" alt="image-20200719201411654"  />



##### 线程池参数

![image-20200719224607260](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200719224607260.png)

参数说明
▪
corePoolSize ：核心线程池的大小
▪
maximumPoolSize ：线程池能创建线程的最大个数
▪
keepAliveTime ：空闲线程存活时间
▪
unit ：时间单位，为 keepAliveTime 指定时间单位
▪
workQueue ：阻塞队列，用于保存任务的阻塞队列
▪
threadFactory ：创建线程的工程类
▪
handler ：饱和策略（拒绝策略



阻塞队列（面试）

![image-20200719225113160](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200719225113160.png)

![image-20200719225646796](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200719225646796.png)



Arrayblockingqueue和Linkblockqueue的区别

![image-20200719225422453](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200719225422453.png)



##### 网络编程

```java
package com.mashibing.client;

import java.io.DataOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.net.Socket;

* 客户端向服务端发送数据
* */
public class Client {
    public static void main(String[] args) throws IOException {

        //创建socket对象，其实是开启实现io的虚拟接口（此接口不是java中的接口，而是类似于网线的插槽）
        //需要指定数据接受方的ip地址和端口号
        Socket client = new Socket("localhost",10086);
        //获取输出流对象，想服务端发送数据
        OutputStream outputStream = client.getOutputStream();
        //将输出流对象进行包装
        DataOutputStream dataOutputStream = new DataOutputStream(outputStream);
        //传输数据
        dataOutputStream.writeUTF("hello,你好");
        //关闭流操作
        dataOutputStream.close();
        outputStream.close();
        client.close();
    }
}

```



##### Lambda表达式

函数式接口：有且只有一个抽象方法的接口

​	Supplier 代表一个输出
​	Consumer 代表一个输入
​	BiConsumer 代表两个输入
​	Function 代表一个输入，一个输出（一般输入和输出是不同类型的）
​	UnaryOperator 代表一个输入，一个输出（输入和输出是相同类型的）
​	BiFunction 代表两个输入，一个输出（一般输入和输出是不同类型的）
​	BinaryOperator 代表两个输入，一个输出（输入和输出是相同类型的）

案例：



![image-20200721105658144](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721105658144.png)

方法引用

![image-20200721111243128](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721111243128.png)

实例引用方法

![image-20200721113025198](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721113025198.png)

构造方法引用

![image-20200721121604756](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721121604756.png)

![image-20200721110847591](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721110847591.png)



注解：表示当前接口的功能

![image-20200721001553521](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721001553521.png)





##### stream API

数组遍历，新方法

![image-20200721141200806](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721141200806.png)

![image-20200721142121635](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721142121635.png)

![image-20200721142556509](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721142556509.png)

![image-20200721143212497](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721143212497.png)

![image-20200721150414940](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721150414940.png)

![image-20200721150838421](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721150838421.png)

![image-20200721151237388](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721151237388.png)



##### 自定义注解（Annotation）

@作为开头

##### 元注解

元注解的做哟个是负责注解其他注解，java中定义了四个标准的meta-annotation类型，他们被用来提供对其他annotation类型作说明
▪这些类型和它们所支持的类在java.lang.annotation包中
–@Target：用来描述注解的使用范围（注解可以用在什么地方）
–@Retention：表示需要在什么级别保存该注释信息，描述注解的生命周期
▪Source < Class < Runtime
–@Document：说明该注解将被包含在javadoc中
–@Inherited：说明子类可以继承父类中的该注解

![image-20200721154355151](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721154355151.png)

##### 复习

![image-20200721160207523](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721160207523.png)



### 数据库

![image-20200721165154944](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721165154944.png)

#### Oracle



sqlplus /nolog    不登录，使用命令

 conn sys/bjmsb@orcl as sysdba;   以sys用户登录

conn scott/tiger;     scott为普通用户名，tiger 为密码

show user;

select * from tab;    查看所有表

select * from 表名;   查看某个表

select * from scott.emp;   sys用户查看scott用户的emp表



###### 设置命令行中表的格式：

```mysql
set pagesize 50;  
set linesize 200;
```





 show index from tab_with_index;           查看表索引



Select * from tab;//查看用户下的所有表
▪Select * from user_tables;//详细查询当前用户下的所有表
▪--desc 表名； //查看表结构
▪查看所有表：select table_name from user_tables;
▪查看表结构：describe dept;(戒	者desc dept;)
▪emp表雇员表(employee)
–Empno: 雇员工号 Ename: 雇员名字
–Job:工作。（秘书、销售、经理、分析员、保管）
–Mgr(manager):经理的工号 Hiredate:雇用日期
–Sal: 工资 Comm: 津贴 Deptno: 所属部门号
▪dept表部门表（department）
–Deptno:部门号 Dname:部门名字 Loc: 地址
▪salgrade表一个公司是有等级制度，用此表表示一个工资的等级
▪Grade:等级 losal:最低工资 hisal:最高工资
▪bonus表 奖金表：表示一个雇员的工资及奖金。
–Ename:雇员名字， job:



Hire

OLAP:

OLIP

时间拉链表



conn scott/tiger@cqc20721;  创建的新数据库

![image-20200721194206957](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200721194206957.png)



services.msc   启动服务

结构化查询诧言 (Structured Query Language)，具有定义、查询、更新和控制等多种功能，是关系数据库的标准诧言。

更改mysql密码使用规则 ：

​	mysql8之前的版本使用的密码加密规则是mysql_native_password，但是在mysql8则是caching_sha2_password，所以需要修改密码加密规则: 

`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root';`



MySQL时区错误，按如下方法修改

```mysql
mysql> show variables like '%time_zone%';
+------------------+--------+
| Variable_name    | Value  |
+------------------+--------+
| system_time_zone |        |
| time_zone        | SYSTEM |
+------------------+--------+
2 rows in set, 1 warning (0.03 sec)
 
mysql> set global time_zone='+8:00';
Query OK, 0 rows affected (0.03 sec)
 
mysql> show variables like '%time_zone%';
+------------------+--------+
| Variable_name    | Value  |
+------------------+--------+
| system_time_zone |        |
| time_zone        | SYSTEM |
+------------------+--------+
2 rows in set, 1 warning (0.00 sec)
```



#### SQL分类

##### ==DML==

 (Data Manipulation Language)  数据操作语言 :

​			SELECT

​	INSERT 

​	UPDATE

```sql
UPDATE		tablename
SET		column = value [, column = value, ...]
[WHERE 		condition];
```

​	DELETE

```sql
--DML：数据库操作语言
--增
--删
--改

--在实际项目中，使用最多的是读取操作，但是插入数据和删除数据同等重要，而修改操作相对较少

/*
插入操作：
  元组值的插入
  查询结果的插入
*/
--最基本的插入方式
--insert into tablename values(val1,val2,....) 如果表名之后没有列，那么只能将所有的列都插入
--insert into tablename(col1,col2,...) values(val1,val2,...) 可以指定向哪些列中插入数据

insert into emp values(2222,'haha','clerk',7902,to_date('2019-11-2','YYYY-MM-dd'),1000,500,10);
select * from emp;
--向部分列插入数据的时候，不是想向哪个列插入就插入的，要遵循创建表的时候定义的规范
insert into emp(empno,ename) values(3333,'wangwu')

--创建表的其他方式
--复制表同时复制表数据，不会复制约束
create table emp2 as select * from emp;
--复制表结构但是不复制表数据，不会复制约束
create table emp3 as select * from emp where 1=2;
--如果有一个集合的数据，把集合中的所有数据都挨条插入的话，效率如何？一般在实际的操作中，很少一条条插入，更多的是批量插入

/*
删除操作：
 delete from tablename where condition

*/
--删除满足条件的数据
delete from emp2 where deptno = 10;
--把整张表的数据全部清空
delete from emp2;
--truncate ,跟delete有所不同，delete在进行删除的时候经过事务，而truncate不经过事务，一旦删除就是永久删除，不具备回滚的操作
--效率比较高，但是容易发生误操作，所以不建议使用
truncate table emp2

/*
修改操作：
   update tablename set col = val1,col2 = val2 where condition;
   可以更新或者修改满足条件的一个列或者多个列
*/
--更新单列
update emp set ename = 'heihei' where ename = 'hehe';
--更新多个列的值
update emp set job='teacher',mgr=7902 where empno = 15;


/*
增删改是数据库的常用操作，在进行操作的时候都需要《事务》的保证， 也就是说每次在pl/sql中执行sql语句之后都需要完成commit的操作
事务变得非常关键：
    最主要的目的是为了数据一致性
    如果同一份数据，在同一个时刻只能有一个人访问，就不会出现数据错乱的问题，但是在现在的项目中，更多的是并发访问
    并发访问的同时带来的就是数据的不安全，也就是不一致
    如果要保证数据的安全，最主要的方式就是加锁的方式，MVCC
    
    事务的延申：
        最基本的数据库事务
        声明式事务
        分布式事务
    为了提高效率，有可能多个操作会在同一个事务中执行，那么就有可能部分成功，部门失败，基于这样的情况就需要事务的控制。
    select * from emp where id = 7902 for update
    select * from emp where id = 7902 lock in share mode.
    
    如果不保证事务的话，会造成脏读，不可重复读，幻读。
*/
```



##### ==DDL==​

 (Data Definition language)       数据定义语言:	

###### 	CREATE :表的创建

```java
/*
CREATE TABLE [schema.]table
  (column datatype [DEFAULT expr] , …
	);
*/

--设计要求：建立一张用来存储学生信息的表，表中的字段包含了学生的学号、姓名、年龄、入学日期、年级、班级、email等信息，
--并且为grade指定了默认值为1，如果在插入数据时不指定grade得值，就代表是一年级的学生

create table student
(
stu_id number(10),
name varchar2(20),
age number(3),
hiredate date,
grade varchar2(10) default 1,
classes varchar2(10),
email varchar2(50)
);
insert into student values(20191109,'zhangsan',22,to_date('2019-11-09','YYYY-MM-DD'),'2','1','123@qq.com');
insert into student(stu_id,name,age,hiredate,classes,email) values(20191109,'zhangsan',22,to_date('2019-11-09','YYYY-MM-DD'),'1','123@qq.com');

select * from student;
--正规的表结构设计需要使用第三方工具 powerdesigner
--再添加表的列的时候，不能允许设置成not null
alter table student add address varchar2(100);
alter table student drop column address;
alter table student modify(email varchar2(100));
--重新命名表
rename student to stu;
--删除表
/*
在删除表的时候，经常会遇到多个表关联的情况，多个表关联的时候不能随意删除，需要使用级联删除
cascade:如果A,B,A中的某一个字段跟B表中的某一个字段做关联，那么再删除表A的时候，需要先将表B删除
set null:再删除的时候，把表的关联字段设置成空
*/
 drop table stu;

 --创建表的时候可以给表中的数据添加数据校验规则，这些规则称之为约束
 /*
 约束分为五大类
 not null: 非空约束，插入数据的时候某些列不允许为空
 unique key:唯一键约束，可以限定某一个列的值是唯一的，唯一键的列一般被用作索引列。
 primary key:主键：非空且唯一，任何一张表一般情况下最好有主键，用来唯一的标识一行记录，
 foreign key:外键，当多个表之间有关联关系（一个表的某个列的值依赖与另一张表的某个值）的时候，需要使用外键
 check约束:可以根据用户自己的需求去限定某些列的值
 */
 --个人建议：再创建表的时候直接将各个表的约束条件添加好，如果包含外键约束的话，最好先把外键关联表的数据优先插入

 insert into emp(empno,ename,deptno) values(9999,'hehe',50);

 create table student
(
stu_id number(10) primary key,
name varchar2(20) not null,
age number(3) check(age>0 and age<126),
hiredate date,
grade varchar2(10) default 1,
classes varchar2(10),
email varchar2(50) unique,
deptno number(2)
);
insert into student(stu_id,name,age,hiredate,classes,email,deptno) values(20191109,'zhansgan',111,to_date('2019-11-09','YYYY-MM-DD'),'1','12443@qq.com',10);

alter table student add constraint fk_0001 foreign key(deptno) references dept(deptno);
```



###### 	ALTER :表的修改

```mysql
#语法格式：
alter table 表名 drop column 列名;
#示例：
alter table test4 drop column addr;
```

​	

​	ADD

```mysql
#语法格式：
ALTER TABLE tbl_name
ADD [COLUMN] (column_definition...) type;
#示例：追加一个新列
ALTER TABLE dept80 
ADD job_id varchar(15);
```



​	DROP 

```mysql
#语法格式：
ALTER [IGNORE] TABLE tbl_name
DROP [COLUMN] col_name

#示例：删除列
ALTER TABLE  dept80
DROP COLUMN  job_id; 
```

​	

​	CHANGE

```mysql
#语法格式：
ALTER TABLE tbl_name
CHANGE old_column  new_column  dataType

#示例：重命名一个列
ALTER TABLE  dept80
CHANGE department_name dept_name varchar(15); 
```

​	

​	MODIFY

```mysql
#语法格式：
ALTER TABLE tbl_name 
MODIFY COLUMN column_definition  BIGINT NOT NULL

#修改约束或类型
ALTER TABLE cqc22
MODIFY COLUMN  VARCHAR(10);
```



​	RENAME 

​	TRUNCATE

##### ==DCL==  

(Data Control Language)             数据控制语言 :

​			GRANT      REVOKE
–Transaction:commit rollback savepoint

##### Select子句顺序

▪Sql语句执行过程：
1.读取from子句中的基本表、视图的数据，[执行笛卡尔积操作]。
2.选取满足where子句中给出的条件表达式的元组
3.按group子句中指定列的值分组，同时提取满足Having子句中组条件表达式的那些组
4.按select子句中给出的列名戒列表达式求值输出
5.Order by子句对输出的目标表进行排序。

![image-20200723191041886](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200723191041886.png)

##### 外连接

![image-20200723200151396](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200723200151396.png)

##### 自连接和笛卡尔积

![image-20200723201138697](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200723201138697.png)

##### 99语法

natural join 自然连接

--natural join==等值连接
select * from emp e natural join dept d;
--当两张表中不具有相同的列名时，会进行笛卡尔积

Oracle不支持limit（显示前n条），用rownum，不能直接用，要嵌套使用

![image-20200723224755158](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200723224755158.png)

![image-20200723225243360](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200723225243360.png)

![image-20200723225415830](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200723225415830.png)



##### view 视图

视图也称虚表，不占用物理空间

物化视图：on demand，

​					on commit

创建视图

在 CREATE VIEW 语句后加入子查询
CREATE [OR REPLACE] VIEW
view
[(alias[, alias]...)]
AS subquery
[WITH READ ONLY];
▪
create or replace view v$_

##### 视图定义

视图 ( view)，也称虚表 , 不占用物理空间，这个也是相对概念，因为视图本身的定义语句还
是要存储在数据字典里的。视图只有逻辑定义。 每次使用的时候 , 只是重新执行 SQL.
▪
视图是从一个或多个实际表中获得的，这些表的数据存放在数据库中。那些用于产生视图的
表叫做该视图的基表。一个视图也可以从另一个视图中产生。
▪
视图的定义存在数据库中，与此定义相关的数据并没有再存一份于数据库中。通过视图看到
的数据存放在基表中。
▪
视图看上去非常象数据库的物理表，对它的操作同任何其它的表一样。当通过视图修改数据
时，实际上是在改变基表中的数据；相反地，基表数据的改变也会自动反映在由基表产生的
视图中。由于逻辑上的原因，有些 Oracle 视图可以修改对应的基表，有些则不能（仅仅能查
询）。

使用 system 用户为 scott 增加权限： grant create view,create
table to scott ;
▪
使用 system 用户为 scott 解锁： alter user scott account
unlock;

```sql
--创建视图
create view v_emp as select * from emp where deptno = 30;

--普通用户，第一次创建视图要开通权限，管理员登录，授权
grant create view to scott;
```



##### 创建用户

语法：
create user username identified by password
红色字体为用户名密码。
create user
bjmsb identified by bjmsb

查看用户是否创建
SQL>select username from
dba_users

使用管理员账号创建用户
Sys
system

创建用户
–
Create user 用户名 identified by 密码
–
链接登录
▪
Grant create session to 用户名
–
授予表的权限
▪
Grant all on scott.emp to 用户名
–
收回权限
▪
Revoke all on scott.emp from 用户名



##### 序列sequence

序列是 oracle 专有的对象，它用来产生一个自动递增的数列
创建序列的语法：
create sequence
seq_ name
increment by n
start with n
maxvalue
n|nomaxvalue 10^27 or 1
minvalue
n|no minvalue
cycle|nocycle
cache
n|nocache
实例： create sequence seq_empcopy_id start with 1 increment by 1;

```sql
--在oracle中如果需要完成一个列的自增操作，必须要使用序列
/*
create sequence seq_name
  increment by n  每次增长几
  start with n    从哪个值开始增长
  maxvalue n|nomaxvalue 10^27 or -1  最大值
  minvalue n|no minvalue  最小值
	cycle|nocycle           是否有循环
	cache n|nocache          是否有缓存

*/
create sequence my_sequence
increment by 2
start with 1

--如何使用？
--注意，如果创建好序列之后，没有经过任何的使用，那么不能获取当前的值，必须要先执行nextval之后才能获取当前值
--dual是oracle中提供的一张虚拟表，不表示任何意义，在测试的时候可以随意使用
--查看当前序列的值
select my_sequence.currval from dual;
--获取序列的下一个值
select my_sequence.nextval from dual;

insert into emp(empno,ename) values(my_sequence.nextval,'hehe');
select * from emp;

```



##### SQL数据更新DML






##### 事务

事务（ Transaction ）是一个操作序列。这些操作要么都做，要么都不做，是一个不可分割的工作单位，是数据库环境中的逻辑工作单位。

事务是为了保证数据库的完整性

事务不能嵌套

在 oracle 中，没有事务开始的语句。 一个 Transaction 起始于一条
DML(Insert 、 Update 和 Delete ) 语句，结束于以下的几种情况：
用户显式执行 Commit 语句提交操作或 Rollback 语句回退。
当执行 DDL(Create 、 Alter 、 Drop) 语句事务自动提交。
用户正常断开连接时， Transaction 自动提交。
系统崩溃或断电时事务自动回退 。



###### ACID

指数据库事务正确执行的四个基本要素:原子性（Atomicity）、一致性（Consistency）、隔离性（Isolation）、持久性（Durability）。

默认隔离级别：repeated read 不可重复读

```sql
--事务：表示操作集合，不可分割，要么全部成功，要么全部失败

--事务的开始取决于一个DML语句
/*
事务的结束
  1、正常的commit（使数据修改生效）或者rollback（将数据恢复到上一个状态）
  2、自动提交，但是一般情况下要将自动提交进行关闭，效率太低
  3、用户关闭会话之后，会自动提交事务
  4、系统崩溃或者断电的时候回回滚事务，也就是将数据恢复到上一个状态
*/
insert into emp(empno,ename) values(2222,'zhangsan');
--commit;
--rollback;
select * from emp;

--savepoint  保存点
--当一个操作集合中包含多条SQL语句，但是只想让其中某部分成功，某部分失败，此时可以使用保存点
--此时如果需要回滚到某一个状态的话使用 rollback to sp1;
delete from emp where empno = 1111;
delete from emp where empno = 2222;
savepoint sp1;
delete from emp where empno = 1234;
rollback to sp1;
commit;
/*
事务的四个特性：ACID
  原子性：表示不可分割，一个操作集合要么全部成功，要么全部失败，不可以从中间做切分
  一致性：最终是为了保证数据的一致性，当经过N多个操作之后，数据的状态不会改变（转账）
          从一个一致性状态到另一个一致性状态，也就是数据不可以发生错乱
  隔离性：各个事务之间相关不会产生影响，（隔离级别）
          严格的隔离性会导致效率降低，在某些情况下为了提高程序的执行效率，需要降低隔离的级别
          隔离级别：
            读未提交
            读已提交
            可重复读
            序列化
          数据不一致的问题：
            脏读
            不可重复读
            幻读
  持久性：所有数据的修改都必须要持久化到存储介质中，不会因为应用程序的关闭而导致数据丢失

  四个特性中，哪个是最关键的？
     所有的特性中都是为了保证数据的一致性，所以一致性是最终的追求
     事务中的一致性是通过原子性、隔离性、持久性来保证的

     锁的机制：
     为了解决在并发访问的时候，数据不一致的问题，需要给数据加锁
     加锁的同时需要考虑《粒度》的问题：
         操作的对象
            数据库
            表
            行
     一般情况下，锁的粒度越小，效率越高，粒度越大，效率越低 
            在实际的工作环境中，大部分的操作都是行级锁  

*/
```







创建表





##### 三范式

减少数据冗余

第一范式：

​	列不可分

第二范式：

​	列必须直接依赖于主键

​	列可以单独构成一张表，就查分开

​	数据部分依赖，产生数据冗余，需要分解表

第三范式：

​	避免传递依赖

​	表里的列不能出现其它表的非主键字段



##### JDBC

JDBC(Java Database Connectivity) 是基于 JAVA 语言访问数据库的一种技术,java连接数据库。

JDBC Java Data Base Connectivity,java 数据库连接）是一种用于执行 SQL 语句的 Java API ，可以为多种关系数据库提供统一访问，它由一组用 Java 语言编写的类和接口组成。 JDBC 提供了一种基准，据此可以构建更高级的工具和接口，使数据库开发人员能够编写数据库应用程序，同时， JDBC 也是个商标名。

JDBC 的设计思想：由 SUN 公司 ( 提供访问数据库的接口，由数据库厂商提供对这些接口的实现，程序员编程时都是





##### MySQL连接池

###### 	c3p0

###### 	Druid连接池

​		Druid连接池是阿里巴巴开源的数据库连接池项目。Druid连接池为监控而生，内置强大的监控功能，监控特性不影响性能。功能强大，能防SQL注入，内置Loging能诊断Hack应用行为。

###### 	hikariCP

#### 索引

###### 	局部性原理：

​		时间局部性和空间局部性

![image-20200725232203751](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725232203751.png)

###### 磁盘预读

预读的长度一般为页（ page ）的整数倍

页是存储器的逻辑块，操作系统往往将主存和磁盘存储区分割为连续的大小
相等的块，每个存储块称为一页（在许多操作系统中，页大小通常为 4k
主存和磁盘以页为单位交换数据 。



###### 连接器

连接器负责跟客户端建立连接，获取权限、维持和管理连接

用户名密码验证

查询权限信息，分配对应的权限

可以使用 show processlist 查看现在的连接

如果太长时间没有动静，就会自动断开，通过 wait_timeout 控制，默认 8 小时

连接可以分为两类：

长连接：推荐使用，但是要周期性的断开长连接

短链接



![image-20200725233301550](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725233301550.png)

![image-20200725234754903](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200725234754903.png)



##### 索引文件的结构

###### hash

###### 二叉树

###### B 树

![image-20200726001928433](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200726001928433.png)

###### B+ 树（MySQL使用）

![image-20200726002213815](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200726002213815.png)

![image-20200726002810850](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200726002810850.png)

B+树示例：

![image-20200726004358258](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200726004358258.png)

###### 回表

![image-20200726003409556](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200726003409556.png)

![image-20200726003524125](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200726003524125.png)



##### 索引分类

主键索引：主键是一种唯一性索引，但它必须指定为PRIMARY KEY，每个表只能有一个主键。

唯一索引
– 索引列的所有值都只能出现一次，即必须唯一，值可以为空。
▪ 普通索引
– 基本的索引类型，值可以为空，没有唯一性的限制。（覆盖索引）
▪ 全文索引,MyISAM支持，Innodb在5.6之后支持
– 全文索引的索引类型为FULLTEXT。全文索引可以在varchar、char、text类型的列上创建
▪ 组合索引
– 多列值组成一个索引，专门用于组合搜索（最左匹配原则）



##### Mysql存储引擎

memory，数据持久化不好，性能好，断电数据消失

|              | MyISAM     | InnoDB                   |
| ------------ | ---------- | ------------------------ |
| 索引类型     | 非聚簇索引 | 聚簇索引                 |
| 支持事务     | 否         | 是                       |
| 支持表锁     | 是         | 是                       |
| 支持行锁     | 否         | 是                       |
| 支持外键     | 否         | 是                       |
| 支持全文索引 | 是         | 是（5.6后支持）          |
| 适合操作类型 | 大量select | 大量insert,update,delete |



Redolog（保证持久性），属于InnoDB，前滚

Undolog（保证原子性），属于InnoDB，回滚

Binlog 归档日志，服务端日志文件，默认不开启

​	查看属性状态：show variables like '%log_%';



##### MySQL锁机制

OLTP(Oline Transaction Process) 联机事务处理

OLAP(Oline Analysis Process)      联机分析处理

kylin麒麟







### 反射

反射：框架设计的灵魂

#### 什么是反射？

 反射是Java的特征之一，是一种间接操作目标对象的机制，一个类在被JVM加载内存后，JVM为这个类自动创建一个Class对象（一个类只产生一个Class对象）。

**反射的本质：得到Class对象后，反向获取类的各种信息**

将类的各个组成部分封装为其他对象（从源代码到类对象阶段），这就是反射机制

反射优点：

1、可以在程序运行过程中，操作这些对象；

2、可以解耦，提高程序的可扩展性；

Java代码在计算机中的三个阶段：Source源代码阶段、Class类对象阶段、Runtime运行时阶段

所有Person对象都是由类对象创建的

![image-20200805133107912](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200805133107912.png)



#### 获取类对象

获取Class对象

1、Class.forName（"全类名"）: 将字节码文件加载到内存，返回Class对象（java代码在第一阶段，只有字节码文件，还未进内存，要手动将其加载进内存，生成字节码文件对象）；

应用：多用于配置文件，将类名定义在配置文件中，读取文件，加载类。

2、类名.class：通过类名属性class获取Class对象（java代码第二阶段，已经有字节码文件对象(有了类名，但还没有实际对象)，可以通过类名获取Class对象，）；

应用：多用于参数传递

3、对象.getClass()：getClass方法在Object类中定义的（java代码第三阶段，有new对象，可以通过对象方法（继承子Object类的getClass方法）来获取Class对象）；

应用：多用于对象获取字节码文件的方式



Class对象功能：

获取功能：获取成员变量；获取构造方法；获取成员方法；获取类名。



结论：同一个字节码文件（.class）在一次运行过程中，只会被夹在一次，哪种方式获取的Class对象都是同一个

```java
//1.方法一：通过类名获取Person的Class对象
Class personClass = Person.class;
//方法二：通过类的实例，获取类对象
Person p = new Person();
Class aClass = p.getClass();
System.out.println(aClass);
//方法三：通过静态方法获取Class对象
Class aClass1 = Class.forName("com.cqc.Person");
System.out.println(aClass1);
```

获取字段

```java
//2.获取成员变量(只会获取所有public修饰的成员变量)getFields()
Field[] fields = personClass.getFields();
for(Field field:fields){
    System.out.println(field);
}
// personClass.getField获取指定public修饰的变量
Field field = personClass.getField("name");
System.out.println(field);
System.out.println("----------------------");
//3.对fields 成员变量的操作，get(属性名)
Field weight = personClass.getField("weight");
Person p1 = new Person();
Object value = weight.get(p1);
System.out.println(value);

//4.设置值set(对象实例，属性值)
weight.set(p,50);
System.out.println(p);

//getDeclaredFields()获取所有成员属性，不考虑修饰符
Field[] declaredFields = personClass.getDeclaredFields();
for(Field declaredField:declaredFields){
    System.out.println(declaredField);
}
Field declaredField = personClass.getDeclaredField("address");
//忽略安全访问修饰符的安全检查,进行暴力访问
declaredField.setAccessible(true);
Object o = declaredField.get(p);
System.out.println(o);
}
```

获取构造方法

```java
//1.获取Person的Class对象
Class personClass = Person.class;

//2.获取构造方法getConstructors()
Constructor[] constructors = personClass.getConstructors();
for(Constructor c:constructors){
    System.out.println(c);
}
System.out.println("======================");

//3.获取指定类型构造方法getConstructor(int.class),构造方法是用来创建对象的
Constructor constructor = personClass.getConstructor(int.class);
System.out.println(constructor);

//4.创建对象
Object person = constructor.newInstance(608);
System.out.println(person);
//5.如果用无参构造方法创建对象，可以简化操作：Class对象的newInsatance方法(已弃用)
Object person1 = personClass.newInstance(); //已过时

//java 9后都是用getDeclaredConstructor().newInstance()方法来创建对象
Object person1 = personClass.getDeclaredConstructor().newInstance();
System.out.println(person1);
```

获取成员方法

```java
//1.获取Person的Class对象
Class personClass = Person.class;
//2.获取指定成员方法 getMethod(方法名,形参类型)
Method sp = personClass.getMethod("eat",String.class);
Person p = new Person();
//调用成员方法 invoke(对象实例,实际参数)
sp.invoke(p,"面包");

//3.获取所有public修饰的方法(还包括Object继承的方法)
Method[] methods = personClass.getMethods();
for(Method m:methods){System.out.println(m);}
//4.获取方法名称
for(Method m:methods) {
    String name = m.getName();
    System.out.println(name);
}
```





#### 反射应用

需求：写一个框架，不能改变该类的任何代码的情况下，可以任意创建对象，并执行其中任意方法

实现：1、配置文件；2、反射；

步骤：

1.将需要创建的对象全类名和需要执行的方法定义在配置文件中；

2.在程序中加载配置文件

3.使用反射技术来加载类文件进内存；

4.创建对象，执行方法；









## 进程 线程 纤程 中断



##### 面试高频：进程和线程有什么区别？

答案：进程就是一个程序运行起来的状态，线程是一个进程中的不同的执行路径。专业：进程是OS分配资源的基本单位，线程是执行调度的基本单位。分配资源最重要的是：独立的内存空间，线程调度执行（线程共享进程的内存空间，没有自己独立的内存空间）

纤程：用户态的线程，线程中的线程，切换和调度不需要经过OS

优势：1：占有资源很少 OS : 线程1M Fiber：4K 2：切换比较简单 3：启动很多个10W+

目前2020 3 22支持内置纤程的语言：Kotlin Scala Go Python(lib)... Java? （open jdk : loom）



##### 源码，补码，反码

原码，反码，补码的产生过程，就是为了解决，计算机做减法和引入符号位（正号和负号）的问题

无符号数：0--255

有符号数：它的表示范围是多少？

- 正数的反码是其本身
- 负数的反码是在其原码的基础上, 符号位不变，其余各个位取反.
- 正数的补码就是其本身
- 负数的补码是在其原码的基础上, 符号位不变, 其余各位取反, 最后+1. (即在反码的基础上+1)

![image-20200713113547233](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200713113547233.png)

 0     0000 0000-----取反-----0000 0000----补码-----0000 0000

-0    1000 0000------取反-----1111 1111----补码（反码+1）-----10000 0000（溢出1）



##### 二进制逻辑运算

~   取反

^  异或

/>>/  符号右移：正整数往右移一位等于除2，左移乘2

/>>>/  无符号右移



a=3,b=4,a与b值交换计算机最快的方法

![image-20200713132850571](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200713132850571.png)

![image-20200713131618935](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200713131618935.png)

![image-20200713131728474](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200713131728474.png)

首先, 因为人脑可以知道第一位是符号位, 在计算的时候我们会根据符号位, 选择对真值区域的加减. (真值的概念在本文最开头).

但是对于计算机, 加减乘数已经是最基础的运算, 要设计的尽量简单. 计算机辨别"符号位"显然会让计算机的基础电路设计变得十分复杂! 于是人们想出了将符号位也参与运算的方法.

根据运算法则减去一个正数等于加上一个负数, 即: 1-1 = 1 + (-1) = 0 , 所以机器可以只有加法而没有减法, 这样计算机运算的设计就更简单了.





##### DCL 

外面的那层判断是为了提高效率

![image-20200723211041139](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200723211041139.png)



指令重排：提高cpu效率，

##### 内存屏障：阻止指令重排，Load是读，Store是写

![image-20200723212413513](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200723212413513.png)



##### hanppens-before

![image-20200723212723863](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200723212723863.png)



cpu如何实现内存屏障的：

![image-20200723213216484](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200723213216484.png)

