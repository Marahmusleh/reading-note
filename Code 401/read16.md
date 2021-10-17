# Authentication and Access Control

Application security boils down to two more or less independent problems: authentication (who are you?) and authorization (what are you allowed to do?). Sometimes people say “access control” instead of "authorization", which can get confusing, but it can be helpful to think of it that way because “authorization” is overloaded in other places. Spring Security has an architecture that is designed to separate authentication from authorization and has strategies and extension points for both.

## Authentication
The main strategy interface for authentication is AuthenticationManager

```
public interface AuthenticationManager {

  Authentication authenticate(Authentication authentication)
    throws AuthenticationException;
}
```
An AuthenticationManager can do one of 3 things in its authenticate() method:

* Return an Authentication (normally with authenticated=true) if it can verify that the input represents a valid principal.

* Throw an AuthenticationException if it believes that the input represents an invalid principal.

* Return null if it cannot decide.

## Customizing Authentication Managers
Spring Security provides some configuration helpers to quickly get common authentication manager features set up in your application. The most commonly used helper is the AuthenticationManagerBuilder, which is great for setting up in-memory, JDBC, or LDAP user details or for adding a custom UserDetailsService. The following example shows an application that configures the global (parent) AuthenticationManager:
```
@Configuration
public class ApplicationSecurity extends WebSecurityConfigurerAdapter {

   ... // web stuff here

  @Autowired
  public void initialize(AuthenticationManagerBuilder builder, DataSource dataSource) {
    builder.jdbcAuthentication().dataSource(dataSource).withUser("dave")
      .password("secret").roles("USER");
  }
  ```

## Web Security


Spring Security in the web tier (for UIs and HTTP back ends) is based on Servlet Filters, so it is helpful to first look at the role of Filters generally. The following picture shows the typical layering of the handlers for a single HTTP request.

* The client sends a request to the application, and the container decides which filters and which servlet apply to it based on the path of the request URI.

* At most, one servlet can handle a single request, but filters form a chain, so they are ordered.

* The order of the filter chain is very important, and Spring Boot manages it through two mechanisms: @Beans of type Filter can have an @Order or implement Ordered, and they can be part of a FilterRegistrationBean that itself has an order as part of its API.

* In a Spring Boot application, the security filter is a @Bean in the ApplicationContext, and it is installed by default so that it is applied to every request.

