# 401_Read_06 - Authentication

- [Securing Passwords](#securing-passwords)
  - [Answers.1](#answers1)
- [Basic Auth](#basic-auth)
  - [Answers.2](#answers2)
- [OWASP Auth](#owasp-auth-cheatsheet)
  - [Answers.3](#answers3)
- [Bookmark and Review](#bookmark-and-review)
- [Things to Learn More About](#things-to-learn-more-about)

## [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)

A password-hashing algorithm should be used to transform confidential text strings like passwords when being stored, instead of plaintext. The hash is then used to check whether it matches to what a user submits when trying to log in / authenticate.

### Answers.1

1. Explain to a non-technical friend how you would safely hash and store a password.
    - Keeping the bread recipe safe from the competition; only authorized bread makers have the key / cypher to decypher the recipe and use it to make the bread everyone loves.
2. What is Bcrypt?
    - A password-hashing algorithm specifically designed to protect passwords.
    - 'Salt' (random data) is added to password before hashing.
3. Why might you use something like Bcrypt?
    - Much more secure than reglar hashing.
    - protects against rainbow-table attacks.
    - intentionally slow, dettering from brute force.

## [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)

### Answers.2

**Basic Authentication** is a simple HTTP authentication method. The client places a username and password inside the request’s `Authorization` header.
`Base64` is encoding, not encryption. Anyone who obtains the encoded value can easily decode it. **Basic Authentication** must therefore be used over `HTTP(S)` so that the request is encrypted while traveling across the network.

1. What is **Basic Authentication**?
    - simple way to prove identity to server.
    - encoded, not encrypted.
    - should be used only through HTTP(S) not HTTP.
2. What properties are necessary in the `Authorization` header of a Basic Auth request?
    - The authentication scheme
    - one space
    - base64-encoded credentials
    - `Authorization: Basic YW50b25pbzpzZWNyZXQ=`.
3. How are `username:password` in Basic Auth encoded?
    - conmbined with colon `:`
    - converted to Base64; username:password -> YW50b25pbzpzZWNyZXQ=
    - placed after `Basic` in the `Authorization` header (`Authorization: Basic YW50b25pbzpzZWNyZXQ=`)

## [OWASP auth cheatsheet](https://www.owasp.org/index.php/Authentication_Cheat_Sheet)

Security recommendations for creating accounts, logging in, handling passwords, responding to errors, automated-attack protection, more from the authentication cycle.  
Authentication should be planned from the beginning of development because it affects access to protected resources.  
Leaving it as an afterthought, at the end can leave vulnerabilities throughout the application exposed to bad actors to exploit. Applications developed with security in mind from inception have fewer vulnerabilities throughout their lifecycle.

### Answers.3

1. Define the authentication process to a non-technical recruiter.
    - You place a bread order, when its time to pick up / receive order, you must prove you are who you say you are and that you ordered said bread, through an order confirmation or some other proof.
2. How should your error messaging respond (both HTTP and HTML)?  Why?
    - through consistent and generic responses (`Invalid username or password.`).
    - should not reveal anything (whether account exist, whether username or password as incorrect, etc.) that could lead to **user enumertion**.
    - detailed info can still be recorded in secure logs available to admins; no one else.

## Bookmark and Review

- [bcrypt docs](https://www.npmjs.com/package/bcrypt)
  - provides method `bcrypt.hash()` creates a protected password hash for storage.  
  - `bcrypt.compare()` safely checks a submitted password against an existing hash.

## Things to Learn More About

- salt and complexity
- other schemes for auth header.
- encodings other than `base64`.
- stacking `base64` encoding + basic authen (`HTTP(S)`) + encrypt (bcrypt).
- how a server receives credentials, verifies a hashed password, identifies the authenticated user, and protects routes that should only be available to authorized users.
