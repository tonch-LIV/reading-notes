# 301_Read_13 - More Crud

- [CRUD Basics](#crud-basics)
  - [Why CRUD?](#why-crud)
  - [Answers.1](#answers1)
- [Building a CRUD API](#video---speed-coding-building-a-crud-apiwatch-a-twitch-streamer-code-an-express-api-in-20-minutes)
  - [Answers.2](#answers2)
- [Things to Learn More About](#things-to-learn-more-about)

This is important because...  

It builds off of what learned in the previous reading; from learning **what** to knowing **why** and seeing **how**. Together we are able tp paint the picture and see the whole lifecycle from server creation to route definition , then data and request handling.  

HTTP request sent to REST endpoint (route) by client,  
CRUD operation performed on data,  
Response returned.  

Building APIs is about creating consistent and predictable ways for clients and servers to communicate and manage data.

## [CRUD Basics](https://medium.com/geekculture/crud-operations-explained-2a44096e9c88)

The acronym CRUD stands for,  
**C**reate, **R**ead, **U**pdate, **D**elete, and each relates to an HTTP / REST method.  

| CRUD    | REST            | Description               |
|---------|-----------------|---------------------------|
| Create  |  POST           |  Adds new data            |
| Read    |  GET            |  Retrieves existing data  |
| Update  |  PUT / PATCH    |  Modifies existing data   |
| Delete  |  DELETE         |  ... Deletes              |

These are the basic operations that almost all, if not every application performs on data.  

When creating (POST) a new object, the server creates a unique ID.  
That ID comes in handy when using GET to retrieve data, or updating and/or deleting an object as well.  

PUT replaces an entire object, PATCH only modifies the specific fields.  

### Why CRUD?

CRUD provides consistency; it is a convention followed by developers, because its understanding and the meanings are defined and agreed upon.  

Ultimately leading to better teamwork, easier maintanenece to handle, predictable APIs, standardized / easier documentation, and last, but not least; easier communication between fornt and back-end.

### Answers.1

1. Which HTTP method would you use to update a record through an API?
   - either PUT or PATCH; depending on whether its the whole object or just a property / entry.
2. Which REST methods require an ID parameter?
   - PUT, PATCH, DELETE, and GET when retrieving only a specific resource.

## [[Video] - Speed Coding: Building a CRUD API](https://www.youtube.com/watch?v=EzNcBhSv1Wo)(*Watch a Twitch streamer code an Express API in 20 minutes!*)

Before handling data, a server must exist.  
Multiple endpoints, or routes are built (each one with a single resposibility) to process different methods of CRUD operations.  

Routes that deal with handling a specific object, must define so in their route by using `/:id` in the URI.  

`req.body` is used to receive information from PUT and POST, which contains the JSON sent from client.  
The server reads the body and stores or updates the object (tie to the id).  

The use of a testing suite to verify route creation is suggested (Insomnia or EchoAPI).  

### Answers.2

1. What's the relationship between REST and CRUD?
   - CRUD is ***what*** is being done to data; REST is ***how*** to perform said actions over HTTP.
      - CRUD describes the basic four operations that can be performed.
      - REST is the architecture style for designing APIs, which maps CRUD to HTTP methods.
2. If you had to describe the process of creating a RESTful API in 5 steps, what would they be?
   - set up Express server / config the app.  
   - Create routes; PUT, GET, etc.  
   - Write route logic (do what and how).  
   - Use route parameters and request bodies (`req.params` and `req.body`) to identify resources and receive client data; connect to DB.  
   - Test API and each endpoint to verify correct behavior.  

## Things to Learn More About

- server creation  
- npx  
- route logic  
