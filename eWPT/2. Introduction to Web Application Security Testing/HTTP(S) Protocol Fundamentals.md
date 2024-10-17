

HTTP (Hypertext Transfer Protocol) is a stateless application layer protocol used for the transmission of resources like web application data and runs on top of TCP.
It was specifically designed for communication between web browsers and web servers.
HTTP utilizes the typical client-server architecture for communication, whereby the browser is the client and the web server is the server.
Resources are uniquely identified with a URL/URI/
HTTP has 2 versions: HTTP 1.0 & HTTP 1.1
- HTTP 1.1 is the most widely used version of HTTP and has several advantages over HTTP 1.0 such as the ability to re-use the same connection and can request multiple URIs/Resources.
During HTTP communication, the client and the server exchange messages, typically classified as HTTP requests and responses.
The client sends requests to the server and gets back responses.


HTTP Request Components

Request Line

The request line is the first line of an HTTP request and contains the following 3 components:
- HTTP method (GET, POST, PUT etc) indicates the type of request being made.
- URL (Uniform Resource Locator): the address of the resource the client wants to access
- HTTP version: The version of the HTTP protocol being used

Request Headers

Headers provide additional information about the request. Common headers include:
- User-Agent: Information about the client making the request(e.g. browser type)
- Host: the hostname of the server
- Accept: The media types the client can handle in the response(e.g HTML, JSON)
- Authorization: Credentials for authentication, if required
- Cookie: Information stored on the client-side and sent back to the server with each request

Request Body(Optional)

Some HTTP methods (like POST or PUT) include a request body where data is sent to the server, typically in JSON or form data format.


HTTP Request Methods Explained

GET - the GET method is used to retrieve data from the server. It requests the resource specified in the URL and does not modify the server's state. It is a safe and idempotent method, meaning that making the same GET request multiple times should not have any side effects.

POST - the POST method is used to submit data to be processed by the server. It typically includes data in the request body and the server may perform actions based on the data. POST requests can cause changes on the server's state and they are not idem potent.

PUT - the PUT method is used to update or create a resource on the server at specified URL. It replaces the entire resource with the new representation provided in the request body. If the resource does not exist, PUT can create it.

DELETE - the DELETE method is used to remove the resource specified by the URL from the server. After a successful DELETE request the resource will no longer be available at the URL.

PATCH - the PATCH method is used to apply partial modifications to resource. It is similar to the PUT method but only updates specific parts if the resource rather than replacing the entire resource.

HEAD - the HEAD method is similar to the GET method, but only retrieves the response headers and not the response body. It is often used to check the headers for things like resource existence or modification dates.

OPTIONS - the OPTIONS method is used to retrieve information about the communication options available for the target resource. It allows clients to determine the supported methods and headers for a particular resource.


**==HTTP Response Components==**

**Response Headers**

Similar to request headers, response headers provide additional information about the response. Common headers include:
- Content-Type: The media type of the response content(e.g. text/html, application/json)
- Content-Length: The size of the response body in bytes
- Set-Cookie: Used to set cookies on the client-side for subsequent requests
- Cache-Control: Directives for caching behavior


**Response Body(Optional)**


The response body contains the actual content of the response. For example, in case of an HTML page, the response body will contain the HTML markup.



Common HTTP Status Codes

200 OK - The request was successful and the server has returned the requested data.
301 Moved Permanently - The requested resource has been permanently moved to a new URL and the client should use the new URL for future requests
302 Found - The requested resource is temporarily located at a different URL. This code is commonly used for temporary redirections, but it's often better to use 303 or 307 instead
400 Bad Request - The server cannot process the request due to client error
401 Unauthorized - Authentication is required and the client must provide valid credentials to access the requested resource.
403 Forbidden - The server understood the request, but the client does not have permission to access the requested resource.
404 Not Found - The requested resource could not be found on the server.
500 Internal Server Error - The server encountered an error while processing the request and the specific cause is not provided


HTTPS

HTTPS(Hypertext Transfer Protocol Secure) is a secure version of the HTTP protocol, which is used to transmit data between a user's web browser and a website or web application.
HTTPS provides an added layer of security by encrypting the data transmitted over the internet, making it more secure and protecting it from unauthorized access and interception.
HTTPS is the preferred way to use and configure HTTP and involves running HTTP over SSL/TLS.
SSL(Secure Sockets Layer) and TLS(Transport Layer Security) are cryptografic protocols used to provide secure communication over a computer network, most commonly the internet. They are essential for establishing a secure and encrypted connection between a user's web browser or application and a web server.


![[HTTPS]]




