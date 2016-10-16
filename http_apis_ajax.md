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

**URLs**, uniform resource locators, are URIs which contain instructions on how to load the resource and explicitly list http or https as the protocol and the host name. The example ```GET``` request above is equivalent to the following URL: ```http://httpbin.org/xml``` where ```http://``` is the protocol, ```httpbin.org``` is the host name and ```/xml``` is the URI.



---


#### Request methods

Common request methods include:

- `GET`: this is the most common request when accessing a website with your browser. A `GET` request method indicates that the client is requesting some resource from the server, but is not sending any resources along with the request.
  - Example: typing www.facebook.com into your browser and pressing enter. You are requesting the Facebook webpage.
- `POST`: sends a request along with a resource to be posted to the server.
  - Example: making a Facebook status update and pressing submit. The status update is sent as the `body` of the request.
- `DELETE`: sends a request to delete a resource on the server.
  - Example: deleting a Facebook status update.
- `PUT`: this method sends a request to post something to the server; if there is already something at the specified location, it is modified.
  - Example: editing a Facebook status update. The new status update is sent as the `body` of the request.

When you type a URL into the browser and press enter, your browser makes a `GET` request to a server for a specific resource.



---

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
* **cURL**, a command line library, allows you to make HTTP requests and return the raw response in your terminal
* The HTML elements ```<a>``` and ```<form>``` make HTTP requests to request the resource specified in the ```href``` url and to ```GET``` or ```POST``` data to the ```action``` attribute's url 


## APIs
### What is it?
* Stands for Application Programming Interface
* How programmers search for, access, post, and retreive information online
* Method for connecting your site to a 3rd party webservice
* Defines what the client (your web browser) can get from a web server and how you get it

### How to use it
* API requests can be made directly in the browser or terminal, but it's hard to work with the returned data
* Most API requests will be called using a **wrapper library**, a thin layer of code which translates a library's existing interface into a compatible interface. Wrapper libraries work like a translator to enable cross language interoperability
* Some APIs require API keys, which act like passwords. They let the server know who is requesting their content and track how much content they're requesting

## AJAX
### What is it?
* Stands for **asynchronous javascript and xml**
* From MDN: the use of the XMLHttpRequest object to communicate with server-side scripts
* A technique for requesting a loading data from a server into an HTML page without having to refresh the entire page
* AJAX allows direct access to API data using JavaScript instead of a server-side programming language

### How to use it
* Most commonly used with jQuery which provides greater efficiency and cross-browser support
* AJAX requests only work on a web server

