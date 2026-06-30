# 301_Read_12 - CRUD

This is important because...  
if we are to build web applications, it stands to reason that we should know how they communicate.
We will be learning how to tie the front-end and backend with tools such as REST APIs and HTTP Requsts.

## [Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

All HTTP communications include a status code; the beginning digit of said code, categorizes the response.  

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
        - hj

2. What is a status code 202?
   - Accepted.  
3. What is a status code 308?
   -Permanent Redirect.  
4. What code would you use if an update didn't return data to a client?
   - 204 No Content
5. What code would you use if a resource used to exist but no longer does?
   - 410 Gone
6. What is the 'Forbidden' status code?
   - 403 Forbidden.  

## [[Video] - Build A REST API With Node.js, Express, & MongoDB - Quick](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw) - First 20 minutes

### Answers.2

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
2. What is middleware?
3. What does `app.use(express.json())` do?
4. What does the `/:id` mean in a route?
5. What is the difference between `PUT` and `PATCH`?
6. How do you make a default value in a schema?
7. What does a `500` error status code mean?
8. What is the difference between a status `200` and a status `201`?

## Things to Learn More About
