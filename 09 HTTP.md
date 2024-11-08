# Web and HTTP Applications

### Author: Sunimal Rathnayake, CSE, UOM

---

## 1. Structure of the Web
- **Web Clients**: Applications like browsers (e.g., Chrome, Firefox) that request and display web pages from servers.
- **Web Servers**: Software such as Apache or Nginx that provide web pages upon client requests.
- **Web Pages**: Documents written in HTML, consisting of text, images, and other resources.
- **Resources**: Information pieces accessible on the web, including documents, images, and videos.
- **URL (Uniform Resource Locator)**: The address used to access resources on the web, e.g., `https://www.example.com/index.html`.
  
### Hyperlinks
- **Function**: Web pages contain links (URLs) that connect to other pages, creating a web structure. For instance, a news article may link to related stories or external sources.

---

## 2. Client-Server Communication (HTTP)
- **Protocol**: HTTP (HyperText Transfer Protocol) serves as the web’s primary application-layer protocol.
- **Model**: Follows a client/server model.
  - **Client**: A browser that requests, receives, and displays web resources.
  - **Server**: A web server that sends resources in response to client requests.

*Example*: When you enter `https://www.wikipedia.org` in your browser, your browser (client) sends a request to Wikipedia's server, which responds with the homepage.

---

## 3. HTTP Overview
- **Connection Setup**: Uses TCP (typically on ports 80 for HTTP or 443 for HTTPS).
  - **Client**: Initiates a TCP connection to the server.
  - **Server**: Accepts the connection and exchanges HTTP messages.
- **Stateless Protocol**: HTTP does not retain information about previous requests. Each request is independent.

*Example*: Visiting `https://www.example.com/page1` and then `https://www.example.com/page2` involves separate, stateless HTTP requests.

```
GET /index.html HTTP/1.1        
Host: www.example.com       
User-Agent: Mozilla/5.0     
Accept-Language: en-US
```

### HTTP Response Message
- **Status Line**: Contains protocol, status code, and status phrase.
- **Header Lines**: Include Date, Server information, Content-Type, Content-Length, etc.
- **Body**: Contains the requested resource (e.g., HTML file data).

*Example*:

HTTP/1.1 200 OK     
Date: Mon, 27 Jul 2009 12:28:53 GMT     
Server: Apache/2.2.14 (Win32)       
Content-Type: text/html; charset=UTF-8      
Content-Length: 88          
```
<html>
<body>
<h1>Hello, World!</h1>
</body>
</html>
```

---

## 6. HTTP Methods
- **GET**: Retrieve data from a specified resource.
- **POST**: Send data to a server to create or update resources.
- **HEAD**: Retrieve header information without the body.
- **PUT**: Upload a file to the specified URL path.
- **DELETE**: Remove the resource identified by the URL.

*Example*:
- **GET**: Fetching a webpage.
- **POST**: Submitting a form on a website.
- **PUT**: Uploading a file to a server.
- **DELETE**: Deleting a resource via an API.

---

## 7. HTTP Response Status Codes
- **200 OK**: Request succeeded.
- **301 Moved Permanently**: Resource moved to a new location.
- **400 Bad Request**: Malformed request syntax.
- **404 Not Found**: Requested resource was not found.
- **505 HTTP Version Not Supported**: HTTP version not supported by the server.

*Example*:
- **200 OK**: Accessing a webpage successfully.
- **404 Not Found**: Trying to access a non-existent page.

---

## 8. HTTP Testing with Telnet
- **Telnet Connection**: Open a TCP connection to a server’s HTTP port.
- **Example Request**: Using `GET` to retrieve data from a URL and view the server's response.

*Example*:
```
telnet www.example.com 80
GET / HTTP/1.1
Host: www.example.com
```
---

## 9. Uploading Data to a Website
- **POST Method**: Data is uploaded within the request body, often from form input.
- **GET Method**: Data encoded in the URL (e.g., search parameters).

*Example*:
- Using `POST` for login forms, submitting data in the body.
- Using `GET` to perform search queries, as in `https://www.example.com/search?q=keywords`.

---

## 10. Additional Headers in HTTP
- **Cookies**: Maintain session state across requests, with components:
  - **Response Cookie**: Header line in the HTTP response.
  - **Request Cookie**: Header line in HTTP requests.
  - **Client-Side Cookie File**: Managed by the browser.
  - **Server-Side Database**: Maintains session data linked to cookie ID.
- **Conditional GET**: Ensures resources are only re-downloaded if modified.
- **Accept-Language**: Specifies language preferences; server responds in preferred language if available.

### Cookies Example
- **Session Maintenance**: The server assigns a unique ID, stored in a cookie file, for tracking user sessions over multiple visits.

---

## 11. Web Caching
- **Purpose**: Stores copies of recently accessed pages to reduce load times and bandwidth.
- **Types**:
  - **Browser Cache**: Stores resources locally for quicker retrieval.
  - **Proxy Cache**: Intermediate storage that serves cached pages to multiple users.
- **Conditional GET**: Ensures resources are downloaded only if updates exist, using the `If-Modified-Since` header.

*Example*: Accessing a site like `https://www.news.com` may use a cache to serve previously loaded images.

---

## 12. Secure HTTP (HTTPS)
- **Data Encryption**: Prevents unauthorized access to data.
- **Authentication**: Verifies the identity of web servers and sometimes clients, showing a padlock or similar security icon in the browser.

*Example*: Online banking sites like `https://www.bank.com` use HTTPS to secure transactions and personal information.

---

## 13. Web Applications
- **Static Websites**: Traditional, non-interactive pages.
- **Interactive Web (Web 2.0)**: Allows user modifications (e.g., Gmail, Facebook, Wikipedia, UoM Moodle).
- **Search Engines**: Google, Bing, and others, providing powerful, global information retrieval.

---

## 14. Conclusion
- HTTP is foundational for web applications.
- Mastering HTTP is essential for web development and application functionality.

