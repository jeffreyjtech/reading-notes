# Read 12 - CRUD

## [Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

In your own words, describe what each group of status code represents:

1. **100’s =** Informational status codes tell the client that the header of their request has been received, and some process besides a instant success is occurring.
2. **200’s =** Success codes! The clients request was accepted. In the case of an async WRRC, this can be an indicator that the server has started processing something which merely passed initial inspection.
3. **300’s =** Redirection codes which tell the client to look somewhere else for the requested resource, as it's no longer available.
4. **400’s =** Client error codes. If the client's request was invalid for one reason or another, this is what they will get back.
5. **500’s =** These are server error codes which indicate something went wrong with the server as it processed an otherwise valid request.
6. **What is a status code 202?** This is the "Accepted" status code, which is used in async processing as a "your request is being process" indicator.
7. **What is a status code 308?** This tells the client that they should use another URL for this resource.
8. **What code would you use if an update didn’t return data to a client?** I would use code `204 No Content`. This is a success code which specifically indicates that no content will be returned.
9. **What code would you use if a resource used to exist but no longer does?** I would use code `410 Gone` if it really no longer exists, or `307 Temporary Redirect` or `308 Permanent Redirect` if a redirect exists.
10. **What is the ‘Forbidden’ status code?** `403 Forbidden` indicates the client is not authorized to access the requested resource.

## [Build A REST API](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
2. What is middleware?
3. What does app.use(express.json()) do?
4. What does the /:id mean in a route?
5. What is the difference between PUT and PATCH?
6. How do you make a default value in a schema?
7. What does a 500 error status code mean?
8. What is the difference between a status 200 and a status 201?
