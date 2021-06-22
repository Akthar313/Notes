# http & https 

#### What is http?
* Hyper Text Transfer Protocol
* It is stateless Application layer protocol Used to communicate between client and server 
* Every request are completly INDEPENDENT. Programming, Local storage, cookies, sessions used to create enhanced user experience.
* Default port is 80
* Here data are transfered in clear text and thus http are not preffered for banking etc websites

#### What is https?
* Hyper Text Transfer Protocol secured
* Default port is 443
* The communication protocol is secured using TLS or SSL
* This is also known as **http over TLS** or **http over ssl**

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

### Http Flow
![URL STRUCTURE](https://academy.hackthebox.eu/storage/modules/35/HTTP_Flow.png)
1. User enters URL in broswer.For eg:example.com
2. Browser sends it to DNS to resolve the IP
3. DNS resolves the IP and Sends Back the IP of the Domain to the browser
4. Browser requests IP:80 to Web server
5. Web server responds and sends 200 ok

### Https Flow
![URL STRUCTURE](https://academy.hackthebox.eu/storage/modules/35/HTTPS_Flow.png)
1. Browser tries to resolve IP
2. Once IP is resolved, Browser sends the IP:80 to the web hosting server 
3. Web server notes that its http request and hence it will be redirected to port 443 [This is done via 301 Moved permenently Response code]
4. CLient sends "CLIENT HELLO" packet giving info about client
5. Server sends "SERVER HELLO" packet giving info about server and followed by **Key exchange**
6. Client verifies the key and sends on of its own and then handshake is done!
7. After succesfull ```Handshake```, a normal connection is continued with Encryption. 


### URL-UNIFORM RESOURCE LOCATOR

![URL STRUCTURE](https://academy.hackthebox.eu/storage/modules/35/url_structure.png)

RESOURCES:
- http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol
- https://academy.hackthebox.eu/module/35
