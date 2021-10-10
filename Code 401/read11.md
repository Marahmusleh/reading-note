# Spring MVC

A Spring MVC is a Java framework which is used to build web applications. It follows the Model-View-Controller design pattern. It implements all the basic features of a core spring framework like Inversion of Control, Dependency Injection.

A Spring MVC provides an elegant solution to use MVC in spring framework by the help of DispatcherServlet. Here, DispatcherServlet is a class that receives the incoming request and maps it to the right resource such as controllers, models, and views.

## Spring model attributes

Spring MVC calls the pieces of data that can be accessed during the execution of views model attributes. The equivalent term in Thymeleaf language is context variables.

In Thymeleaf, these model attributes (or context variables in Thymeleaf jargon) can be accessed with the following syntax: ${attributeName}, where attributeName in our case is messages. This is a Spring EL expression. In short, Spring EL (Spring Expression Language) is a language that supports querying and manipulating an object graph at runtime.

You can access model attributes in views with Thymeleaf as follows:

```
<tr th:each="message : ${messages}">
            <td th:text="${message.id}">1</td>
            <td><a href="#" th:text="${message.title}">Title ...</a></td>
            <td th:text="${message.text}">Text ...</td>
        </tr>


```
## Request parameters

Request parameters can be easily accessed in Thymeleaf views. Request parameters are passed from the client to server like:

    https://example.com/query?q=Thymeleaf+Is+Great!

## Session attributes
In the below example we add mySessionAttribute to session:
```
    @RequestMapping({"/"})
        String index(HttpSession session) {
            session.setAttribute("mySessionAttribute", "someValue");
            return "index";
        }
```

Similarly to the request parameters, session attributes can be accessed by using the session. prefix:

    <p th:text="${session.mySessionAttribute}" th:unless="${session == null}">[...]</p>

## Spring beans

Thymeleaf allows accessing beans registered at the Spring Application Context with the @beanName syntax, for example:

    <div th:text="${@urlService.getApplicationUrl()}">...</div> 
