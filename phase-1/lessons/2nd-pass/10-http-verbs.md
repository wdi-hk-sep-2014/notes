# HTTP Verbs

## Request-response

Wikipedia:

> Request-response or request-reply is one of the basic methods computers use to communicate to each other. When using request-response, the first computer sends a request for some data and the second computer responds to the request. Usually there is a series of such interchanges until the complete message is sent. Browsing a web page is an example of request-response communication.

When I click on a link in my browser, the browser sends a *request* to the server (identified by the domain name in the URL) and the server sends a *response* (typically a web page) back to my browser, which displays it. This is the request-response cycle.


## HTTP request methods (verbs)

If the web page is the thing&mdash;the noun&mdash;then the HTTP request method is the *verb* that tells us what we want to do with that noun (resource). The resource is identified by the URL (uniform *resource* locator).

There are two primary request methods that the browser provides for interacting with the server. There are more, but for now this is enough. The two methods are GET and POST.

## GET

GET is what we call a **nullipotent** action. That means "has no power." Put another way, a GET can be used to *get* something from a server, but it should never be used to *change* anything on the server. When you click on a link in a browser, it does a GET request to the associated URL and the server responds with the page at that URL.

## POST

POST is used to make changes on the server. When duplicate requests can be sent to the same URL without resulting in duplicate changes, we say that the request is **idempotent**. *Idem* means "same," so an **idempotent** request is one that leaves things the same no matter how many times we make it.

POST is **NOT** idempotent. If you POST data to a server, and then POST it again, you will almost always get two copies of the data, which is probably not what you want. We'll talk more about POST and idempotency later in the course and will explain how you can prevent this undesirable behavior.

A POST request is generally sent when you submit a form on a web page. It is very important to use the request methods properly. A GET should never be used to change anything on the server. Keep the GET **nullipotent**!

## Successful completion

The students should have a basic understanding of MVC, including the roles of the model, view, and controller and how they interact, specifically how they are used to develop a website (vs. a desktop application).

## Resources

* [Model-View-Controller](http://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller)