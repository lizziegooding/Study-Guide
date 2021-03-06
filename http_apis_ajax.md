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
From Lyzi Diamond: https://github.com/lyzidiamond/explains/blob/master/how-the-internet-works.md#request-methods

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

The URL is broken into a few parts:

`https://hostname:port/path-or-endpoint/resource?query=parameter`

- **hostname:port**: this is the main location of the server. When you type a URL into the browser and press enter (or use any other client), the URL is translated to an IP address using **[DNS (domain name system)](https://en.wikipedia.org/wiki/Domain_Name_System)**, which is like a phone book for domain names, and the request is routed to the correct device (most typically a server). When that server is identified, the client establishes a connection with the server that is listening for request (this is called an HTTP server). The HTTP server then interprets the request, usually by routing it to the code related to the specificed **endpoint**. (Note: most of the time, the _port_ is not explicitly defined and instead is handled by the server.)
- **path-or-endpoint**: once on the server, this is where to look for the resource. In the case of web pages, this is considered to be a _path_. When engaging with an API, it is often called an **endpoint** (see below for more information on APIs).
- **resource**: the actual resource being requested. This can be a webpage (like `index.html`), an image (like `puppies.jpg`), or some other resource.
- **query=parameter**: query parameters allow you to send additional information along with the request. Sometimes this provides more information for the server to better respond to the request.

#### HTTP Responses

If you type a URL into a browser window and press enter, you are making a `GET` request for whatever resource is at the other end of that URL. Most of the time this is a HTML webpage. In this case, the server interprets the request, and returns the HTML page to be displayed in your browser.

HTML pages tend to also require a bunch of other resources besides the HTML page itself, including JavaScript and CSS files, images, fonts, content from databases, and much more. Once the HTML page is returned to the browser, the browser reads through it and makes requests for everything that is listed in the `head` and `body` of the HTML page. As an example, to load `www.mapbox.com` requires nearly 100 individual HTTP requests, including SVGs like [turf.svg](https://www.mapbox.com/home/icons/turf.svg), JavaScript files like [base.js](https://www.mapbox.com/base.js/dist/base.js), fonts like OpenSans, and even [static map images](https://api.mapbox.com/styles/v1/mapbox/satellite-streets-v9/static/140.01,-21.24,3/800x500?access_token=pk.eyJ1IjoibXNsZWUiLCJhIjoiclpiTWV5SSJ9.P_h8r37vD8jpIH1A6i1VRg) from the Mapbox Static API.

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

