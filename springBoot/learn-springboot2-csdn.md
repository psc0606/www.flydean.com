Spring Boot 2.X系列教程:七天从无到有掌握Spring Boot-持续更新

# 简介

自从Spring横空出世之后，Spring就成了事实上的J2EE标准。Spring作为一个轻量级的J2EE应用框架，就是针对EJB的复杂特性而设计的，最后毫无疑问，Spring凭借它的简洁，可理解性和可用性赢得了最后的胜利。

Spring从最初的xml配置到后面的注解配置，一直都在不断的进步，但是可不可以，能不能够有一种方法可以不要配置就能运行Spring应用程序？于是Spring Boot应运而生。

> 更多内容请访问[www.flydean.com](www.flydean.com)

SpringBoot是由Pivotal团队在2013年开始研发、2014年4月发布第一个版本的全新开源的轻量级框架。

![](https://img-blog.csdnimg.cn/20200519220936364.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_0,text_aHR0cDovL3d3dy5mbHlkZWFuLmNvbQ==,size_35,color_8F8F8F,t_70)

Spring Boot让你的企业级应用更加容易编写，更加容易运行。并且集成了很多常用的第三方lib库，免去了大家手动引用配置的麻烦。

使用最简单的配置运行最复杂的Spring应用程序，应该就是Spring Boot的终极目标。

同时Spring Boot尽可能的摆脱xml配置，能够提供包括独立运行，服务器内部运行等各种运行方式，方便我们的使用。

# Spring Boot的基本操作

最新的Spring Boot版本是2.3.0.RELEASE，它需要至少JDK8的支持和Spring Framework 5.2.6.RELEASE。

在构建工具方面，需要Maven 3.3+ 和 Gradle 6.3+。

服务器方面，Spring Boot内置三个服务器：Tomcat 9.0，Jetty 9.4和Undertow 2.0。Spring Boot需要部署在Servlet 3.1+的环境中才能正常运行。

在安装方面，Spring Boot有两种安装方式，第一种就是在Maven或者Gradle中以jar包的形式引入，这种方式的好处就是直观，并且Spring Boot的配置都是在项目中可以看到的。

第二种方式就是使用Spring Boot CLI，通过cli还可以运行groovy脚本。

下面列出了Spring Boot中的几个基本模块：

![](https://img-blog.csdnimg.cn/20200519230601826.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_0,text_aHR0cDovL3d3dy5mbHlkZWFuLmNvbQ==,size_35,color_8F8F8F,t_70)

下面列出的教程文件，大家可以一步一步的去参考运行，运行完毕相信大家对Spring Boot会有一个深刻的理解。

* [使用Spring Boot搭建你的第一个应用程序](https://blog.csdn.net/superfjj/article/details/104059204)
* [如何在Spring boot中修改默认端口](https://blog.csdn.net/superfjj/article/details/104067691)
* [Spring Boot Starters介绍](https://blog.csdn.net/superfjj/article/details/104073953)
* [Spring boot自定义parent POM](https://blog.csdn.net/superfjj/article/details/104086259)
* [使用spring boot创建fat jar APP](https://blog.csdn.net/superfjj/article/details/104094146)
* [spring boot 使用maven和fat jar/war运行应用程序的对比](https://blog.csdn.net/superfjj/article/details/104098555)
* [Spring Boot注解](https://blog.csdn.net/superfjj/article/details/104112926)
* [Spring Boot @EnableAutoConfiguration和 @Configuration的区别](https://blog.csdn.net/superfjj/article/details/104152621)
* [自定义spring boot的自动配置](https://blog.csdn.net/superfjj/article/details/104165368)
* [在Spring Boot中配置web app](https://blog.csdn.net/superfjj/article/details/104178295)
* [从Spring迁移到Spring Boot](https://blog.csdn.net/superfjj/article/details/104192355)
* [Spring Boot中的Properties](https://blog.csdn.net/superfjj/article/details/104243859)
* [SpringBoot @ConfigurationProperties详解](https://blog.csdn.net/superfjj/article/details/104258460)
* [在Spring Boot中加载初始化数据](https://blog.csdn.net/superfjj/article/details/104273470)
* [Spring Boot的exit code](https://blog.csdn.net/superfjj/article/details/104290745)
* [Shutdown SpringBoot App](https://blog.csdn.net/superfjj/article/details/104306985)
* [Spring boot 自定义banner](https://blog.csdn.net/superfjj/article/details/104338704)
* [Spring Boot filter](https://blog.csdn.net/superfjj/article/details/104353494)
* [Spring Boot中使用@JsonComponent](https://blog.csdn.net/superfjj/article/details/104387103)
* [Spring Boot国际化支持](https://blog.csdn.net/superfjj/article/details/104422396)
  
# Spring Boot的构建和部署

开发java项目少不了要用到maven或者gradle,对比gradle而言，可能maven要更加常用一些。要使用maven那就必要要安装maven,如果有些用户不想安装maven怎么办？或者说用户不想全局安装maven,那么可以使用项目级别的Maven Wrapper来实现这个功能。

如果大家使用IntelliJ IDEA来开发Spring boot项目, 如果选择从Spring Initializr来创建项目，则会在项目中自动应用Maven Wrapper。简单点说就是在项目目录下面会多出两个文件： mvnw 和 mvnw.cmd。

* [Maven Wrapper简介](https://blog.csdn.net/superfjj/article/details/104106831)

当我们创建好了Spring Boot应用程序之后，怎么在生成环境中运行呢？如果只是以原始的java -jar 的方式来运行的话，不能保证程序的健壮性和稳定性，最好的办法是将程序注册成为服务来使用。

* [将Spring Boot应用程序注册成为系统服务](https://blog.csdn.net/superfjj/article/details/104473727)

# Spring Boot工具

Spring Boot Actuator 在Spring Boot第一个版本发布的时候就有了，它为Spring Boot提供了一系列产品级的特性：监控应用程序，收集元数据，运行情况或者数据库状态等。

使用Spring Boot Actuator我们可以直接使用这些特性而不需要自己去实现，它是用HTTP或者JMX来和外界交互。

* [Spring Boot Actuator](https://blog.csdn.net/superfjj/article/details/104232517)

Spring Boot为我们提供了一个便捷的开发Spring Boot应用程序的环境，同时为了方便我们的开发Spring Boot应用程序，Spring Boot 推出了Spring Boot devtool的工具来方便我们更加快速的开发和测试Spring Boot应用程序。

* [Spring Boot devtool的使用](https://blog.csdn.net/superfjj/article/details/104438817)

前面我们讲了Spring Boot的Actuator。但是Spring Boot Actuator只是提供了一个个的接口，需要我们自行集成到监控程序中。今天我们将会讲解一个优秀的监控工具Spring Boot Admin。 它采用图形化的界面，让我们的Spring Boot管理更加简单。

* [Spring Boot Admin的使用](https://blog.csdn.net/superfjj/article/details/104454803)



# Spring Boot的测试

测试是一个应用程序必须要有的功能，它可以保证程序的健壮性，和稳定性，尤其是在CI环境中更是如此。

Spring Boot有专门的spring-boot-starter-test，通过使用它可以很方便的在Spring Boot进行测试。

* [Spring Boot中的测试](https://blog.csdn.net/superfjj/article/details/104206183)
* [Spring Boot的TestRestTemplate使用](https://blog.csdn.net/superfjj/article/details/104219960)


# Spring Boot中使用JPA

JPA的全称是Java Persistence API (JPA)，他是一个存储API的标准，而Spring data JPA就是对JPA的一种实现，可以让我们方便的对数据进行存取。按照约定好的方法命名规则写dao层接口，从而在不实现接口的情况下，实现对数据库的访问和操作。同时提供了很多除了CRUD之外的功能，如分页、排序、复杂查询等等。

Spring data JPA可以看做是对Hibernate的二次封装。在Spring Boot中使用JPA是非常的方便。

* [Spring Boot 之Spring data JPA简介](https://blog.csdn.net/superfjj/article/details/104490203)
* [Spring Boot JPA中java 8 的应用](https://blog.csdn.net/superfjj/article/details/104530224)
* [Spring Boot中Spring data注解的使用](https://blog.csdn.net/superfjj/article/details/104550936)
* [在Spring Boot使用H2内存数据库](https://blog.csdn.net/superfjj/article/details/104569151)
* [在Spring Boot中使用内存数据库](https://blog.csdn.net/superfjj/article/details/104586722)
* [Spring Boot JPA中使用@Entity和@Table](https://blog.csdn.net/superfjj/article/details/104604957)
* [Spring Boot JPA的查询语句](https://blog.csdn.net/superfjj/article/details/104625730)
* [Spring Boot JPA中关联表的使用](https://blog.csdn.net/superfjj/article/details/104646904)
* [Spring Boot JPA 中transaction的使用](https://blog.csdn.net/superfjj/article/details/104689037)

# Spring Boot和第三方系统的集成

Spring Boot为了开发人员的方便，已经集成了很多第三方的服务，我们可以直接使用他们。

甚至如果Spring官方没有提供集成的话，第三方系统本身也会提供跟Spring的集成，因为Spring的使用实在是太广泛了。

* [Spring Boot中使用Swagger CodeGen生成REST client](https://blog.csdn.net/superfjj/article/details/104369249)


# 总结

本文将会持续更新Spring Boot 2.x相关的文章，大家觉得不错可以点个关注，同时如果大家有建议的教程内容，欢迎大家留言回复，我会尽量补齐，谢谢大家的支持！

> 本文作者：flydean程序那些事
> 
> 本文链接：[http://www.flydean.com/learn-spring-boot/](http://www.flydean.com/learn-spring-boot/)
> 
> 本文来源：flydean的博客
> 
> 欢迎关注我的公众号:程序那些事，更多精彩等着您！

