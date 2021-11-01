
## Spring Authorization

this instrction to build a sample app we will use login and sign up page using  OAuth 2.0 and spring boot

1. create new project  [link](https://start.spring.io) using this link to create Spring Boot application faster chosse it as  Gradle Project ,langugae java ,Spring Boot 2.5.6, the name of project ,package jar,java 11,and add basic Dependencies
Spring Boot DevTools,Spring Web,Thymeleaf  

2. Add a Home page ; create home.html in the src/main/resources/static as tamplte 

          dependencies {
     	implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
    	implementation 'org.springframework.boot:spring-boot-starter-security'
    	implementation 'org.springframework.boot:spring-boot-starter-thymeleaf'
    	implementation 'org.springframework.boot:spring-boot-starter-web'
    	implementation 'org.thymeleaf.  extras:thymeleaf-extras-springsecurity5'
    	developmentOnly 'org.springframework.boot:spring-boot-devtools'
    	runtimeOnly 'org.postgresql:postgresql'
    	testImplementation 'org.springframework.boot:spring-boot-starter-test'
    	testImplementation 'org.springframework.security:spring-security-test'

       }

add dependencies to be like that

3. Securing the Application with GitHub and Spring Security
- we add that to dependencies to secure your app with OAuth 2.0 by default.

        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-oauth2-client</artifactId>

- Add a New GitHub app

Configure application.yml add some code 

Boot up the application run the app at this http://localhost:8080







## Add a Logout Button

use rout /logout

at class SocialApplication.java  add this code 

       @Override
     protected void configure(HttpSecurity http) throws Exception {
	// @formatter:off
    http
        // ... existing code here
        .logout(l -> l
            .logoutSuccessUrl("/").permitAll()
        )
        // ... existing code here
    // @formatter:on
      }
