# 401_Read_09 - Authentication/Authorization

- [Lab Requirements](#read-todays-lab-requirements)
- [Bookmark and Review](#bookmark-and-review)
  - [API Server Build](#api-server-build)
  - [Auth Server Build](#auth-server-build)
- [Things to Learn More About](#things-to-learn-more-about)

## [Read today's Lab Requirements](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-09/lab/)

1. Discuss 2 possible project ideas that could be completed by you and a partner in the alloted time.
    - Ice cream business
    - Movie logger/tracker list

## Bookmark and Review

### [API Server Build](https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/api-server/)

- Review on the basic structure of an Express API, before authentication (how a client sends requests to a server and how server organizes routes, models, middleware, error handling, and CRUD operations).
  - **Routes** define the purpose of and what happens at endpoints; `GET /items`, `POST /items`.
  - **Models** define how data is stored and retrieved, ususally through database tools (Sequelize).
  - **Controllers / Route handlers** receive the request, call the model, and send the response.
  - **Middleware** runs between incoming request and route handler; i.e. logging, JSON parsing, error handling, or checking tokens.
  - **CRUD routes** create, read, update, and delete resources.

The flow might look like,

```text
Client request
   ↓
Express route
   ↓
Middleware
   ↓
Model / database
   ↓
Response sent back
```

Authen and authoriz are usally added as middleware *before* otherwise normal API routes. If the token is valid, Express continues. If not, then error response.

## [Auth Server Build](https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/auth-server/)

Review that builds on the API server structure by creating users, hashing passwords, verifying credentials, token creations, the protection of routes with authen and authoriz middleware.  
The flow here would look like,

```text
User signs up
   ↓
Server hashes password and stores user
   ↓
User signs in with credentials
   ↓
Server verifies password
   ↓
Server sends back a token
   ↓
User sends token with later requests
```

Major concepts are;

- **User Model**: Stores info (username, password, role, etc.).
- **Hashing**: Passwords are not stored as readable text, it is hashed during signup; hash then compared during signin.
- **Basic Authen**: If valid credentials sent during sign in, server can create JWT.
- **Bearer Authen**: JWT is then used and sent in `Authorization` header by client in subsequent requests.
- **ACL / RBAC middleware**: one more middleware check after token proves user authen, to determine permissions for requested action.

```js
router.delete('/users/:id', bearerAuth, acl('admin'), deleteUser);
```

`deleteUser` will only run if both, the token is valid and if authen user has `admin` role.

## Things to Learn More About

- Better understand the flow from user request to response.
- Incorporating protected routes and access to them.
  - Spearating authen and authoriz.
- Building and using middleware, tokens, RBAC effectively.
