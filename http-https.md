# http & https 

#### What is http?
>Hyper Text Transfer Protocol
>It is stateless Application layer protocol Used to communicate between client and server 
>Every request are completly INDEPENDENT. Programming, Local storage, cookies, sessions used to create enhanced user experience.
>Default port is 80
>Here data are transfered in clear text and thus http are not preffered for banking etc websites

#### What is https?
>Hyper Text Transfer Protocol secured
>Default port id 443
>The communication protocol is secured using TLS or SSL
>This is also known as **http over TLS** or **http over ssl**

#### Some Http methods
```
GET: It retrives data from the server
POST: Submits data to the server
PUT: Creates/Updates data on the  server
DELETE: Deletes data from server
OPTION: Returns all the supported methods on that particular site
TRACE:Echo's the recived request
CONNECT:Converts request connection to TCP/IP
HEAD:Retrives data without response body
```

***Here GET, OPTIONS, TRACE, HEAD methods are safe.
POST, PUT, DELETE are said to be unsafe.***

#### Http status code
```
- 1xx - Informational
- 2xx - Success
- 3xx - Redirection
- 4xx - Client side error
- 5xx - Server side error
```

Some status code to remember
```
-200 - ok
-201 - ok Created
-301 - Moved to new URL
-304 - Not modified
-400 - Bad request
-401 - UnAuthorized
-404 - Not found
-500 - Internal server error
```

#### Http Headers
1. General Headers --> Date, connection etc
2. Entity Headers --> Content-type, media-type. content-length, content-encoding etc
3. Request Headers --> Host, User-Agent, Accept, Cookie, Referrer, Authorization etc
4. Response Headers --> Server, set-cookie, www-Authentication etc
5. Security Headers --> content-security-policy, strict-transport-security, referrer-policy

### URL-UNIFORM RESOURCE LOCATOR

![URL STRUCTURE](https://academy.hackthebox.eu/storage/modules/35/url_structure.png)

RESOURCES:
- http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol
- https://academy.hackthebox.eu/module/35
