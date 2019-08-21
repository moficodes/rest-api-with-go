# Rest API

Most APIs written this days are web apis. Don't quote me on that one because I didn't do any research to get a proper number. 😁But given the number of web services and web application I don't think I am too far off.



## What is REST

REST is acronym for **RE**presentational **S**tate **T**ransfer. It is architectural style for **distributed hypermedia systems** and was first presented by Roy Fielding in 2000 in his famous [dissertation](https://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm).

Like any other architectural style, REST also does have it’s own [6 guiding constraints](https://restfulapi.net/rest-architectural-constraints/) which must be satisfied if an interface needs to be referred as **RESTful**. These principles are listed below.

### Guiding Principles of REST

1. **Client–server** – By separating the user interface concerns from the data storage concerns, we improve the portability of the user interface across multiple platforms and improve scalability by simplifying the server components.
2. **Stateless** – Each request from client to server must contain all of the information necessary to understand the request, and cannot take advantage of any stored context on the server. Session state is therefore kept entirely on the client.
3. **Cacheable** – Cache constraints require that the data within a response to a request be implicitly or explicitly labeled as cacheable or non-cacheable. If a response is cacheable, then a client cache is given the right to reuse that response data for later, equivalent requests.
4. **Uniform interface** – By applying the software engineering principle of generality to the component interface, the overall system architecture is simplified and the visibility of interactions is improved. In order to obtain a uniform interface, multiple architectural constraints are needed to guide the behavior of components. REST is defined by four interface constraints: identification of resources; manipulation of resources through representations; self-descriptive messages; and, hypermedia as the engine of application state.
5. **Layered system** – The layered system style allows an architecture to be composed of hierarchical layers by constraining component behavior such that each component cannot “see” beyond the immediate layer with which they are interacting.
6. **Code on demand \(optional\)** – REST allows client functionality to be extended by downloading and executing code in the form of applets or scripts. This simplifies clients by reducing the number of features required to be pre-implemented.

To see an example of a REST API we can use 

{% embed url="https://jsonplaceholder.typicode.com/" %}

### HTTP Verbs

These are some conventions HTTP apis follow. These are actually not part of Rest specification. But we need to understand these to fully utilize Rest API.

HTTP defines a set of **request methods** to indicate the desired action to be performed for a given resource. Although they can also be nouns, these request methods are sometimes referred as _HTTP verbs_. Each of them implements a different semantic, but some common features are shared by a group of them: e.g. a request method can be [safe](https://developer.mozilla.org/en-US/docs/Glossary/safe), [idempotent](https://developer.mozilla.org/en-US/docs/Glossary/idempotent), or [cacheable](https://developer.mozilla.org/en-US/docs/Glossary/cacheable).

[`GET`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET)The `GET` method requests a representation of the specified resource. Requests using `GET`should only retrieve data.

[`HEAD`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/HEAD)The `HEAD` method asks for a response identical to that of a `GET` request, but without the response body.

[`POST`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/POST)The `POST` method is used to submit an entity to the specified resource, often causing a change in state or side effects on the server.

[`PUT`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PUT)The `PUT` method replaces all current representations of the target resource with the request payload.

[`DELETE`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/DELETE)The `DELETE` method deletes the specified resource.

[`CONNECT`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/CONNECT)The `CONNECT` method establishes a tunnel to the server identified by the target resource.

[`OPTIONS`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/OPTIONS)The `OPTIONS` method is used to describe the communication options for the target resource.

[`TRACE`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/TRACE)The `TRACE` method performs a message loop-back test along the path to the target resource.

[`PATCH`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PATCH)The `PATCH` method is used to apply partial modifications to a resource.

_THESE ARE ALL LIES._  


### Status Codes

{% tabs %}
{% tab title="1xx Information" %}
* [100 Continue](https://httpstatuses.com/100)
* [101 Switching Protocols](https://httpstatuses.com/101)
* [102 Processing](https://httpstatuses.com/102)
{% endtab %}

{% tab title="2xx Success" %}
* [200 OK](https://httpstatuses.com/200)
* [201 Created](https://httpstatuses.com/201)
* [202 Accepted](https://httpstatuses.com/202)
* [203 Non-authoritative Information](https://httpstatuses.com/203)
* [204 No Content](https://httpstatuses.com/204)
* [205 Reset Content](https://httpstatuses.com/205)
* [206 Partial Content](https://httpstatuses.com/206)
* [207 Multi-Status](https://httpstatuses.com/207)
* [208 Already Reported](https://httpstatuses.com/208)
* [226 IM Used](https://httpstatuses.com/226)
{% endtab %}

{% tab title="3xx Redirects" %}
* [300 Multiple Choices](https://httpstatuses.com/300)
* [301 Moved Permanently](https://httpstatuses.com/301)
* [302 Found](https://httpstatuses.com/302)
* [303 See Other](https://httpstatuses.com/303)
* [304 Not Modified](https://httpstatuses.com/304)
* [305 Use Proxy](https://httpstatuses.com/305)
* [307 Temporary Redirect](https://httpstatuses.com/307)
* [308 Permanent Redirect](https://httpstatuses.com/308)
{% endtab %}

{% tab title="4xx Client Error" %}
* [400 Bad Request](https://httpstatuses.com/400)
* [401 Unauthorized](https://httpstatuses.com/401)
* [402 Payment Required](https://httpstatuses.com/402)
* [403 Forbidden](https://httpstatuses.com/403)
* [404 Not Found](https://httpstatuses.com/404)
* [405 Method Not Allowed](https://httpstatuses.com/405)
* [406 Not Acceptable](https://httpstatuses.com/406)
* [407 Proxy Authentication Required](https://httpstatuses.com/407)
* [408 Request Timeout](https://httpstatuses.com/408)
* [409 Conflict](https://httpstatuses.com/409)
* [410 Gone](https://httpstatuses.com/410)
* [411 Length Required](https://httpstatuses.com/411)
* [412 Precondition Failed](https://httpstatuses.com/412)
* [413 Payload Too Large](https://httpstatuses.com/413)
* [414 Request-URI Too Long](https://httpstatuses.com/414)
* [415 Unsupported Media Type](https://httpstatuses.com/415)
* [416 Requested Range Not Satisfiable](https://httpstatuses.com/416)
* [417 Expectation Failed](https://httpstatuses.com/417)
* [418 I'm a teapot](https://httpstatuses.com/418)
* [421 Misdirected Request](https://httpstatuses.com/421)
* [422 Unprocessable Entity](https://httpstatuses.com/422)
* [423 Locked](https://httpstatuses.com/423)
* [424 Failed Dependency](https://httpstatuses.com/424)
* [426 Upgrade Required](https://httpstatuses.com/426)
* [428 Precondition Required](https://httpstatuses.com/428)
* [429 Too Many Requests](https://httpstatuses.com/429)
* [431 Request Header Fields Too Large](https://httpstatuses.com/431)
* [444 Connection Closed Without Response](https://httpstatuses.com/444)
* [451 Unavailable For Legal Reasons](https://httpstatuses.com/451)
* [499 Client Closed Request](https://httpstatuses.com/499)
{% endtab %}

{% tab title="5xx Server Error" %}
* [500 Internal Server Error](https://httpstatuses.com/500)
* [501 Not Implemented](https://httpstatuses.com/501)
* [502 Bad Gateway](https://httpstatuses.com/502)
* [503 Service Unavailable](https://httpstatuses.com/503)
* [504 Gateway Timeout](https://httpstatuses.com/504)
* [505 HTTP Version Not Supported](https://httpstatuses.com/505)
* [506 Variant Also Negotiates](https://httpstatuses.com/506)
* [507 Insufficient Storage](https://httpstatuses.com/507)
* [508 Loop Detected](https://httpstatuses.com/508)
* [510 Not Extended](https://httpstatuses.com/510)
* [511 Network Authentication Required](https://httpstatuses.com/511)
* [599 Network Connect Timeout Error](https://httpstatuses.com/599)
{% endtab %}
{% endtabs %}

This also has no actual meaning. 



### **Terminologies**

The following are the most important terms related to REST APIs

* **Resource** is an object or representation of something, which has some associated data with it and there can be set of methods to operate on it. E.g. Animals, schools and employees are resources and _delete, add, update_ are the operations to be performed on these resources.
* **Collections** are set of resources, e.g _Companies_ is the collection of _Company_ resource.
* **URL** \(Uniform **Resource** Locator\) is a path through which a **resource** can be located and some actions can be performed on it.

### API Endpoint

This is what a API endpoint looks like.

```text
https://www.github.com/golang/go/search?q=http&type=Commits
```

This URL can be broken into these parts

| **protocol** | subdomain | **domain** | **path** | Port | **query** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| _http/https_ | subdomain | _base-url_ | _resource/some-other-resource_ | some-port | _key value pair_ |
| https | www | github.com | golang/go/search | 80 | ?q=http&type=Commits |

#### Protocol

How the browser or client should communicate with the server.

#### Subdomain

Sub Division of the main domain

#### Domain

Unique reference to identify web site on the internet

#### Port

Port on the server the application is running on. By default its 80. So most cases we don't see it 

#### Path

Path parameters in a Rest API represents resources.

```text
https://jsonplaceholder.typicode.com/posts/1/comments
```

`posts/1/comments`

This path is representing the `1st` `posts` resource'c `comments` 

Basic structure is 

```text
top-level-resource/<some-identifier>/secondary-resource/<some-identifier>/...
```

#### Query

Queries are key value pairs of information, used mostly for filtering purposes.

```text
https://jsonplaceholder.typicode.com/posts?userId=1
```

Parts after the `?` is the query parameters. We have only one query here. `userId=1`

#### Headers

This was not part of the URL itself but header is a part of network component sent by the client or the server. Based on who sends it. There are two kinds of header

1. Request Header \(client -&gt; server\)
2. Response Header \(server -&gt; client\)

#### Body

You can add extra information to both the request to the server and to the response from the server.

