[Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)


    In your own words, describe what each group of status code represents:
        100’s = infocode
        200’s = successcode
        300’s = redirect code
        400’s = client error
        500’s = server error
    What is a status code 202?

Request Accepted but will finish in the future due to async nature. 

    What is a status code 308?

Permanent Redirect: Useful when you have multiple endopoints for a resource 

    What code would you use if an update didn’t return data to a client?

204: No content

    What code would you use if a resource used to exist but no longer does?

410: The requested resource is gone and isn't coming back

    What is the ‘Forbidden’ status code?

403: Access Forbidden

## [Build A REST API With Node.js, Express, & MongoDB - Quick ](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)

    Why do we need to pull our MongoDB database string out of our server and put it into our .env?

because it contains sensitive information like your mongoDB user and password. this also allows you to use the environmental variables outside of local host.

    What is middleware?

Software that provides common services and capabilities to applications outside of what is offered by the OS

    What does app.use(express.json()) do?
    
Lets our server accept JSON as a body.
    
    What does the /:id mean in a route?
    
This is a parameter that we can access by typing in req.params. 

    What is the difference between PUT and PATCH?
    
PAtch only updates specific informtaion put updates a whole object.   
    
    How do you make a default value in a schema?
    
 `default: `  
    
    What does a 500 error status code mean?
    
Means there is an error on the server that cuased things to fail.
    
    What is the difference between a status 200 and a status 201?

200: Everything is OK, everything acted the way we expected
201: Created -> Server has fufilled the request and created a new resource.