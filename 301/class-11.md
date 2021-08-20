# Authentication
![](https://d33wubrfki0l68.cloudfront.net/99bea281c4d8758b97fe07ded0136019b0ed75f6/3da15/assets-jekyll/blog/oauth/oauth-actors-cd8b4861e839037400d8521e97c5d8cf0cb029add65d1036488991c7e85dcb72.png)
## What is OAuth?
OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.
## Give an example of what using OAuth would look like.
The simplest example of OAuth is when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon. You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permission gained from the second website.
## How does OAuth work? What are the steps that it takes to authenticate the user?
1. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
2. The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
3. The first site gives this token and secret to the initiating user’s client software.
4. The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
5. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
6. The user approves (or their software silently approves) a particular transaction type at the first website.
7. The user is given an approved access token (notice it’s no longer a request token).
8. The user gives the approved access token to the first website.
9. The first website gives the access token to the second website as proof of authentication on behalf of the user.
10. The second website lets the first website access their site on behalf of the user.
11. The user sees a successfully completed transaction occurring.
12. OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).
## What is OpenID?
 OpenID is about authentication: as a commenter on StackOverflow pithily put it: "OpenID is for humans logging into machines, OAuth is for machines logging into machines on behalf of humans."


 -------------------------------------------
 # Authorization and Authentication flows
 ## What is the difference between authorization and authentication?
 |Authentication   	 |	Authorization|
 |-------------------|-------------------------|
|Determines whether users are who they claim to be|Determines what users can and cannot access|
|Challenges the user to validate credentials (for example, through passwords, answers to security questions, or facial recognition)|Verifies whether access is allowed through policies and rules|
|Usually done before authorization|Usually done after successful authentication|
|Generally, transmits info through an ID Token|Generally, transmits info through an Access Token|
|Generally governed by the OpenID Connect (OIDC) protocol|Generally governed by the OAuth 2.0 framework|
|Example: Employees in a company are required to authenticate through the network before accessing their company email|Example: After an employee successfully authenticates, the system determines what information the employees are allowed to access|







## What is Authorization Code Flow?
![](https://i2.wp.com/blogs.innovationm.com/wp-content/uploads/2019/07/blog-open1.png?resize=625%2C348)
is used to obtain an access token to authorize API requests. Authorization code flow is the most flexible of the three supported authorization flows and is the recommended method of obtaining an access token for the API. This authorization flow is best suited to applications that have access to secure, private storage such as web applications deployed on a server. Other authorization flows are available to obtain an access token that may be suitable for your application.
## What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?

During authentication, mobile and native applications can use the Authorization Code Flow, but they require additional security. Additionally, single-page apps have special challenges. To mitigate these, OAuth 2.0 provides a version of the Authorization Code Flow which makes use of a Proof Key for Code Exchange (PKCE).
## What is Implicit Flow with Form Post?
 it does offer a streamlined workflow if the application needs only an ID token to perform user authentication.

   The client can request an access token using only its client
   credentials (or other supported means of authentication) when the
   client is requesting access to the protected resources under its
   control, or those of another resource owner that have been previously
   arranged with the authorization server (the method of which is beyond
   the scope of this specification).
## What is Device Authorization Flow?
The OAuth 2.0 device authorization grant is designed for Internet-
   connected devices that either lack a browser to perform a user-agent-
   based authorization or are input constrained to the extent that
   requiring the user to input text in order to authenticate during the
   authorization flow is impractical.  It enables OAuth clients on such
   devices (like smart TVs, media consoles, digital picture frames, and
   printers) to obtain user authorization to access protected resources
   by using a user agent on a separate device.
## What is Resource Owner Password Flow?
 The resource owner password credentials grant type is suitable in
   cases where the resource owner has a trust relationship with the
   client, such as the device operating system or a highly privileged

