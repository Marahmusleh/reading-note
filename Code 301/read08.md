## APIs
1. **What does REST stand for?**
* *It stands for Representational State Transfer, it is an architectural style for building distributed systems based on hypermedia, this means that developers do not need to install libraries or additional software in order to take advantage of a REST API design
REST APIs are designed around a resources, which are any kind of object, data, or service that can be accessed by the client.*
2. **What is an identifer of a resource? Give an example.**
*It is an URI that uniquely identifies that resource, for example:*  https://adventure-works.com/orders/1 .
3. **What are the most common HTTP verbs?**
*GET, POST, PUT, PATCH, and DELETE.*
4. **What should the URIs be based on?**
*It should be based on nouns (the resource) and not verbs (the operations on the resource), and it should be short, unique, easy to type, and give the user an idea of what is linked.*
5. **Give an example of a good URI.**
https://adventure-works.com/orders
6. **What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?**
*They are the web APIs that expose a large number of small resources, they are bad because all web requests impose a load on the web server, the more requests, the bigger the load.*
7. **What status code does a successful GET request return?**
*returns HTTP status code 200 (OK).*
8. **What status code does an unsuccessful GET request return?**
*It should return 404 (Not Found).*
9. **What status code does a successful POST request return?**
*It returns HTTP status code 201 (Created), the response body contains a representation of the resource.*
10. **What status code does a successful DELETE request return?**
*The web server should respond with HTTP status code 204, but that the response body contains no further information.*
