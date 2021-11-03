# Spring and Sockets
WebSocket create the connection btween a web browser and a server  by defines an API this channels full-duplex communication channels that mean server or client can send data any time

STOMP Simple Text Oriented Message Protocol use because clients and message brokers exchange text frames that contain a mandatory command, optional headers, and an optional body 

![](https://suhasjavablog.files.wordpress.com/2019/12/1_sfhlx5nhl8t_s0k2dg6vpw.png)


1. create spring application [link](https://start.spring.io) we can use Spring Initializr to  adding this  dependency 
- implementation 'org.webjars:webjars-locator-core'
- implementation 'org.webjars:sockjs-client:1.0.2' 
- implementation 'org.webjars:stomp-websocket:2.3.3' 
- implementation 'org.webjars:bootstrap:3.3.7'
- implementation 'org.webjars:jquery:3.1.1-1



2. create two class as modles to handle the messages (json formate) first one  public class HelloMessage 
           
              public HelloMessage(String name) {
            this.name = name;
                      }
 
                 public String getName() {
              return name;
                }



                 public void setName(String name) {
              this.name = name;
               }
               }




 - the second class

                package com.example.messagingstompwebsocket;

                   public class Greeting {
     
                     private String content;
     
                    public Greeting() {
                 }
     
                   public Greeting(String content) {
                     this.content = content;
              }
     
                       public String getContent() {
                       return content;
                  }


3.  i think we must make a Message-handling Controller to second class

         @Controller
          public class GreetingController {
            @MessageMapping("/hello")
         @SendTo("/topic/greetings")
         public Greeting greeting(HelloMessage message) throws Exception {
             Thread.sleep(1000); // simulated delay
          return new Greeting("Hello, " + HtmlUtils.htmlEscape(message.getName()) + "!");
         }                
            }


4. Configure Spring for STOMP messaging 
- create a class (name it WebSocketConfig) 
   that implement WebSocketMessageBrokerConfigurer interface 

- override configureMessageBroker and registerStompEndpoints methods 


       @Configuration
       @EnableWebSocketMessageBroker
        public class WebSocketConfig implements WebSocketMessageBrokerConfigurer {
             @Override
        public void configureMessageBroker(MessageBrokerRegistry config) {
   config.enableSimpleBroker("/topic");
   config.setApplicationDestinationPrefixes("/app");
   }
 
        @Override
        public void registerStompEndpoints(StompEndpointRegistry registry) {
          registry.addEndpoint("/gs-guide-websocket").withSockJS();
          }

            }   



5. Create a Browser Client: 

Create  html page to check the resource in this page we will

-imports the SockJS and STOMP  libraries that will be used to communicate with our server through STOMP over websocket

-  import app.js, which contains the logic of our client application.



6. run the app