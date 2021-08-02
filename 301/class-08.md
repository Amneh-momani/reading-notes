# API Design Best Practices

## REST stand for

**Roy Fielding proposed Representational State Transfer**

## REST APIs are designed around a ____

**resources** which are any kind of (object, data, or service) that can be accessed by the client

## A resource has an identifier, which is a URI that uniquely identifies that resource.

Example :
      
      https ://adventure-works.com/orders/1


## The most common HTTP verbs are:

_GET, POST, PUT, PATCH, and DELETE_

## The URIs should be based on:

 nouns (the resource) and not verbs (the operations on the resource).

 Example of a good URL:

         https  ://adventure-works.com/orders 

## ‘chatty’ web API:

it exposes a large number of small resources and It's not good


## successful GET request return:

 _HTTP status code 200 (OK)_

## unsuccessful GET request return:
_404 (Not Found)_

## successful POST request return:

_HTTP status code 201 (Created)_

## successful DELETE request return:

 _HTTP status code 204 (No Content)_


