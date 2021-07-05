# REpresentational State Transfer (REST)
Architectural style for providing standards between computer systems on the web.

REST-compliant systems = RESTful systems

- stateless
- separation of concerns of client - server

## Request elements
- HTTP verb
- header
    - eg. type of content ("Accept" field)
    - uses MIME Types [more info](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types)
- path to resource
    - >Conventionally, the first part of the path should be the plural form of the resource.
- optional message body
 
## HTTP verbs
| Verb | Description |
| ---- | ----------- |
| GET | retrieve a resource |
| POST | create new resource |
| PUT | update a resource |
| DELETE | remove resource |

## Response codes
http://www.restapitutorial.com/httpstatuscodes.html

| Status code | Meaning |
| ----------- | ------- |
| 200 (OK) | This is the standard response for successful HTTP requests. |
| 201 (CREATED) | This is the standard response for an HTTP request that resulted in an item being successfully created. |
| 204 (NO CONTENT) | This is the standard response for successful HTTP requests, where nothing is being returned in the response body.
| 400 (BAD REQUEST) | The request cannot be processed because of bad request syntax, excessive size, or another client error.
| 403 (FORBIDDEN) | The client does not have permission to access this resource.
| 404 (NOT FOUND) | The resource could not be found at this time. It is possible it was deleted, or does not exist yet.
| 500 (INTERNAL SERVER ERROR) | The generic answer for an unexpected failure if there is no more specific information available.
