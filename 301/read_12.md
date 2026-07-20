# 301_Read_12 - CRUD

- [REST Methods Status Codes](#status-codes-based-on-rest-methods)
  - [Answers.1](#answers1)
- [Building a REST API](#video---build-a-rest-api-with-nodejs-express--mongodb---quick---first-20-minutes)
  - [Answers.2](#answers2)
- [Things to Learn More About](#things-to-learn-more-about)

This is important because...  
if we are to build web applications, it stands to reason that we should know how they communicate.
We will be learning how to tie the front-end and backend with tools such as REST APIs and HTTP Requests.

Clients request data from servers, in turn the server responds with the data (if any) and a status code that tells the client much useful information.

## [Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

All HTTP communications include a status code; the beginning digit of said code, categorizes the response.  

**100 - Informational**  
Uncommon in everyday development; indicate that the srever has received the request and will continue the process.  
Used for communications between clients and servers during transmission.  

**200 - Success**  
indicates request was received and was succesful.  
200 OK (GET, PUT/PATCH, DELETE)  
201 Created  (POST)  
202 Accepted  (POST)  
205 No Content

**300 - Redirection**  
The requested resource is real, but is not at the location queried.  
Must make new request to new location.

**400 - Client-side Errors**  
Invalid request is sent sent by client.  
Client must resolve before attempting again.  
(wrong url, missing data, bad request format, missing authen / lacking autho, etc.)  

**500 - Server-side Errors**  
Request correctly reached server, but error / failure occured while processing it.  
(server crashed, external service connection failure, etc.)  

### Answers.1

1. In your own words, describe what each group of status code represents:
   - 100's = Informational;  
      - uncommon, but still found in the wild; gives feedback that request was received and is being processed.  
   - 200's = Success;  
      - request was recived and accepted.  
        - 200 OK; 201 Created; 202 Accepted; 204 No Content.  
   - 300's = Redirection;  
      - indicate resource exist, but is not at the current location.  
   - 400's = Client Errors;  
      - Wrong URL; missing data; bad request format; missing authentication and/or permissions; resolved by client.  
   - 500's = Server errors;  
      - request succesfully reached server, but error occured while processing.

2. What is a status code 202?
   - Accepted; valid request, but still processing and will finish later (*asynch*).  
3. What is a status code 308?
   -Permanent Redirect; resource has moved and must be reuest at new location.  
4. What code would you use if an update didn't return data to a client?
   - 204 No Content; updates succeded, but response body to return to
5. What code would you use if a resource used to exist but no longer does?
   - 410 Gone; resource has been removed, permanently.  
6. What is the 'Forbidden' status code?
   - 403 Forbidden; lacking permissions to access.  

## [[Video] - Build A REST API With Node.js, Express, & MongoDB - Quick](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw) - First 20 minutes

**Environement Files**  
Sensitive information sould be held within the `.env` file. This prevents such info from being 'hard-coded' into source / production files and/or shared publicly, such as when pushed to Github.  

**MiddleWare (WAAAAH!)**  
Code that runs in-between a request being received and a response being sent; a checkpoint of sorts where;  
JSON can be parsed,  
Request can be validated, logged,  
Authentication of users can occur,  
EWrrirs can be handled,  

`espress.json()` is middleware that tells Express to automatically parse incoming JSON request bodies.  
Needed by `req.body` when clients send JSON.  

**Route Parameters**  
Seen in a routes' URI by a value after the colon,  

```js
`/subscribers/:id`
```

that `id` value become dynamic, meaning it constantly changes to correctly match the ID with the appropriate object.  

**PUT vs PATCH**  
PUT replaces the entire resource; whereas,  
PATCH updates specific field within.  

**Mongoose Schemas**  
Default values should be added to the schema fields, otherwise Mongoose automatically inserts the default value.

### Answers.2

1. Why do we need to pull our MongoDB database string out of our server and put it into our `.env`?
   - contains sensitive info; keep it secure so it is not shared during ACP process to version control (Git).
2. What is middleware?
   - `cors`; the middle-man that allows communication between the front-end and backend.
   - can modify requests, validate data, parse JSON, authrnticate users, or handle errors.  
3. What does `app.use(express.json())` do?
   - middleware that parses incoming JSON requests automatically; makes data available through `req.body`.  
4. What does the `/:id` mean in a route?
   - a dynamic route *parameter*; placeholder value for whatever content will live in that location.  
5. What is the difference between `PUT` and `PATCH`?
   - PUT - replaces an entire resource.  
   - PATCH - updates specified fields / values.
6. How do you make a default value in a schema?
   - through the use of the `default` property inside the fields definition:
      - `default: "Unknown"`  
   - if no `default` is specified, Mongoose assumes true.
7. What does a `500` error status code mean?
   - internal server error occured while processing the request; something failed on the server end.
8. What is the difference between a status `200` and a status `201`?
   - 200 OK - request was succesful.
   - 201 Created - request succeeded **and** a new resource was created.

## Things to Learn More About

- MiddleWare details,  
