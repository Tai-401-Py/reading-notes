

## [What is OAuth](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)

        What is OAuth?

Open Standard Authorization protocol 

        Give an example of what using OAuth would look like.

Netlify allows login via github, 

        How does OAuth work? What are the steps that it takes to authenticate the user?

Hello other site? Is this person ok to use my stuff? Oh they have credentials through you. You've verified thier identity? Ok, they are clear to use my services

        What is OpenID?

A type of authentication for logging into machines, It originally fell to the wayside because facebook connect did the same thing but was easier to understand who was controlling your login identity. It is now an authentication layer for OAuth.         

[Authorization and Authentication flows](https://auth0.com/docs/get-started/authentication-and-authorization-flow)

        What is the difference between authorization and authentication?

Authentication is who you are, Authorization is what you have access to. 

        What is Authorization Code Flow?

Authorization code is exchanged for an access token to grant access

        What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?

The calling application creates a verifier and sends over to hte serve who sends back the auth code, but it can't be exchanged for a token without the verfier. 

        What is Implicit Flow with Form Post?

A simpler way of handling logins as the application requests ands sends tokens through the front channel, without the need for secrets or extra backend calls.

        What is Client Credentials Flow?

Machine to machine authentication, they pass along thier client ID and Secret to authenticate users. 

        What is Device Authorization Flow?

rather than authenticate directy it usues a external device to authenticate who the user is, typically a smart phone. 

        What is Resource Owner Password Flow?

The application handles the user login and password. Typically using an interactive form.

## things I want to know more about

Implementation of login authorization. 