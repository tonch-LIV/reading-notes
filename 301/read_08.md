# 301_Read_08

- [API Design](#api-design-best-practices)
  - [Answers.1](#answers1)
- [Bookmark / Review](#bookmark-and-review)
- [Things I Want to Know](#things-i-want-to-know-more-about)

This is important because...  
REST APIs teach us how systems expose data, clients request data, How APIs organize resources, and work with data efficiently. Regex can be used to process and validate data once received.

## [API Design Best Practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)

REST API's are built around resources and can be anything a client would need to access (user, service, products, etc.). They aim to be stateless in interfacing between client and service. They also perform operations on resources through HTTP and return representations that may be hyperlinks and/or HTTP status codes; meaning they allow clients to communicate with servers using standard HTTP methods.  

Their main goal is to be;  
independant of platorms,  
scalable,  
simple,  
and more.  

"Chatty" API's require multiple small requests to retrieve data. Not a good or desirable method as this will increase impact performance negatively and resources used by increasing server load.  

APIs communicate using JSON and XML. Clients can specify the format through the HTTP Accept header.  

### HTTP Methods

Verbs that notify the server of what action to perform.

- **GET** - Retrieves / Read
- **POST** - Creates
- **PUT** - Replaces / Updates
- **PATCH** - Partial Update
- **DELETE** - Removes

Request must have all information needed to complete and fufill. The server should not depend on memory of prior requests.  

Responses can and may contain links to related resources; which in turn, should allow clients to dynamically discover available actions.  

Some operations may take time; rather than having to wait for it to be fufilled, we rely on asynchronous operations return a `202 Accepted` and let the client check a status endpoint later.  

### URI's

URI's (Uniform Resource Identifiers) are a variant of URL's, where its unique to each resource. Resource are represented as key/value pairs in JSON.  
these should be nouns rather than verbs; identifying what the resource group is, because later they will be appended to the corresponding HTTP method.  

### Methods and Status Codes

**GET**  
200 OK - Success  
204 No Content - Nothing to return
404 Not Found - No Resource  

**POST**  
201 Created - Resource Created  
200 OK - Processing Succeeded  
204 No Content - Success, No Content  
400 Bad Request - Invalid data  

**PUT**  
Sending a request multiple times produces the same result. - idempotent.  

**DELETE**  
204 No Content - Deleted Successfully  
404 Not Found - Resource does not exist  

### Answers.1

1. What does REST stand for?
    - Representational State Transfer
2. REST APIs are designed around _resources_.
3. What is an identifier of a resource? Give an example.
    - A URI uniquely identifies a resource.
    - ".../orders/1"
4. What are the most common HTTP verbs?
    - GET, POST, PUT, PATCH, DELETE
5. What should the URIs be based on?
    - Nouns (resources)
6. Give an example of a good URI.
    - /orders
7. What does it mean to have a 'chatty' web API? Is this a good or a bad thing?
    - to require many small requests to retrieve; bad, because it increase server load and reduces performance.
8. What status code does a successful `GET` request return?
    - **200 ok**
9. What status code does an unsuccessful `GET` request return?
    - **404 Not Found**
10. What status code does a successful `POST` request return?
    - **201 Created**
11. What status code does a successful `DELETE` request return?
    - **204 No Content**

## Bookmark and Review

- [RegExr](https://regexr.com/) - [cheatsheet]
  - A testing and learning environment for interactive regular expression.  
    - Allows for writing regex, highlighting matches, read explanations, see a built-in cheatsheet.  
  - Regex is notoriously difficult to learn, but RegExr makes it easier to learn through visual feedback, explaining the patterns in plain english, providing references.  
- [Regex Tutorial](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)
  - Characters match character classes. Examples and common use cases.  
- [Regex 101](https://regex101.com/)
  - Also a regex testing environment.

## Things I Want to Know More About

- status codes (expected, troubleshooting, etc.).
- RegEx.
