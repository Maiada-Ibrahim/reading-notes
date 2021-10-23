# Spring
A Spring MVC is a Java framework which is used to build web applications. It follows the Model-View-Controller design pattern. It implements all the basic features of a core spring framework like Inversion of Control, Dependency Injection.

A Spring MVC provides an elegant solution to use MVC in spring framework by the help of DispatcherServlet. Here, DispatcherServlet is a class that receives the incoming request and maps it to the right resource such as controllers, models, and views.

- Model - A model contains the data of the application. A data can be a single object or a collection of objects.

- Controller - A controller contains the business logic of an application. Here, the @Controller annotation is used to mark the class as the controller.

- View - A view represents the provided information in a particular format. Generally, JSP+JSTL is used to create a view page. Although spring also supports other view technologies such as Apache Velocity, Thymeleaf and FreeMarker.
Front Controller - In Spring Web MVC, the DispatcherServlet class works as the front controller. It is responsible to manage the flow of the Spring MVC application.
## Understanding the flow of Spring Web MVC
![](../img/401/class-111.png)

## Serving Web Content with Spring MVC
- we will have app with  a static home page and accept HTTP GET requests at: http://localhost:8080/greeting.
- respond “Hello, World!” because that body of http


How to complete this guide

Download and unzip the source repository for this guide, or clone it using Git: git clone https://github.com/spring-guides/gs-serving-web-content.git

cd into gs-serving-web-content/initial

Jump ahead to Create a Web Controller.

When you finish, you can check your results against the code in gs-serving-web-content/complete.

- Starting with Spring Initializr
- Create a Web Controller:identify the controller by the @Controller

- Enabling Dev Tools Module
To enable dev tools in spring boot application is very easy. Just add the spring-boot-devtools dependency in your build file.
## How to access data in Thymeleaf templates
Thymeleaf is a popular server-side template engine for Java applications. You can easily integrate it into a Spring Boot project to develop web applications.

- Spring Model Attributes
- The simplest way is to use the Model's addAttribute() method
 - you could also return a ModelAndView object with model attributes included
 - You can also use the @ModelAttribute annotation to expose common model attributes

------------------------------------------------------------

  ## Request parameters:
  we have collecter have request parameter we accses param.
  ## Session attributes
we use session. 
## ServletContext attributes
table we access it #servletContext.
## Spring beans
Spring beans are the objects which are created and managed completely by spring container.

These beans are the heart of the application.

Beans can be defined in spring either by using XML configuration or by using Annotation.

In XML configuration, bean can be defined using < bean > tag inside < beans > tag.

In Annotation configuration , bean can be defined using the annotations like @Component,@Service,@Controller,@Repository on top of the class definition.




