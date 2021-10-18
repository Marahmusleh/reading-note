# Spring Boot and OAuth2
OAuth2 is an authorization framework that enables the application Web Security to access the resources from the client. To build an OAuth2 application, we need to focus on the Grant Type (Authorization code), Client ID and Client secret.

## Single Sign On With GitHub
In this section, you’ll create a minimal application that uses GitHub for authentication. This will be quite easy by taking advantage of the autoconfiguration features in Spring Boot.

### Creating a New Project
First, you need to create a Spring Boot application, which can be done in a number of ways. The easiest is to go to https://start.spring.io and generate an empty project (choosing the "Web" dependency as a starting point). Equivalently, do this on the command line:
```
$ mkdir ui && cd ui
$ curl https://start.spring.io/starter.tgz -d style=web -d name=simple | tar -xzvf -COPY
```
You can then import that project into your favorite IDE (it’s a normal Maven Java project by default), or just work with the files and mvn on the command line.

### Generating a 401 in the Server
A 401 response will already be coming from Spring Security if the user cannot or does not want to login with GitHub, so the app is already working if you fail to authenticate (e.g. by rejecting the token grant).

To spice things up a bit, you can extend the authentication rule to reject users that are not in the right organization.

You can use the GitHub API to find out more about the user, so you’ll just need to plug that into the right part of the authentication process.

Fortunately, for such a simple use case, Spring Boot has provided an easy extension point: If you declare a @Bean of type OAuth2UserService, it will be used to identify the user principal. 