# HTTP, APIs, and AJAX


## HTTP Requests
### What is it?
* Stands for Hypertext Transfer Protocol
* It's the language that is used to communicate over the internet and has rigid rules to ensure interoperability
* Functions mainly as a request-response cycle

![Client-server request-response cycle](https://zapier.cachefly.net/static/1BMOoE/images/learn/apis/ch2-request-response-cycle.gif)
* Web browsers are GUIs for HTTP


### Anatomy
#### HTTP Request
1. Starts with ```GET```, ```POST```, ```PUT```, ```PATCH```, or ```DELETE```
2. Next is the **URI**, uniform resource identifier
3. HTTP/
4. Version of HTTP

For example, ```GET /xml HTTP/1.1```

HTTP requests often include **headers** which are described in key value pairs. 
For example,
```
Headers
Host: httpbin.org
```

#### HTTP Response
1. Status, in the format:
```
HTTP/[version][status code][status message]
HTTP/1.1 200 OK
```
2. Headers, specified in request and default
3. Blank line
4. **Payload** or response data

### How to use it
* **cURL** allows you to make HTTP requests and return the raw response in your terminal


## APIs
### What is it?
* Stands for Application Programming Interface
* How programmers search for, access, post, and retreive information online
* Method for connecting your site to a 3rd party webservice
* Defines what the client (your web browser) can get from a web server and how you get it
* 

## AJAX
### What is it?
* AJAX allows direct access to API data using JavaScript instead of a server-side programming language
* API keys act as passwords and are required by some websites. They let the server know who is requesting their content and track how much content they're requesting


