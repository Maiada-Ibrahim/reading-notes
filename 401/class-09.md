# The HTTP Request Lifecycle

 ![](https://cdn.journaldev.com/wp-content/uploads/2015/03/java-HttpURLConnection.png)


- Step 1: Local Processing
<protocol>://<host><:optional port>/<path/to/resource><?query>
|http|://|www.example.com||:5000||/mainpage||?query=param&query2=param2|
we write link in our browser in this form the browser will take requested URLs, the operating system’s take queries, your router’s cache, and your DNS cache.

-  Step 2: Resolve an IP

our browser  fires off a DNS request using UDP take ip and try to find dns server and send respons 

-  Establish a TCP Connection
we send http request over  TCP, which is a transport layer protocol open connection delivery and ordered data transmission so know server and client acknowledgment of the connection from the other party.

-  Step 4: Send an HTTP Request
send requst this is host it have domain.com:8080 domain and port the respons genrate in form data or JSON.


-  Tearing Down and Cleaning Up
 browser will send the page


# cookie
 An HTTP cookie (web cookie, browser cookie) is a small piece of data that a server sends to a user's web browser. The browser may store the cookie and send it back to the same server with later requests. Typically, an HTTP cookie is used to tell if two requests come from the same browser—keeping a user logged in, for example. It remembers stateful information for the stateless HTTP protocol.

Cookies are mainly used for three purposes:

Session management
Logins, shopping carts, game scores, or anything else the server should remember

Personalization
User preferences, themes, and other settings

Tracking
Recording and analyzing user behavior

in java way of performing HTTP requests in Java — by using the built-in Java class HttpUrlConnection. 

Note that starting with JDK 11, Java provides a new API for performing HTTP requests, which is meant as a replacement for the HttpUrlConnection, the HttpClient API.

I didnt under stand the differnt with JDK 11 and before that???
