# Read 08 - APIs

## [API Design Best Practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)

1. What does REST stand for?
    - Representational State Transfer

    ***

2. REST APIs are designed around a ____.
    - resource or resources

    ***

3. What is an identifier of a resource? Give an example.
    - A URI that uniquely identifies as resource. `www.my-weather-api.com/forecast/Seattle`

    ***

4. What are the most common HTTP verbs?
    - `GET`, `POST`, `PUT`, `PATCH`, and `DELETE`

    ***

5. What should the URIs be based on?
    - URIs should be based on resources (as opposed to being based around processes)

    ***

6. Give an example of a good URI.
    - `www.my-weather-api.com/forecast/3day/Seattle`

    ***

7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
    - A chatty web API is an API which exposes a large number of small resources, which increases the amount of requests it needs to process. This can be seen as a bad thing, however having an over-consolidated API can result in too much data being fetched when a request is being served. There is balance to be had between chattiness and extraneous fetching depending on how one chooses to implement their API.
    ***

8. What status code does a successful GET request return?
    - HTTP status code 200

    ***

9. What status code does an unsuccessful GET request return?
    - HTTP status code 404

    ***

10. What status code does a successful POST request return?
    - HTTP status codes 201, 200, or 204. The latter two are used when the POST method does not create a resource (200) and if it does not produce a return (204).

    ***

11. What status code does a successful DELETE request return?
    - HTTP status code 204

    ***

## [RegExr](https://regexr.com/)

1. How would you match a phone number from your city using RegEx?

- I would create a regular expression such as `^(206)` and use the .match method.

## Things I want to know more about

- I want to know more about the creation and intent behind RegEx.
- I would like to know more about the `POST` request and what it's use cases are in comparison to similar verbs like `PUT`.
