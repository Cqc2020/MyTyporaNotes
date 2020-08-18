# Servlet学习

## 什么是Servlet？

![image-20200802120555513](C:%5CUsers%5CAdministrator%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20200802120555513.png)

## HTTP协议

### URI和URL的区别

名字标识符和定位标识符

统一资源标志符URI就是在某一规则下能把一个资源独一无二地标识出来。
拿人做例子，假设这个世界上所有人的名字都不能重复，那么名字就是URI的一个实例，通过名字这个字符串就可以标识出唯一的一个人。
现实当中名字当然是会重复的，所以身份证号才是URI，通过身份证号能让我们能且仅能确定一个人。
那统一资源定位符URL是什么呢。也拿人做例子然后跟HTTP的URL做类比，就可以有：

动物住址协议://地球/中国/浙江省/杭州市/西湖区/某大学/14号宿舍楼/525号寝/张三.人

可以看到，这个字符串同样标识出了唯一的一个人，起到了URI的作用，所以URL是URI的子集。URL是以描述人的位置来唯一确定一个人的。
在上文我们用身份证号也可以唯一确定一个人。对于这个在杭州的张三，我们也可以用：

身份证号：[123456789](tel:123456789)

来标识他。
所以不论是用定位的方式还是用编号的方式，我们都可以唯一确定一个人，都是URl的一种实现，而URL就是用定位的方式实现的URI。

回到Web上，假设所有的Html文档都有唯一的编号，记作html:xxxxx，xxxxx是一串数字，即Html文档的身份证号码，这个能唯一标识一个Html文档，那么这个号码就是一个URI。
而URL则通过描述是哪个主机上哪个路径上的文件来唯一确定一个资源，也就是定位的方式来实现的URI。

### HTTP协议请求报文格式

![image-20200802122310237](C:%5CUsers%5CAdministrator%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20200802122310237.png)



### HTTP请求方法

![image-20200802122620262](C:%5CUsers%5CAdministrator%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20200802122620262.png)



### HTTP协议响应报文格式

![image-20200802122841397](C:%5CUsers%5CAdministrator%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20200802122841397.png)



### 响应状态码

![image-20200802133953038](C:%5CUsers%5CAdministrator%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20200802133953038.png)



![image-20200802134018253](C:%5CUsers%5CAdministrator%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20200802134018253.png)

![image-20200802163949312](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802163949312.png)

## Servlet基本原理

### Servlet访问流程

```
url：http://服务器地址:端口/虚拟项目名/servlet别名

uri：虚拟项目名/servlet别名
```

![image-20200802155105371](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802155105371.png)

![image-20200802155351910](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802155351910.png)



### Servlet生命周期

![image-20200802161043335](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802161043335.png)

### request常用方法

![image-20200802172300547](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802172300547.png)



### 解决乱码

![image-20200802202647106](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802202647106.png)



### Servlet处理流程

![image-20200802202826387](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802202826387.png)



### Cookie

![image-20200802214441683](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802214441683.png)

![image-20200802214503599](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802214503599.png)



### Session

![image-20200802220743245](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802220743245.png)

#### Session基本原理

![image-20200802221122707](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802221122707.png)

![image-20200802222933485](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802222933485.png)





### ServletContext

#### 什么是ServletContext？

![image-20200802223952153](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802223952153.png)

#### ServletContext原理

![image-20200802224101382](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802224101382.png)



#### 获取servletContext对象3种方式

![image-20200802224620198](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802224620198.png)



#### ServletContext API

![image-20200802225158115](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802225158115.png)



作用

![image-20200802225710472](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802225710472.png)

![image-20200802225800902](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200802225800902.png)

### ServletConfig

作用

![image-20200803100722328](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803100722328.png)



## JSP

### 什么是JSP？

JSP（Java Server Pages）动态网页技术标准

静态和动态的区别：

1. 动态网页会随着时间，地点，用户操作的改变而改变
2. 动态网页要用到脚本语言JS

ASP(Active Server Pages) 

PHP(Hylpertext Preprocessor) 超文本预处理语言

![image-20200803101303681](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803101303681.png)





### include

![image-20200803105749942](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803105749942.png)



### JSP九大内置对象

pageContext:表示页面的上下文的对象，封存的了其它的内置对象，封存了当前页面的运行信息

![image-20200803110816062](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803110816062.png)



### 四大作用域

![image-20200803111036498](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803111036498.png)



### 路径问题

建议使用绝对路径

![image-20200803111735975](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803111735975.png)



## EL

### EL表达式

![image-20200803120808470](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803120808470.png)



### EL表达式用法

![image-20200803121037815](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803121037815.png)



![image-20200803121611510](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803121611510.png)

![image-20200803121928110](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803121928110.png)



### JSTL标签库

*JSTL*（Java server pages standarded tag library，即JSP标准标签库）是由JCP（Java community Process）所制定的标准规范，它主要提供给Java Web开发人员一个标准通用的标签库

​	帮助我们在jsp页面中添加复杂的逻辑判断，避免逻辑代码和页面标签混在一起



![image-20200803122023816](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803122023816.png)



### 标签学习



![image-20200803132725967](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803132725967.png)

![image-20200803132632373](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803132632373.png)

![image-20200803134214345](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803134214345.png)



## 过滤器

![image-20200803142039585](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803142039585.png)



### 过滤器功能

![image-20200803142214815](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803142214815.png)



### 过滤器基本原理

![image-20200803142228298](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803142228298.png)

![image-20200803151542188](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803151542188.png)





## 事件监听器

![image-20200803152715731](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803152715731.png)







![image-20200803153351639](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803153351639.png)

![image-20200803153338250](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803153338250.png)

![image-20200803154435706](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20200803154435706.png)