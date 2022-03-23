# reading 08

## [API DESIGN BEST PRACTICES](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)

    What does REST stand for?

REST means Representational server transfer

    REST APIs are designed around a ____.

They are designed around resources: they are any object, data, service

    What is an identifer of a resource? Give an example.
 
A URI that uniquely identifies the resource, they can be an HTTP:// address or JSON data

    What are the most common HTTP verbs?

The most common operations are GET, POST, PUT, PATCH, and DELETE.

    What should the URIs be based on?

A consistent naming convention, with a heirarchy

    Give an example of a good URI.

A good URI should not be more than 3 resources deep. ./A/B/C/ 

    What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

Chatty APIs  are both good and bad, while the data retrieval comes in smaller waves, this can cause a load on the server, however by trying to package more info in a single request you risk sending unwanted data and using more bandwidth. 

    What status code does a successful GET request return?

HTTP STATUS 200 OK! 

    What status code does an unsuccessful GET request return?

404 - NOT FOUND

    What status code does a successful POST request return?

HTTP STATUS 201 CREATED

    What status code does a successful DELETE request return?

HTTP status CODE 204 (no content)


## Things I want to know more about 

Why does my search query add `/undefined` when it's uploaded online, but work just fine in my local... 

