# JavaWeb

## 1、HTML

**HTML:** HyperText Markup Language，超文本标记语言。

- 超文本：超越了文本的限制，比普通文本更强大。除了文字信息，还可以定义图片、音频、视频等内容。

- 标记语言：由标签构成的语言



 路径书写方式:

- 绝对路径:
  1. 绝对磁盘路径：C:\Users\Administrator\Desktop\HTML\img\news_logo.png
  2. 绝对网络路径：https://i2.sinaimg.cn/dy/deco/2012/0613/yocc20120613img01/news_logo.png

- 相对路径:

  1. **./** : 当前目录 , ./ 可以省略的

  2. **../**: 上一级目录



## 2、CSS

### 使用方式

![image-20231114021519200](https://gitee.com/sheldon_kkk/typora-image/raw/master/img/202311140215281.png)

### 颜色表达

![image-20231114091214679](https://gitee.com/sheldon_kkk/typora-image/raw/master/img/202311140912734.png)

### 选择器

```html
选择器名 {
css样式名：css样式值;
css样式名：css样式值;
}
```

- 元素选择器

  选择器的名字必须是标签的名字

- Id选择器

  选择器的名字前面需要加上#

- class选择器

  选择器的名字前面需要加上 .



### 超链接

- 标签: <a href="..." target="...">央视网
- 属性:
  - href: 指定资源访问的url
  - target: 指定在何处打开资源链接
    - _self: 默认值，在当前页面打开
    - _blank: 在空白页面打开

![image-20231114171354741](https://gitee.com/sheldon_kkk/typora-image/raw/master/img/202311141713863.png)

### 盒子模型

![image-20231114172641591](https://gitee.com/sheldon_kkk/typora-image/raw/master/img/202311141726698.png)

### 表格和表单

![image-20231114173228397](https://gitee.com/sheldon_kkk/typora-image/raw/master/img/202311141732466.png)

![image-20231114173922469](https://gitee.com/sheldon_kkk/typora-image/raw/master/img/202311141739596.png)

![image-20231114174737637](https://gitee.com/sheldon_kkk/typora-image/raw/master/img/202311141747716.png)

## 3、JavaScript

> JavaScript（简称：JS） 是一门跨平台、面向对象的脚本语言。是用来控制网页行为的，它能使网页可交互。

### 引入方式

**第一种方式：**内部脚本，将JS代码定义在HTML页面中

- JavaScript代码必须位于&lt;script&gt;&lt;/script&gt;标签之间
- 在HTML文档中，可以在任意地方，放置任意数量的&lt;script&gt;
- 一般会把脚本置于&lt;body&gt;元素的底部，可改善显示速度

**第二种方式：**外部脚本将， JS代码定义在外部 JS文件中，然后引入到 HTML页面中

- 外部JS文件中，只包含JS代码，不包含&ltscript&gt;标签
- 引入外部js的&lt;script&gt;标签，必须是双标签

### 基础语法

#### 变量

| 关键字 | 解释                                                         |
| ------ | ------------------------------------------------------------ |
| var    | 早期ECMAScript5中用于变量声明的关键字                        |
| let    | ECMAScript6中新增的用于变量声明的关键字，相比较var，let只在代码块内生效 |
| const  | 声明常量的，常量一旦声明，不能修改                           |

#### 数据类型和运算符

| number    | 数字（整数、小数、NaN(Not a Number)）              |
| --------- | -------------------------------------------------- |
| string    | 字符串，单双引皆可                                 |
| boolean   | 布尔。true，false                                  |
| null      | 对象为空                                           |
| undefined | 当声明的变量未初始化时，该变量的默认值是 undefined |

- ==：只比较值是否相等，不区分数据类型，哪怕类型不一致，==也会自动转换类型进行值得比较
- ===：不光比较值，还要比较类型，如果类型不一致，直接返回false

### 函数

#### 定义格式

```js
function 函数名(参数1,参数2..){
    要执行的代码
}
```

```html
<script>
     function add(a,b){
        return  a + b;
     }
</script>
```

#### 对象

第一类：基本对象,我们主要学习Array和JSON和String

![1668587953841](https://gitee.com/sheldon_kkk/typora-image/raw/master/img/202311170235190.png) 

第二类：BOM对象,主要是和浏览器相关的几个对象

| 对象名称  | 描述           |
| :-------- | :------------- |
| Window    | 浏览器窗口对象 |
| Navigator | 浏览器对象     |
| Screen    | 屏幕对象       |
| History   | 历史记录对象   |
| Location  | d地址栏对象    |

 

第三类：DOM对象，JavaScript中将html的每一个标签都封装成一个对象

- Document：整个文档对象
- Element：元素对象
- Attribute：属性对象
- Text：文本对象
- Comment：注释对象

如下图，左边是 HTML 文档内容，右边是 DOM 树

![1668796698067](https://gitee.com/sheldon_kkk/typora-image/raw/master/img/202311170236802.png)  

#### 获取DOM对象

| document.getElementById()         | 根据id属性值获取，返回单个Element对象    |
| --------------------------------- | ---------------------------------------- |
| document.getElementsByTagName()   | 根据标签名称获取，返回Element对象数组    |
| document.getElementsByName()      | 根据name属性值获取，返回Element对象数组  |
| document.getElementsByClassName() | 根据class属性值获取，返回Element对象数组 |

### 事件

#### 事件绑定

- 通过html标签中的事件属性进行绑定
- 通过DOM中Element元素的事件属性进行绑定

#### 常见事件

| 事件属性名  | 说明                     |
| ----------- | ------------------------ |
| onclick     | 鼠标单击事件             |
| onblur      | 元素失去焦点             |
| onfocus     | 元素获得焦点             |
| onload      | 某个页面或图像被完成加载 |
| onsubmit    | 当表单提交时触发该事件   |
| onmouseover | 鼠标被移到某元素之上     |
| onmouseout  | 鼠标从某元素移开         |

## 4、servlet

```
2. Servlet的继承关系 - 重点查看的是服务方法（service()）
    1. 继承关系
      javax.servlet.Servlet接口
          javax.servlet.GenericServlet抽象类
              javax.servlet.http.HttpServlet抽象子类

    2. 相关方法
      javax.servlet.Servlet接口:
        void init(config) - 初始化方法
        void service(request,response) - 服务方法
        void destory() - 销毁方法

      javax.servlet.GenericServlet抽象类：
        void service(request,response) - 仍然是抽象的

      javax.servlet.http.HttpServlet 抽象子类：
        void service(request,response) - 不是抽象的
        1. String method = req.getMethod(); 获取请求的方式
        2. 各种if判断，根据请求方式不同，决定去调用不同的do方法
            if (method.equals("GET")) {
                this.doGet(req,resp);
            } else if (method.equals("HEAD")) {
                this.doHead(req, resp);
            } else if (method.equals("POST")) {
                this.doPost(req, resp);
            } else if (method.equals("PUT")) {
        3. 在HttpServlet这个抽象类中，do方法都差不多:
        protected void doGet(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
            String protocol = req.getProtocol();
            String msg = lStrings.getString("http.method_get_not_supported");
            if (protocol.endsWith("1.1")) {
                resp.sendError(405, msg);
            } else {
                resp.sendError(400, msg);
            }
        }
    3.小结：
    1) 继承关系： HttpServlet -> GenericServlet -> Servlet
    2) Servlet中的核心方法： init() , service() , destroy()
    3) 服务方法： 当有请求过来时，service方法会自动响应（其实是tomcat容器调用的）
            在HttpServlet中我们会去分析请求的方式：到底是get、post、head还是delete等等
            然后再决定调用的是哪个do开头的方法
            那么在HttpServlet中这些do方法默认都是405的实现风格-要我们子类去实现对应的方法，否则默认会报405错误
    4) 因此，我们在新建Servlet时，我们才会去考虑请求方法，从而决定重写哪个do方法


3. Servlet的生命周期
    1） 生命周期：从出生到死亡的过程就是生命周期。对应Servlet中的三个方法：init(),service(),destroy()
    2） 默认情况下：
        第一次接收请求时，这个Servlet会进行实例化(调用构造方法)、初始化(调用init())、然后服务(调用service())
        从第二次请求开始，每一次都是服务
        当容器关闭时，其中的所有的servlet实例会被销毁，调用销毁方法
    3） 通过案例我们发现：
        - Servlet实例tomcat只会创建一个，所有的请求都是这个实例去响应。
        - 默认情况下，第一次请求时，tomcat才会去实例化，初始化，然后再服务.这样的好处是什么？ 提高系统的启动速度 。 这样的缺点是什么？ 第一次请求时，耗时较长。
        - 因此得出结论： 如果需要提高系统的启动速度，当前默认情况就是这样。如果需要提高响应速度，我们应该设置Servlet的初始化时机。
    4） Servlet的初始化时机：
        - 默认是第一次接收请求时，实例化，初始化
        - 我们可以通过<load-on-startup>来设置servlet启动的先后顺序,数字越小，启动越靠前，最小值0
    5） Servlet在容器中是：单例的、线程不安全的
        - 单例：所有的请求都是同一个实例去响应
        - 线程不安全：一个线程需要根据这个实例中的某个成员变量值去做逻辑判断。但是在中间某个时机，另一个线程改变了这个成员变量的值，从而导致第一个线程的执行路径发生了变化
        - 我们已经知道了servlet是线程不安全的，给我们的启发是： 尽量的不要在servlet中定义成员变量。如果不得不定义成员变量，那么不要去：①不要去修改成员变量的值 ②不要去根据成员变量的值做一些逻辑判断


```



##5、Http

```
1、Http协议

   1） Http 称之为 超文本传输协议
   2） Http是无状态的
   3） Http请求响应包含两个部分：请求和响应

     - 请求：
       请求包含三个部分： 1.请求行 ； 2.请求消息头 ； 3.请求主体
       1)请求行包含是三个信息： 1. 请求的方式 ； 2.请求的URL ； 3.请求的协议（一般都是HTTP1.1）
       2)请求消息头中包含了很多客户端需要告诉服务器的信息，比如：我的浏览器型号、版本、我能接收的内容的类型、我给你发的内容的类型、内容的长度等等
       3)请求体，三种情况
         get方式，没有请求体，但是有一个queryString
         post方式，有请求体，form data
         json格式，有请求体，request payload
     - 响应：
       响应也包含三本： 1. 响应行 ； 2.响应头 ； 3.响应体
       1)响应行包含三个信息：1.协议 2.响应状态码(200) 3.响应状态(ok)
       2)响应头：包含了服务器的信息；服务器发送给浏览器的信息（内容的媒体类型、编码、内容长度等）
       3)响应体：响应的实际内容（比如请求add.html页面时，响应的内容就是<html><head><body><form....）

2、会话

   1） Http是无状态的
       - HTTP 无状态 ：服务器无法判断这两次请求是同一个客户端发过来的，还是不同的客户端发过来的
       - 无状态带来的现实问题：第一次请求是添加商品到购物车，第二次请求是结账；如果这两次请求服务器无法区分是同一个用户的，那么就会导致混乱
       - 通过会话跟踪技术来解决无状态的问题。

   2） 会话跟踪技术
       - 客户端第一次发请求给服务器，服务器获取session，获取不到，则创建新的，然后响应给客户端
       - 下次客户端给服务器发请求时，会把sessionID带给服务器，那么服务器就能获取到了，那么服务器就判断这一次请求和上次某次请求是同一个客户端，从而能够区分开客户端
       
       - 常用的API：
         request.getSession() -> 获取当前的会话，没有则创建一个新的会话
         request.getSession(true) -> 效果和不带参数相同
         request.getSession(false) -> 获取当前会话，没有则返回null，不会创建新的
         session.getId() -> 获取sessionID
         session.isNew() -> 判断当前session是否是新的
         session.getMaxInactiveInterval() -> session的非激活间隔时长，默认1800秒
         session.setMaxInactiveInterval()
         session.invalidate() -> 强制性让会话立即失效
         ....

   3） session保存作用域
     - session保存作用域是和具体的某一个session对应的
     - 常用的API：
       void session.setAttribute(k,v)
       Object session.getAttribute(k)
       void removeAttribute(k)

3、服务器内部转发以及客户端重定向

   1）服务器内部转发 : request.getRequestDispatcher("...").forward(request,response);

     - 一次请求响应的过程，对于客户端而言，内部经过了多少次转发，客户端是不知道的
     - 地址栏没有变化
   2）客户端重定向： response.sendRedirect("....");
     - 两次请求响应的过程。客户端肯定知道请求URL有变化
     - 地址栏有变化
     
4、保存作用域
   原始情况下，保存作用域我们可以认为有四个： page（页面级别，现在几乎不用） , request（一次请求响应范围） , session（一次会话范围） , application（整个应用程序范围）
   1） request：一次请求响应范围
   2） session：一次会话范围有效
   3） application： 一次应用程序范围有效

```





##6、thymeleaf

```
Thymeleaf - 视图模板技术
1） 添加thymeleaf的jar包
2） 新建一个Servlet类ViewBaseServlet
3） 在web.xml文件中添加配置

   - 配置前缀 view-prefix
   - 配置后缀 view-suffix
     4） 使得我们的Servlet继承ViewBaseServlet

5） 根据逻辑视图名称 得到 物理视图名称
//此处的视图名称是 index
//那么thymeleaf会将这个 逻辑视图名称 对应到 物理视图 名称上去
//逻辑视图名称 ：   index
//物理视图名称 ：   view-prefix + 逻辑视图名称 + view-suffix
//所以真实的视图名称是：      /       index       .html
super.processTemplate("index",request,response);
6） 使用thymeleaf的标签
  th:if   ,  th:unless   , th:each   ,   th:text
```

