# Web Development & Internet Fundamentals — Notes

> Cleaned and structured notes based on handwritten study notes.  
> Focus: HTML, CSS, JavaScript, frontend/backend, APIs, Internet, DNS, HTTP/HTTPS, hosting, and website development.

---

## 1. Web Development Overview

Web development is the process of building websites and web applications that users access through a web browser.

A typical web application has three major parts:

- **Frontend** — what the user sees and interacts with.
- **Backend** — server-side logic, authentication, business rules, and data processing.
- **Database** — stores and retrieves application data.

### Basic Architecture

```text
User
  |
  v
Browser / Frontend
HTML + CSS + JavaScript
  |
  | HTTP/HTTPS Request
  v
Backend / Server
Python / Java / Node.js / PHP / C# / etc.
  |
  v
Database
MySQL / PostgreSQL / MongoDB / Oracle / etc.

Server
  |
  | HTTP/HTTPS Response
  v
Browser / Frontend
```

---

# 2. Frontend Development

Frontend development deals with everything that runs in or is presented through the user's browser.

### Main Technologies

1. **HTML**
   - Defines the structure and content of a webpage.
   - Example: headings, paragraphs, forms, buttons, images, links.

2. **CSS**
   - Controls presentation and styling.
   - Example: colors, spacing, layouts, animations, responsive design.

3. **JavaScript**
   - Adds behavior and interactivity.
   - Example: button actions, form validation, DOM manipulation, API calls.

### Common Frontend Tools / Technologies

- HTML5
- CSS3
- JavaScript
- Bootstrap
- jQuery
- React
- Angular
- Vue

---

# 3. HTML

**HTML = HyperText Markup Language**

HTML is a markup language used to structure content on webpages.

### HTML Topics

- HTML basics
- HTML5
- Semantic HTML
- Forms
- Tables
- Links
- Images
- Audio and video
- Input elements
- Accessibility
- Advanced HTML concepts

### Simple Example

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
</head>
<body>
    <h1>Hello World</h1>
    <p>Welcome to my website.</p>
</body>
</html>
```

---

# 4. CSS

**CSS = Cascading Style Sheets**

CSS is used to style and arrange HTML elements.

### Important CSS Topics

- CSS basics
- Selectors
- Box model
- Flexbox
- CSS Grid
- Positioning
- Responsive design
- Transitions
- Animations
- 2D/3D transformations
- Advanced CSS

### Flexbox vs Grid

**Flexbox**
- Best for one-dimensional layouts.
- Useful for arranging elements in a row or column.

**Grid**
- Best for two-dimensional layouts.
- Useful for rows and columns together.

---

# 5. Bootstrap

Bootstrap is a frontend CSS framework that provides ready-made components and responsive layout utilities.

Common Bootstrap features:

- Grid system
- Buttons
- Cards
- Forms
- Navigation bars
- Modals
- Alerts
- Responsive utilities

Bootstrap can speed up frontend development because many common UI components are already available.

---

# 6. JavaScript

JavaScript is a programming language commonly used to make webpages interactive.

### Important JavaScript Topics

- Variables
- Data types
- Operators
- Conditions
- Loops
- Functions
- Arrays
- Objects
- ES6+
- DOM
- Events
- Asynchronous JavaScript
- Fetch API
- Promises
- `async/await`
- Browser APIs
- Libraries and frameworks

### DOM

**DOM = Document Object Model**

The browser represents an HTML document as a tree of objects.

JavaScript can use the DOM to:

- Find HTML elements
- Change text
- Change styles
- Add/remove elements
- Respond to user actions

Example:

```javascript
const heading = document.querySelector("h1");
heading.textContent = "Hello JavaScript!";
```

---

# 7. jQuery

jQuery is a JavaScript library that simplifies tasks such as:

- DOM manipulation
- Event handling
- Animations
- AJAX requests

Modern applications often use native JavaScript APIs or frameworks such as React, Angular, or Vue instead, but understanding jQuery can still be useful when working with older projects.

---

# 8. Backend Development

The backend runs on the server and handles application logic that should not be trusted to or exposed directly in the browser.

### Common Backend Technologies

- Python
- Java
- JavaScript / Node.js
- PHP
- C#
- Ruby
- Go

### Backend Responsibilities

- Authentication and authorization
- Business logic
- Data processing
- Database operations
- API development
- File handling
- Security
- Server-side validation

### Databases

Common databases include:

- MySQL
- PostgreSQL
- MongoDB
- Oracle
- Microsoft SQL Server

---

# 9. Frontend vs Backend

| Frontend | Backend |
|---|---|
| Runs mainly in the browser | Runs on the server |
| User interface | Application logic |
| HTML, CSS, JavaScript | Python, Java, Node.js, PHP, C#, etc. |
| Handles user interaction | Handles processing and data |
| Can be inspected in browser tools | Server-side source code is not directly exposed |
| Calls APIs | Provides APIs |

### Important Point

Frontend source code and resources delivered to the browser can generally be inspected using browser Developer Tools.

Backend source code normally remains on the server. The browser receives only the server's response, such as HTML, JSON, images, or other resources.

---

# 10. API

**API = Application Programming Interface**

An API is an interface that allows different software systems to communicate according to defined rules.

For example:

```text
Frontend
   |
   | API Request
   v
Backend
   |
   | Database Query
   v
Database

Database
   |
   v
Backend
   |
   | API Response
   v
Frontend
```

### Example

A frontend might request:

```http
GET /api/users/101
```

The backend may return:

```json
{
  "id": 101,
  "name": "Sai",
  "role": "Student"
}
```

---

# 11. Request and Response

Most web communication follows a **request-response model**.

### Request

The client sends a request to a server.

A request may contain:

- URL
- HTTP method
- Headers
- Query parameters
- Request body

### Response

The server sends a response back.

A response may contain:

- Status code
- Headers
- Body/data

Example:

```text
Client
  |
  | GET /products
  v
Server
  |
  | 200 OK + product data
  v
Client
```

---

# 12. Internet Fundamentals

### What is a Network?

A **network** is a collection of connected devices that can communicate and share resources.

### What is the Internet?

The **Internet is a global network of interconnected networks**.

It connects computers, servers, phones, routers, data centers, and other devices around the world.

---

# 13. Types of Networks

### LAN — Local Area Network

A network covering a small geographic area.

Examples:

- Home network
- School network
- Office network

### MAN — Metropolitan Area Network

A network covering a city or metropolitan area.

### WAN — Wide Area Network

A network covering a large geographic area.

The Internet is a large-scale example of interconnected networks.

---

# 14. How Does a Website Load?

Suppose the user enters:

```text
https://www.google.com
```

A simplified flow is:

```text
User
  |
  v
Browser
  |
  v
DNS Lookup
  |
  | Domain -> IP address
  v
Server / CDN
  |
  | HTTP/HTTPS Request
  v
Web Server
  |
  | Response
  v
Browser
  |
  v
Webpage displayed
```

### Step-by-step

1. User enters a URL.
2. The browser determines the destination domain.
3. DNS resolution finds an appropriate IP address.
4. The browser establishes the required network connection.
5. The browser sends an HTTP/HTTPS request.
6. The server processes the request.
7. The server sends a response.
8. The browser receives resources such as HTML, CSS, JavaScript, images, and data.
9. The browser renders the webpage.

---

# 15. URL

**URL = Uniform Resource Locator**

A URL identifies where a resource can be accessed.

Example:

```text
https://www.example.com/products?id=101
```

Parts:

```text
https://        -> Scheme / protocol
www             -> Subdomain
example.com     -> Domain
/products       -> Path
?id=101         -> Query parameter
```

---

# 16. Domain Name and IP Address

Computers communicate using IP addresses, while humans commonly use domain names.

Example:

```text
example.com
     |
     | DNS
     v
IP address
```

A domain name is easier for humans to remember than an IP address.

> Note: DNS does not always simply return the final physical server IP. Modern websites may use CDNs, load balancers, proxies, and other infrastructure.

---

# 17. DNS

**DNS = Domain Name System**

DNS translates domain names into IP addresses or other DNS records.

Example:

```text
www.example.com
       |
       v
      DNS
       |
       v
IP address / DNS record
```

Without DNS, users would generally need to remember IP addresses instead of domain names.

### DNS Resolver

When a device needs to resolve a domain, it usually asks a DNS resolver, which may query other DNS servers to obtain the required record.

---

# 18. Client-Server Model

A large portion of Internet communication follows the **client-server model**.

### Client

The client requests a service or resource.

Examples:

- Web browser
- Mobile app
- Desktop application

### Server

The server receives requests and provides services or resources.

Examples:

- Web server
- Application server
- Database server

```text
Client
  |
  | Request
  v
Server
  |
  | Response
  v
Client
```

---

# 19. HTTP

**HTTP = HyperText Transfer Protocol**

HTTP is a protocol used for communication between clients and web servers.

A protocol is a defined set of rules for communication.

Common HTTP methods:

- `GET` — retrieve data
- `POST` — submit/create data
- `PUT` — replace/update data
- `PATCH` — partially update data
- `DELETE` — delete data

### Common HTTP Status Codes

```text
200 OK
201 Created
400 Bad Request
401 Unauthorized
403 Forbidden
404 Not Found
500 Internal Server Error
```

---

# 20. HTTPS

**HTTPS = HTTP Secure**

HTTPS is HTTP communication protected using **TLS (Transport Layer Security)**.

It provides:

- Encryption
- Data integrity
- Server authentication through certificates

```text
HTTP
  |
  v
HTTPS = HTTP + TLS security
```

### Important Correction

It is not correct to say that an `http://` website simply "will not open because it is not secure."

HTTP can still work, but it does not provide the same encryption and security protections as HTTPS. Modern browsers may warn users when entering sensitive information over an insecure HTTP connection.

> SSL is an older protocol name. Modern HTTPS uses TLS.

---

# 21. Hypertext

**Hypertext** refers to text or other content that contains links to other resources.

For example:

```html
<a href="https://example.com">Visit Example</a>
```

Clicking the link can take the user to another resource.

Hypertext is not the process of "transferring one page to another page."

---

# 22. Hosting

**Web hosting** means providing the infrastructure needed to make a website or web application accessible over a network, typically the Internet.

A simplified process:

```text
Develop website
      |
      v
Deploy files/application
      |
      v
Hosting infrastructure
      |
      v
Domain + DNS
      |
      v
Users access website
```

### Hosting vs Deployment

- **Hosting** — infrastructure where the website/application is available.
- **Deployment** — the process of putting a new version of the application onto that infrastructure.

---

# 23. Google vs Google.com vs Google Chrome

### Google

Google can refer to the company or its search engine/service.

### Google.com

`google.com` is a website/domain, most famously used to access Google's search service.

### Google Chrome

Google Chrome is a **web browser**.

Examples of browsers:

- Google Chrome
- Mozilla Firefox
- Microsoft Edge
- Safari
- Opera

### Search Engine vs Browser

**Search engine**
- Helps users discover information on the web.
- Examples: Google Search, Bing, DuckDuckGo.

**Browser**
- Software used to access and display web resources.
- Examples: Chrome, Firefox, Edge, Safari.

---

# 24. Website Development Process

A typical website development lifecycle can include:

### 1. Requirements

Understand:

- Business goals
- Target users
- Features
- Functional requirements
- Non-functional requirements

### 2. Design

Create:

- Wireframes
- User flows
- UI designs
- UX designs
- Prototypes

A common design tool is **Figma**.

### 3. Frontend Development

Implement the user interface using technologies such as:

- HTML
- CSS
- JavaScript
- React
- Angular
- Vue

### 4. Backend Development

Implement:

- Business logic
- APIs
- Authentication
- Authorization
- Server-side validation
- Database operations

### 5. Database

Choose and configure an appropriate database.

Examples:

- MySQL
- PostgreSQL
- MongoDB
- Oracle
- SQL Server

### 6. Testing

Test the application for:

- Functional bugs
- UI issues
- API issues
- Performance
- Security
- Cross-browser compatibility

Tools may include:

- Selenium
- Postman
- Unit testing frameworks
- Integration testing tools

### 7. Deployment / Hosting

Deploy the application to a server or cloud platform.

### 8. Maintenance

After release:

- Fix bugs
- Improve performance
- Add features
- Update dependencies
- Monitor the application
- Improve security

Modern teams may use:

- Docker
- Kubernetes
- Jenkins
- CI/CD pipelines
- Cloud platforms
- Microservices

---

# 25. UI vs UX

### UI — User Interface

UI focuses on how the interface looks and how its visual components are arranged.

Examples:

- Buttons
- Colors
- Typography
- Icons
- Layout
- Forms

### UX — User Experience

UX focuses on how easy, useful, and satisfying the product is to use.

Questions include:

- Is the navigation clear?
- Can users complete tasks easily?
- Is the flow logical?
- How does the user feel while using the product?

### Simple Difference

```text
UI = How it looks
UX = How it feels and works
```

---

# 26. Why Do Businesses Use Websites?

Businesses may use websites to:

- Communicate with customers
- Promote their brand
- Sell products or services
- Generate leads
- Collect customer information
- Provide support
- Publish information
- Build credibility
- Increase sales

---

# 27. Important Concepts to Remember

```text
HTML  -> Structure
CSS   -> Style
JS    -> Behavior
API   -> Communication interface
DNS   -> Domain name resolution
HTTP  -> Web communication protocol
HTTPS -> HTTP protected by TLS
IP    -> Network address
URL   -> Address used to locate a resource
Browser -> Software used to access web resources
Server -> Provides services/resources
Hosting -> Infrastructure for making an application available
Database -> Stores application data
```

---

# 28. Complete Web Request Flow

A simplified real-world flow:

```text
                 INTERNET
                    |
                    v
User
 |
 v
Browser
 |
 | 1. Enter URL
 v
DNS Resolver
 |
 | 2. Resolve domain
 v
IP / DNS Record
 |
 | 3. Connect securely
 v
Web Server / CDN
 |
 | 4. HTTP/HTTPS Request
 v
Backend Application
 |
 | 5. Business Logic
 v
Database
 |
 | 6. Data
 v
Backend
 |
 | 7. HTTP/HTTPS Response
 v
Browser
 |
 | 8. Render
 v
User sees webpage
```

---

# Quick Revision

- **HTML** → structure of a webpage
- **CSS** → styling and layout
- **JavaScript** → interactivity and browser logic
- **Frontend** → user-facing part of a web application
- **Backend** → server-side logic
- **Database** → persistent data storage
- **API** → interface for software-to-software communication
- **Internet** → global network of interconnected networks
- **DNS** → translates/resolves domain names into DNS records such as IP addresses
- **IP address** → identifies a network interface/device or service endpoint
- **URL** → identifies a resource location
- **HTTP** → web communication protocol
- **HTTPS** → HTTP secured with TLS
- **Browser** → software that accesses web resources
- **Hosting** → infrastructure that makes a website/application available
- **UI** → interface and visual interaction
- **UX** → overall user experience
- **Deployment** → releasing an application to its target environment
- **CI/CD** → automated processes for building, testing, and delivering software

---

## Suggested Learning Order

```text
HTML
  ↓
CSS
  ↓
Bootstrap
  ↓
JavaScript
  ↓
DOM + Events
  ↓
Fetch API + Async JavaScript
  ↓
Frontend Framework
  ↓
Backend Language / Framework
  ↓
REST APIs
  ↓
Database
  ↓
Authentication
  ↓
Testing
  ↓
Git + GitHub
  ↓
Deployment
  ↓
Docker + CI/CD
```

