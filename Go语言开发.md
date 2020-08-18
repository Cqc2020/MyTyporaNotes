#                                 Go语言开发

## Go语言学到什么程度可以找工作？

### Web开发相关问题：

1. 一个字符在互联网之旅——如何从客户端到服务端，又如何返回给客户端？

   ​	







2. Web框架运行时是怎么样的？





2. 如何应对高并发的用户请求？

   

3. 如何应对相互依赖的系统耦合？

4. MySQL如何应对高并发：读写分离，同步如何做的？

5. Redis缓存穿透，缓存雪崩，多级缓存和热点缓存的使用场景和技巧

6. MongoDb：如何使用Elasticsearch构建商品搜索系统？

7. 如何使用UML完成一个设计文档？

   

### 架构相关问题：

1. 设计模式：你知道多少种，怎么应用？
2. 如何对现有系统做微服务改造？
3. 分布式事务：如何保证多个系统间的数据一致？
4. 如何第一时间知道系统哪里出了问题？
5. 如何打造一体化的监控系统？

### 知识点

#### 多路复用器：一个调度器

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200711114454806.png" alt="image-20200711114454806" style="zoom: 50%;" />

#### fmt

1.Println：总是会在相邻参数的输出之间添加空格并在输出结束后添加换行符。返回写入的字节数和遇到的任何错误。



2.Fprintln：将其参数格式化并写入**w**。总是会在相邻参数的输出之间添加空格并在输出结束后添加换行符。返回写入的字节数和遇到的任何错误。



3.Sprintln：

#### 自定义类型和类型别名

##### 类型别名相当于软链接

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712010846009.png" alt="image-20200712010846009" style="zoom:80%;" />

##### 实例化是声明，初始化是赋值

##### pattern：映射的路径"/"

#### 类型断言和强制转换类型

##### 类型断言：

`t,ok:= a.(int)`有两个返回值,第一个是对应类型的值,第二个是bool类型的,类型判断是否正确

##### 强制转换：

```
func main() {
    var a float32 = 5.6
    var b int = 10
    fmt.Println (a * float32(b))
}
```



#### HTTP协议：

HTTP(Hypertext Transfer Protocol)超文本传输协议，它是一种详细规定了浏览器和万维网服务器之间互相通信的规则，通过因特网传输万维网文档的数据传送协议



<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712142627520.png" alt="image-20200712142627520" style="zoom:80%;" />



![image-20200712142950070](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712142950070.png)

![image-20200712143203717](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712143203717.png)

HTTP1.1和HTTP1.0

![image-20200712143427014](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712143427014.png)

![image-20200712143256575](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712143256575.png)

客户端与服务端通信时传输的内容称为  **<u>报文</u>**

![image-20200712143528814](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712143528814.png)

![image-20200712143637465](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712143637465.png)

![image-20200712143744397](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712143744397.png)

![image-20200712143828326](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712143828326.png)



![image-20200712152606132](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712152606132.png)

![image-20200712152623900](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712152623900.png)

![image-20200712152903565](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712152903565.png)



互联网：由通信的设备，如计算bai机、手du机等，组成的网络。
因特网：它是互联网中的一种，由成千上万台设备组成的网络。
万维网：由不同的文档、多媒体文件连通而形成的逻辑网络（其中每个节点都是一个顶级域名即网站）。
三者之间的关系：
互联网包含因特网，因特网包含万维网。即互联网>因特网>万维网

#### 单元测试

![image-20200712165915585](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712165915585.png)

![image-20200712170024485](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200712170024485.png)



### 学习的项目

#### 	海量用户在线聊天系统



#### 	GoWeb

##### 创建步骤：

1. 创建一个处理器函数： 传入参数必须是`(w http.ResponseWriter,r *http.Request)`

   ```go
   func handler(w http.ResponseWriter,r *http.Request) {
      fmt.Fprintln(w ,"Hello World!",r.URL.Path)
   }
   ```

2. 调用处理器，并创建路由：

   ```go
   func main()  {
      http.HandleFunc("/",handler)
   
      //创建路由
      http.ListenAndServe(":8080",nil)
   }
   ```



##### 创建方法一：使用默认多路复用器

```go
package main

import (
   "fmt"
   "net/http"
)


//创建一个处理器函数
func handler(w http.ResponseWriter,r *http.Request) {
   fmt.Fprintln(w ,"Hello World!",r.URL.Path)
}


func main()  {
    /*
    //调用http.HandleFunc函数:使用默认多路复用器DefaultServeMux
    //调用DefaultServeMux的HandleFunc方法
    
    func HandleFunc(pattern string, handler func(ResponseWriter, //*Request)) {
	DefaultServeMux.HandleFunc(pattern, handler)
    }
	*/

    /*
    //调用DefaultServeMux的Handle方法
    
    func (mux *ServeMux) HandleFunc(pattern string, handler func(ResponseWriter,      *Request)) {
	if handler == nil {
		panic("http: nil handler")
	}
	mux.Handle(pattern, HandlerFunc(handler))
   }
    */
    
    /*
    //HandlerFunc(handler):将handler强制转换成HandlerFunc类型，因为它有ServeHTTP方法
    
    type HandlerFunc func(ResponseWriter, *Request)

     // ServeHTTP calls f(w, r).
    func (f HandlerFunc) ServeHTTP(w ResponseWriter, r *Request) {
	     f(w, r)
    }
    */
    http.HandleFunc("/",handler)  

    //创建路由:调用http.ListenAndServe函数
   http.ListenAndServe(":8080",nil)
}
```





## 数据结构

数据结构是一门研究算法的学科，学好数据结构，可以编写出更加漂亮，更有效率的代码。

程序 = 数据结构 + 算法

