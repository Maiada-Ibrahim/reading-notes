# CRUD
![](https://www.dorusomcutean.com/wp-content/uploads/2020/03/crud.jpg)
## In your own words, describe what each group of status code represents:
- 100’s = try to comply with a transmission demand of the client. Like using a different protocol or telling the client that its request will fail before they start sending the body.


- 200’s =These are the success codes. They tell the client    that its request was accepted

- 300’s =the client has to issue a request to the new location.


- 400’s =It's means that these are the client error codes.

- 500’s =It's means that these are the server error codes.
## What is a status code 202?
202 Accepted - Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future. The response body should include an URL to the finished resource with some information about when it will be available, or an URL to some monitoring endpoint that tells the client when the resource is available.
## What is a status code 308?
308 Permanent Redirect - This would be the right code if we know that a resource has moved to a different URL and we can tell the client about it.
## What code would you use if an update didn’t return data to a client?
204 No Content - A proper code for updates that don’t return data to the client, for example when just saving a currently edited document.
## What code would you use if a resource used to exist but no longer does?
410 Gone - This is like 404 but we know that the resource existed in the past, but it got deleted or somehow moved, and we don’t know where.
## What is the ‘Forbidden’ status code?
403 Forbidden - The client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.


