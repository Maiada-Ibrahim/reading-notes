# Spring Security Architecture

To have security in web app we use filters or we can say method annotations.


   ## Authentication and Access Control
  -  we can say access control that mean who are you that is authentication  
   and what you can do that is authorization 



- it has only one method: AuthenticationManager

      public interface AuthenticationManager {

        Authentication authenticate(Authentication authentication)
        throws AuthenticationException;
        }


what can do ?

it return an Authentication 
authenticated = 


true --> input represents a valid principal.

Throw --> input represents an invalid principal.

Return null--> if it cannot decide.

- The diff btween AuthenticationProvider and AuthenticationManager?

AuthenticationProvider
  it has an extra method to allow the caller to query whether it supports a given Authentication type

 So an AuthenticationManager hierarchy using ProviderManager

example:

     public interface AuthenticationProvider {

	Authentication authenticate(Authentication authentication)
			throws AuthenticationException;

	boolean supports(Class<?> authentication);
     }



## Customizing Authentication Managers
- AuthenticationManagerBuilder is use as a helper or setting up in-memory, JDBC, or LDAP user details or for adding a custom UserDetailsService

- if we use AuthenticationManagerBuilder  withe @Autowired that makes bulid is global if use it with @Override then  used only to build a “local” AuthenticationManager

--------------------------------

# Authorization or Access Control

- after Authentication go to Authorization is use AccessDecisionManager strategy  we can use three implementations
all delegate to a chain of AccessDecisionVoter instances

- we pass ConfigAttribute attribute is an interface it contain decoration of the secure Object and  permission required to access it using one method (which is quite generic and returns a String)

------------------------------
Web Security
we us Servlet Filters for Web Security in the web tier (for UIs and HTTP back ends)
![](https://github.com/spring-guides/top-spring-security-architecture/raw/main/images/filters.png)
send requst--> container decides which filters-->move from filter to another from chain-->a filter can veto the rest of the chain-->A filter can also modify the request or the response used in the downstream filters and servlet

so the order is important we use two way
1. @Beans of type Filter can have an @Order or implement Ordered, and they can be part of a FilterRegistrationBean that itself has an order as part of its API.
2. A vanilla Spring Boot application with no custom security configuration has a several (call it n) filter chains, where usually n=6.


------------------------------

## Method Security
 Spring Security using the same format of ConfigAttribute strings  but in a different place in your code.

## Working with Threads
Spring Security is fundamentally thread-bound,to be available to  alot of consumers 
that mean we have ThreadLocal
contain SecurityContextHolder has methods SecurityContext which contain Authentication 

also you can access  user authenticated  now using @RequestMapping

---------------------------

# Spring Auth Cheat Sheet

- Set up model and repo

- create a controller for that model.

- implementation of usersdetails service and implements user details.

- Application User implements user details
 override the neccesary methods and make them return true.

- Configure web security config class it should :

has user detail service.
password encoder autowired.
configure authmanagerbuilder.
Configure http security by overriding the configure method.
Form login .
Add matchers.
logout functionality.
- Add Login page form.
- Add signup page.
- validate the controllers of both.