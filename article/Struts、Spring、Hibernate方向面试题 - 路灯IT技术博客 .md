**Hibernate工作原理及为什么要用？**-
原理：-
1.读取并解析配置文件-
2.读取并解析映射信息，创建SessionFactory-
3.打开Sesssion-
4.创建事务Transation-
5.持久化操作-
6.提交事务-
7.关闭Session-
8.关闭SesstionFactory-
为什么要用：-
1\. 对JDBC访问数据库的代码做了封装，大大简化了数据访问层繁琐的重复性代码。-
2\. Hibernate是一个基于JDBC的主流持久化框架，是一个优秀的ORM实现。他很大程度的简化DAO层的编码工作-
3\. hibernate使用Java反射机制，而不是字节码增强程序来实现透明性。-
4\. hibernate的性能非常好，因为它是个轻量级框架。映射的灵活性很出色。它支持各种关系数据库，从一对一到多对多的各种复杂关系。-
**2． Hibernate是如何延迟加载?**-
1\. Hibernate2延迟加载实现：a)实体对象 b)集合（Collection）-
2\. Hibernate3 提供了属性的延迟加载功能-
当Hibernate在查询数据的时候，数据并没有存在与内存中，当程序真正对数据的操作时，对象才存在与内存中，就实现了延迟加载，他节省了服务器的内存开销，从而提高了服务器的性能。-
**3．Hibernate中怎样实现类之间的关系?(如：一对多、多对多的关系)**-
类与类之间的关系主要体现在表与表之间的关系进行操作，它们都市对对象进行操作，我们程序中把所有的表与类都映射在一起，它们通过配置文件中的many-to-one、one-to-many、many-to-many、-
**4．说下Hibernate的缓存机制**-
1\. 内部缓存存在Hibernate中又叫一级缓存，属于应用事物级缓存-
2\. 二级缓存：-
a) 应用及缓存-
b) 分布式缓存-
条件：数据不会被第三方修改、数据大小在可接受范围、数据更新频率低、同一数据被系统频繁使用、非 关键数据-
c) 第三方缓存的实现-
**5． Hibernate的查询方式**-
Sql、Criteria,object comptosition-
Hql：-
1、 属性查询-
2、 参数查询、命名参数查询-
3、 关联查询-
4、 分页查询-
5、 统计函数-
**6．如何优化Hibernate？**-
1.使用双向一对多关联，不使用单向一对多-
2.灵活使用单向一对多关联-
3.不用一对一，用多对一取代-
4.配置对象缓存，不使用集合缓存-
5.一对多集合使用Bag,多对多集合使用Set-
6\. 继承类使用显式多态-
7\. 表字段要少，表关联不要怕多，有二级缓存撑腰-
-
**7． Struts工作机制？为什么要使用Struts？**-
工作机制：-
Struts的工作流程:-
在web应用启动时就会加载初始化ActionServlet,ActionServlet从-
struts-config.xml文件中读取配置信息,把它们存放到各种配置对象-
当ActionServlet接收到一个客户请求时,将执行如下流程.-
 -(1)检索和用户请求匹配的ActionMapping实例,如果不存在,就返回请求路径无效信息;-
 -(2)如果ActionForm实例不存在,就创建一个ActionForm对象,把客户提交的表单数据保存到ActionForm对象中;-
 -(3)根据配置信息决定是否需要表单验证.如果需要验证,就调用ActionForm的validate()方法;-
 -(4)如果ActionForm的validate()方法返回null或返回一个不包含ActionMessage的ActuibErrors对象, 就表示表单验证成功;-
 -(5)ActionServlet根据ActionMapping所包含的映射信息决定将请求转发给哪个Action,如果相应的 Action实例不存在,就先创建这个实例,然后调用Action的execute()方法;-
 -(6)Action的execute()方法返回一个ActionForward对象,ActionServlet在把客户请求转发给 ActionForward对象指向的JSP组件;-
 -(7)ActionForward对象指向JSP组件生成动态网页,返回给客户;-
为什么要用：-
JSP、Servlet、JavaBean技术的出现给我们构建强大的企业应用系统提供了可能。但用这些技术构建的系统非常的繁乱，所以在此之上，我们需要一个规则、一个把这些技术组织起来的规则，这就是框架，Struts便应运而生。-
基于Struts开发的应用由3类组件构成：控制器组件、模型组件、视图组件-
**8． Struts的validate框架是如何验证的？**-
在struts配置文件中配置具体的错误提示，再在FormBean中的validate()方法具体调用。-
**9．说下Struts的设计模式**-
MVC模式: web应用程序启动时就会加载并初始化ActionServler。用户提交表单时，一个配置好的ActionForm对象被创建，并被填入表单相应的数据，ActionServler根据Struts-config.xml文件配置好的设置决定是否需要表单验证，如果需要就调用ActionForm的Validate（）验证后选择将请求发送到哪个Action，如果Action不存在，ActionServlet会先创建这个对象，然后调用Action的execute（）方法。Execute（）从ActionForm对象中获取数据，完成业务逻辑，返回一个ActionForward对象，ActionServlet再把客户请求转发给ActionForward对象指定的jsp组件，ActionForward对象指定的jsp生成动态的网页，返回给客户。-
**10． spring工作机制及为什么要用?**-
1.spring mvc请所有的请求都提交给DispatcherServlet,它会委托应用系统的其他模块负责负责对请求进行真正的处理工作。-
2.DispatcherServlet查询一个或多个HandlerMapping,找到处理请求的Controller.-
3.DispatcherServlet请请求提交到目标Controller-
4.Controller进行业务逻辑处理后，会返回一个ModelAndView-
5.Dispathcher查询一个或多个ViewResolver视图解析器,找到ModelAndView对象指定的视图对象-
6.视图对象负责渲染返回给客户端。-
为什么用：-
{AOP 让开发人员可以创建非行为性的关注点，称为横切关注点，并将它们插入到应用程序代码中。使用 AOP 后，公共服务 （比如日志、持久性、事务等）就可以分解成方面并应用到域对象上，同时不会增加域对象的对象模型的复杂性。-
 IOC 允许创建一个可以构造对象的应用环境，然后向这些对象传递它们的协作对象。正如单词 倒置 所表明的，IOC 就像反 过来的 JNDI。没有使用一堆抽象工厂、服务定位器、单元素（singleton）和直接构造（straight construction），每一个对象都是用其协作对象构造的。因此是由容器管理协作对象（collaborator）。-
Spring即使一个AOP框架，也是一IOC容器。 Spring 最好的地方是它有助于您替换对象。有了 Spring，只要用 JavaBean 属性和配置文件加入依赖性（协作对象）。然后可以很容易地在需要时替换具有类似接口的协作对象。}-
-
**1、 简述你对IoC（Inversion of Control）的理解，描述一下Spring中实现DI（Dependency Injection）的几种方式。**-
**2、Spring提倡面向接口编程，请讲一下你对它的理解，它有什么好处。**-
**3、Spring的Bean有哪些作用域。**-
**4、简单描述Spring Framework与Struts的不同之处，整合Spring与Struts有哪些方法，哪种最好，为什么？**-
**5、Rails中大量使用Convention over Configuration的思想，SpringMVC在2.0后也引入了CoC，请简单描述一下SpringMVC的CoC。**-
**6、Hibernate中的update()和saveOrUpdate()的区别，session的load()和get()的区别。**-
**7、Spring对多种ORM框架提供了很好的支持，简单描述在Spring中使用Hibernate的方法，并结合事务管理。**-
**8、简述Spring的事务传播行为和隔离级别。**-
**答案：**-
-
1、好莱坞原则——不要打电话找我，我会打给你的。IoC将创建的职责从应用程序代码搬到了框架中。Spring对Setter注入和构造方法注入提供支持。（详见[http://martinfowler.com/articles/injection.html](https://www.eqishare.com/programming/827.html)，以及[http://www.redsaga.com/spring\_re](https://www.eqishare.com/programming/827.html) ... ctory-collaborators）-
-
2、在一个面向对象的系统中，系统的各种功能是由许许多多的不同对象协作完成的。在这种情况下，各个对象内部是如何实现自己的对系统设计人员来讲就不那么重要了；而各个对象之间的协作关系则成为系统设计的关键。小到不同类之间的通信，大到各模块之间的交互，在系统设计之初都是要着重考虑的，这也是系统设计的主要工作内容。（详见[http://deve.blogdriver.com/deve/415943.html](https://www.eqishare.com/programming/827.html)）-
-
3、singleton、prototype、request、session、global session、自定义（详见Spring Framework 2.0 Reference的3.4节bean的作用域）-
-
4、Spring是完整的一站式框架，而Struts仅是MVC框架，且着重于MVC中的C。Spring有三种方式整合Struts：使用 Spring 的 ActionSupport 类整合 Struts；使用 Spring 的 DelegatingRequestProcessor 覆盖 Struts 的 RequestProcessor；将 Struts Action 管理委托给 Spring 框架，动作委托最好。（详见使用Spring 更好地处理Struts 动作）-
Spring 2.0新增一种方式：AutowiringRequestProcessor。（详见[http://www.javaeye.com/topic/24239](https://www.eqishare.com/programming/827.html)）-
-
5、控制器Bean以Controller结尾可直接映射为地址，模型ModelAndView可以不用指定键名，可根据URL自动取得视图名。（详见Spring Framework 2.0 Reference的13.11节惯例优先原则）-
-
6、saveOrUpdate()方法可以实现update()的功能，但会多些步骤，具体如下：-
如果对象在该session中已经被持久化，不进行操作；-
对象的标识符属性(identifier property)在数据库中不存在或者是个暂时的值，调用save()方法保存它；-
如果session中的另一个对象有相同的标识符抛出一个异常；-
以上皆不符合则调用update()更新之。-
-
Session.load/get方法均可以根据指定的实体类和id从数据库读取记录，并返回与之对应的实体对象。其区别在于：-
如果未能发现符合条件的记录，get方法返回null，而load方法会抛出一个ObjectNotFoundException；-
load方法可返回实体的代理类实例，而get方法永远直接返回实体类；-
load方法可以充分利用内部缓存和二级缓存中的现有数据，而get方法则仅仅在内部缓存中进行数据查找，如没有发现对应数据，将越过二级缓存，直接调用SQL完成数据读取。-
-
7、在context中定义DataSource，创建SessionFactoy，设置参数；DAO类继承HibernateDaoSupport，实现具体接口，从中获得HibernateTemplate进行具体操作。在使用中如果遇到OpenSessionInView的问题，可以添加OpenSessionInViewFilter或OpenSessionInViewInterceptor。（详见Spring Framework 2.0 Reference的12.2节Hibernate）-
声明式事务需声明事务管理器，在context中设置<tx:advice>指定属性，用<aop:config>确定<aop:advisor>和<aop:pointcut>。（详见Spring Framework 2.0 Reference的9.5节声明式事务管理）-
-
8、传播行为分为六种：-
PROPAGATION\_REQUIRED--支持当前事务，如果当前没有事务，就新建一个事务。这是最常见的选择。-
PROPAGATION\_SUPPORTS--支持当前事务，如果当前没有事务，就以非事务方式执行。-
PROPAGATION\_MANDATORY--支持当前事务，如果当前没有事务，就抛出异常。-
PROPAGATION\_REQUIRES\_NEW--新建事务，如果当前存在事务，把当前事务挂起。-
PROPAGATION\_NOT\_SUPPORTED--以非事务方式执行操作，如果当前存在事务，就把当前事务挂起。-
PROPAGATION\_NEVER--以非事务方式执行，如果当前存在事务，则抛出异常。-
-
隔离级别：-
ISOLATION\_DEFAULT 这是一个PlatfromTransactionManager默认的隔离级别，使用数据库默认的事务隔离级别.另外四个与JDBC的隔离级别相对应-
ISOLATION\_READ\_UNCOMMITTED 这是事务最低的隔离级别，它充许别外一个事务可以看到这个事务未提交的数据。这种隔离级别会产生脏读，不可重复读和幻像读。-
ISOLATION\_READ\_COMMITTED 保证一个事务修改的数据提交后才能被另外一个事务读取。另外一个事务不能读取该事务未提交的数据。这种事务隔离级别可以避免脏读出现，但是可能会出现不可重复读和幻像读。-
ISOLATION\_REPEATABLE\_READ 这种事务隔离级别可以防止脏读，不可重复读。但是可能出现幻像读。它除了保证一个事务不能读取另一个事务未提交的数据外，还保证了避免下面的情况产生(不可重复读)。-
ISOLATION\_SERIALIZABLE 这是花费最高代价但是最可靠的事务隔离级别。事务被处理为顺序执行。除了防止脏读，不可重复读外，还避免了幻像读。-

-

本文转自 [https://www.eqishare.com/programming/827.html](https://www.eqishare.com/programming/827.html)，如有侵权，请联系删除。