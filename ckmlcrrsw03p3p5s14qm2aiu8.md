## What is REST?

REST is a very common term that you will hear in the programming world and so in your technical interviews. This blog post will focus on what REST is and what does it mean to have a REST*ful* API? 


# What is REST?

REST is an acronym for Representative State Transfer. It is an architectural pattern or you can say a development style that is used to build interactive applications. Ok, that means REST is not a technology or a language but more a style in which you should develop your applications. And, this can be done by following the REST principles and constraints. 

Now before we deep dive into those parts of the REST architecture, it is important to understand why do we need this architecture pattern. 

## History

Before 2000, developers integrating with APIs(Application Programming Interface) used SOAP (Simple Object Access Protocol) for communicating between the sender and the receiver systems. This required too many lines of code in XML format and then adding the SOAP envelope to the end-point. 

The most frustrating thing I find with the SOAP apart from the complex coding is the complexity in troubleshooting an issue. It involves too many calls to trace back the communication made between the systems. 

Ok, so we had APIs which are interacting with SOAP which sounds more complex, unlike its name. Then came Roy Fielding in 2000 who along with his colleagues came up with a standard in a doctoral dissertation. This standard's main goal is to provide a set of constraints(rules) that will simplify the communication between one server and another. The best thing is the interaction uses the HTTP syntax. The birth of these constraints is referred to as REST and when you build an API that follows these constraints, it is known as building a true REST*ful* API. 

## 6 Constraints 

### Client-Server architecture
Simplifying the solution into a client-server architecture. Separating the solution user interface from the data storage side of logic can assist in moving the user interface to different platforms and scaling the server components. 

### Stateless
This is inspired by the HTTP context where the client makes a request to the server. The request will contain all the information required to process the request on the server-side. The server side will not store any information related to the HTTP request and each request will be treated as a new one. That is the state of the request is managed at the client-end only. 

### Cacheable
Caching is an important concept in today's user interactions. The ability to cache a resource when applicable will reduce the number of client-server interactions because the client can re-use the same response. Caching can be applied on either side of the client-server architecture and should mark the resource to be cacheable. 

### Layered System
REST allows you to build applications that follow a layered architecture. In this architecture, the servers will only have knowledge of the intermediary servers there by the client interacting will never know which server has responded to their request. Let's take a simple web form that stores information on a database server. On top of the server, we can add a load balancer, a security layer that authorizes the requests made to the database server. The ability to build an application in this layered style will help in separating the business logic from the security logic and also makes scaling the servers an easy job. 

### Uniform Interface
It is important to apply a generality where the end-point provides the ability to interact with related or additional data using the same URI. This simplifies the interaction and improves the visibility of the resources. It is said if the user knows how to interact with one of your APIs, they should be able to follow the same approach for the remaining APIs. This is achieved through 4 architecture constraints: 

- identification of resources.
- manipulation of resources through representations.
- self-descriptive messages.
- hypermedia as the engine of application state (HATEOAS)

### Code on Demand (optional)
This is an optional constraint that allows your API to send executable code to the client system on demand. For example, Java applets or javascript to run a widget. 


## Summary
The key take-aways are:

- REST is an architecture pattern and is not a technology. 
- REST does not recommend a language in which the client or server-side of the logic must be built. 
- HTTP is not the same as REST, only that a REST application uses HTTP protocol for the requests and responses between client and server. 
- An interactive application can be made REST*ful* by following the six constraints.
- Building an application using REST simplifies the logic into its own layers and improves scalability. 
- Web services that are built using the REST constraints are known as the REST*ful* APIs:
    - This includes a base URI.
    - HTTP methods to GET, PUT, POST, or DELETE to signify the request being made. 
    - media type that tells which parser to invoke for processing the message. 
    - The responses from the server will be returned as payload in HTTP, XML, JSON, or other formats. 

Now that you got the hang of the REST architecture, you should give it a go!

### Thank you for Reading - Let's Connect!
Enjoy my blog? For more such awesome blog articles - follow, subscribe and let's connect.





