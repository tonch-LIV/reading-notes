# 401_Read_07 - Bearer Authorization

- [Intro to JWT](#intro-to-jwt)
  - [Answers.1](#answers1)
- [Are JWTs Secure?](#are-jwts-secure)
  - [Answers.2](#answers2)
- [JWTs Explained - [Video]](#jwts-explained---video)
  - [Answers.3](#answers3)
- [Bookmark and Review](#bookmark-and-review)
- [Things to Learn More About](#things-to-learn-more-about)

## [Intro to JWT](https://jwt.io/introduction/)

An element used during the log in process, typically after logging in. The token is created by the server and its purpose is to identify the user and can include limited permssion-related info. The client ncludes and sends the token with later request as proof that it is allowed to use and access protected routes.

### Answers.1

1. What is a JSON Web Token (JWT)?
    - a compact string used to securely pass info between parties. A server can check that it came from a trusted source and was not changed through its digital signature.
2. When should we use JSON Web Tokens?
    - When trying to ID a user (authen), and for permissions (authoriz). Also to securely exchange info between systems.
3. Claims are expected in which structural component of a JWT?
    - The payload; Claims are information about the user or token. The User ID, role, issuer, expiration time.

## [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

JWts are encoded, not encrypted; meaning they are readable. The signature is what is providing security, if you were to change the content, the signature itself would change, and thus fail verification from the know secret or private key.

### Answers.2

1. If I get a JWT and I can decode the payload, how can we call that secure?
    - Reading (decode) is different than changing / modifying. The signature verifies the contwnt has not been changed.
    - Passwords (or other sensitive info), should never be placed in normal JWT payload.
2. If sending a JWT, what must sender and receiver both know?  Hint, it's appended in the signature.
    - The secret key.
3. Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.
    - a tamper evident seal on a letter or package. The recepient is implied to be familiar with the seal, if a different seals shows up, then the recipient knows the delivery been tampered.

## [JWTs Explained - [Video]](https://www.youtube.com/watch?v=926mknSW9Lo)

JWTs are small and can be sent with HTTP requests, ableto cary the info a server needs to check access, because they are self contained.

```js
Authorization: Bearer <token>
```

### Answers.3

1. Why use JWT?
    - They allow an application to verify authentication and authorization for protected resources. 
    - Useful in APIs, because the client can send tokens with request rather than the server storing different session records for each logged-in users.
2. JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.
    - ID badges; small, compact, and has (can) include useful details (who? when? what?). Servers are able to check and decide wether the pass is valid.
3. What are the three components (the structure) of a JWT signature?
    - Header - describes token type and signing algrithm.
    - Payload - contains claims (user info and token expiration).
    - Signature - proves authenticity (data (header & payload)) has not been changed.

## Bookmark and Review

- [npm jsonwebtoken docs](https://www.npmjs.com/package/jsonwebtoken)
  - `sign()` - create JWTs.
  - `verify()` - check / verify

## Things to Learn More About

- verify routes,
- Bearer Authoriz,
- use of JWT in middleware,
- error handling,
