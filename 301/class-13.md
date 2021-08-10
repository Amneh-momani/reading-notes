## Status Codes Based On REST Methods

+ 100’s  =  **informational status codes** / tell the client the header of the request received 
+ 200’s  =  **the success codes** /  tell the client the request accepted .
+ 300’s  =  **redirection codes**  /  tell the client that the resource they are requesting isn’t available at the expected location anymore
+ 400’s  =  **the client error codes** /  the all  invalid requests a client sent to a server
+ 500’s  =  **the server error codes** /   indicate problems with overwhelmed servers or unreachable servers behind proxies

## status code 202

_**Accepted** - Often used for **asynchronous** processing. This code tells the client that the request was valid, but its processing will finish sometime in the future. The response body should include an URL to the finished resource with some information about when it will be available, or an URL to some monitoring endpoint that tells the client when the resource is available._

## status code 308

_**Permanent Redirect** - This tells the client to use another URL to access the resource and not use the current URL anymore. It’s helpful when we have multiple endpoints for one resource, but don’t want to implement reading from all of them._

4- What code would you use if an update didn’t return data to a client?

**204 No Content**

5- What code would you use if a resource used to exist but no longer does?

**The read action gets implemented via HTTPs GET method and used to fetch resource representations. Asynchronous responses aren’t much of a thing here, because the reason for asynchronous processing is often that the resource doesn’t exist yet and has to be created, so it’s a create action anyway.**

## Forbidden

 The client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.

 ## middleware

 **Middleware** is software that provides common services and capabilities to applications outside of what's offered by the operating system.

 ## app.use(express.json())

 **express. json() is a method inbuilt in express to recognize the incoming Request Object as a JSON Object. This method is called as a middleware in your application using the code: app.**

 ## the /:id mean in a route?

 On our code, that is for express framework middleware, if we want to get any id in the server code using that route, we will get that by id

 ##  the difference between PUT and PATCH

 The main difference between the PUT and PATCH method is that the PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource.

## the difference between a status 200 and a status 201

The 200 status code is by far the most common returned. It means, simply, that the request was received and understood and is being processed. A 201 status code indicates that a request was successful and as a result, a resource has been created (for example a new page).


      Note : By default, mongoose only applies defaults when you create a new document. It will not set defaults if you use update() and findOneAndUpdate(). However, mongoose 4.x lets you opt-in to this behavior using the setDefaultsOnInsert option.




