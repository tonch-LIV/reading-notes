# 301_Read_15 - Authentication

- [What is OAuth](#what-is-oauth)
  - [OpenID](#openid)
  - [Answers.1](#answers1)
- [Authorization and Authentication flows](#authorization-and-authentication-flows)
  - [Code Flows](#code-flows)
  - [Answers.2](#answers2)
- [Bookmark and Review](#bookmark-and-review)
- [Things to Learn More About](#things-to-learn-more-about)

This is important because...  
OAuthis a framework that allows users and applications to securely access another service (on behalf of the user's request) to establish a sense of identity without ever having to see or exchange passwords.  
This can be done many different ways, but the overall main goal is to verify ***who*** you are and ***what*** you are allowed to.

## [What is OAuth](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)

Open Authorization, an authorization framework, lets one application or service access a different service's resources (like identity and permissions), without having to outright provide credentials (assuming you are logged in to the service from which you are making the request to, otherwise you will need to provide credentials to them).  
Seen on a login portal as,  
"Log in with;  
Google,  
Apple,  
Microsoft, etc."  

The supplicant application receives a temporary access token rather than actual credentials.  

### OpenID

OpenID Connect (OIDC), builds on OAuth by answering who the user is.  
OIDC work in tangent with OAuth by saying, "**this user** is *allowed* to **do this** (substituting this with a person and the permissions allowed, repectively).  

### Answers.1

1. What is OAuth?
   - an authorization framwework for providing permissions based on a mutual understanding of a user's identity, theough the use of a token rather than passwords.
2. Give an example of what using OAuth would look like.
   - When logging into a page and seeing the options that say "Log in with..." or "Continue with..." and presented with options of other services or platforms from where one might already have an established account with.  
3. How does OAuth work? What are the steps that it takes to authenticate the user?  
   - Choose "Log in with..." and your choice of 'identity provider' (google, microsoft, apple, etc.),  
   - redirected to identity provider authentication portal where one is either logged in or logs in,  
   - permissions are granted to service from identity provider on what it wants and may access,  
   - user approves,  
   - authorization code or token provided by identity provider,  
   - supplicant applicaton (or service) uses token to access authorized resources to establish a profile for user on their service.
4. What is OpenID?  
   - an identity layer that build on OAuth to authenticate a user's identity and provide verified info (name, email, etc.).

## [Authorization and Authentication flows](https://auth0.com/docs/flows)

Different kinds of services require and use different authentication flows.  
A mobile app is different than a server,  
different than a desktop app,  
different IoT devices, etc.  

**Authentication** answers *who* you are;  
**Authorization** answers *what* you are *allowed* to do.  
*(Permissions to an Identity.)*  

### Code Flows  

The standard OAuth flow used by web apps with a back-end server is based upon,  
the browser receiving an authorization code and the server exchaging that code for a token.  
This allows the token to stay hidden from the browser = most secure OAuth flow.  

**Authorization Code Flow w/ PKCE**  
The recommended flow for Single Page Apps (SPAs).  
Proof Key for Code Exchange (**PKCE**) allows applications that cannot safely store secrets (React, mobile, desktop apps) to create a one-time verification 'challenge' to prevent the theft of authorization codes, rather than rely on a client secret.  

**Implicit Flow w/ Form Post**  
Originally designed for browser-only apps, but has more security risks since the access code is returned directly.  
Having the token exposed to the browser is the leading factor for why it is no longer recommended for new apps.  

**Client Credentials Flow**  
The user factor does not exist; instead it is server communicating with server and authentication occurs through their communications.  

**Device authorization Flow**  
For use on devices with limited input capabilities (IoT),  
a code is displayed on the supplicant device which the user uses to authenticate with on a different device.  

**Resource Owner Password Flow**  
Application straight up asking for credentials; legacy , much less secure, and only should only be used in highly trusted scenarios.  

### Answers.2

1. What is the difference between authorization and authentication?
   - Authentication if for identity,  
   - Authorization is for permissions.  
2. What is Authorization Code Flow?
   - standard flow where a code is exchanged on server for a token; keeps token secure.  
3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
   - A more secure version; designed for SPAs and mobile apps; uses a one-time code and challenge to protect against code theft.  
4. What is Implicit Flow with Form Post?
   - Older flow where token is sent directly to browser; higher security risk.  
5. What is Client Credentials Flow?
   - server-to-server communication; user scenario does not exist. Application authenticates itself with its own credentials.  
6. What is Device Authorization Flow?
   - Buiot for IoT and other low input capabilities where a second device is used to confirm authentication.  
7. What is Resource Owner Password Flow?  
   - Credentials are provided directly to application.  

## Bookmark and Review

- [Auth0 for single page apps](https://auth0.com/docs/libraries/auth0-react)

## Things to Learn More About

- Highly trusted scenarios.  
- other OAuth uses or services beside Auth0.  
