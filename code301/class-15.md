# Read 15 - Authentication

## What is OAuth

1. ***What is OAuth?***
OAuth is an open-standard authorization protocol that allow unrelated services and services to safely delegate authorization between one another.
2. ***Give an example of what using OAuth would look like.***
Using your Google Account to sign into a non-Google service is an example of using OAuth (or similar protocol). The non-Google service never knows and never needs to own your Google login thanks to the authorization protocol.
3. ***How does OAuth work? What are the steps that it takes to authenticate the user?***
OAuth allows an authenticated user of one service get a limited authorization token for resources on another server. I've summarized the steps as follows:

    1. Website A, on behalf of the user, provides the user's identity to Website B.
    2. Website B generates a one-time token and secret unique.
    3. Website A gives the token and unique to the user.
    4. The user presents these to their authorization provider.
    5. The user will be asked to authenticate with the authorization provider if not already.
    6. User (or their software silently) approves a transaction at Website A
    7. User receives an approved access token.
    8. The user gives it to Website A.
    9. Website A gives it to Website B as a proof of user's authentication.
    10. Website B allows access to Website A on behalf of the user.
    11. The user sees the transaction succeed.

4. ***What is OpenID?*** OpenID is an *authentication* framework that arose in 2005, and attempted to provide a similar function to OAuth: allowing a user to access resources in multiple websites with a single log-in. OpenID Connect is a reinvention of OpenID for use as an authentication layer for OAuth

## Authorization and Authentication flows

1. ***What is the difference between authorization and authentication?*** *Authorization* is the level of access a given user has for a resource or system. *Authentication* is the verification of their identity as a the correct and honest user.
2. ***What is Authorization Code Flow?*** Authorization code flow is the process of redirecting the user to the Auth0 servers for authentication when they make an API request, granting them a authorization token, and then double-checking that token in your API with Auth0 before it fulfills the request.
3. ***What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?*** This is an improvement to simple *Authorization Code Flow* for use on native and single-page apps. Is it very similar except Auth0 generates a code verifier and code challenge at the time the user starts the login process. These are cryptographically-random and harder to capture and/or forge.
4. ***What is Implicit Flow with Form Post?*** This is a login process for an app where an ID token is given to the application by Auth0 to verify the user while they access resources.
5. ***What is Client Credentials Flow?*** This is a machine-to-machine (M2M) authorization flow where your back-end service itself authenticates with Auth0, it is then given an access token with which allows it to request and receive data from another API.
6. ***What is Device Authorization Flow?*** Device authorization flow uses a method similar to two-factor authentication to authorize and authenticate a user. This allows an input constrained device to use Auth0 features by authenticating the user on a 2nd device with web-browser capability.
7. **What is Resource Owner Password Flow?** This flow has the user log in to website, have site give those credentials to Auth0 for authentication, and provision of an access token to the website if authentication is successful. This flow has a security vulnerability because the user is not authenticating directly with Auth0 and their credentials are being stored by the website.
