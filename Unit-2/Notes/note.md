
---

Unit I: Introduction to Web Technology
1.1 Web Basics – Internet, Intranet, WWW

Internet: The Internet is a vast, global network of interconnected computer networks that uses the standard Internet Protocol Suite (TCP/IP) to link billions of devices worldwide. It's a public and accessible network for everyone. Think of it as a massive highway system connecting all cities and towns.

Intranet: An intranet is a private network accessible only to an organization's staff. It uses Internet technologies (like web browsers and servers) but is restricted to a specific group of users. It's like a private road system within a specific company campus.

WWW (World Wide Web): The WWW, or simply "the Web," is a system of interlinked hypertext documents and other web resources that are accessed via the Internet. It's one of the many services that run on the Internet. While often used interchangeably, the Internet is the infrastructure, and the Web is the content that travels over it.

1.2 Static vs. Dynamic Web Pages

Static Web Pages:

Definition: Web pages whose content is fixed and displayed to the user exactly as it is stored on the web server. They are built using only HTML, CSS, and client-side JavaScript.

Characteristics:
Content doesn't change unless a developer manually updates the HTML file.
Faster loading times as the server simply sends the pre-built file.
No database interaction.
Suitable for websites with infrequent content updates (e.g., portfolios, brochures).

Example: A simple "About Us" page with fixed text and images.

Dynamic Web Pages:
Definition: Web pages whose content is generated on-the-fly, typically based on user interactions, database information, or other external data. They often involve server-side scripting languages and databases.

Characteristics:
Content can change frequently and automatically.
Interacts with databases to fetch and display up-to-date information.
Provides personalized content to users.
Slower loading times compared to static pages due to server processing.
Suitable for e-commerce sites, social media platforms, blogs, etc.

Example: An online shopping cart displaying real-time stock availability, user-specific recommendations, or a news website showing the latest articles.

Here's a visual comparison:
![alt text](image.png)

1.3 Web Clients and Servers

Web Client:
Definition: A web client is a software application that requests and consumes resources (like web pages, images, videos) from a web server.
Examples: Web browsers (Chrome, Firefox, Safari, Edge), mobile apps that access web services, or even command-line tools like curl.
Function: Sends HTTP requests to web servers, receives HTTP responses, and renders the content for the user.

Web Server:
Definition: A web server is a computer program that stores web content (HTML files, CSS, JavaScript, images, etc.) and delivers it to web clients upon request.
Examples: Apache HTTP Server, Nginx, Microsoft IIS, Node.js servers (e.g., Express).
Function: Listens for incoming HTTP requests, locates the requested resource, and sends an HTTP response containing the resource back to the client.

Here's an illustration of the client-server interaction:
![alt text](image-1.png)

1.4 Client-Server Architecture (Single, Two, Multi-Tier)
The client-server architecture describes how different components of an application are distributed across various machines and communicate with each other.

Single-Tier Architecture:
Definition: All components of the application (presentation, logic, data) reside on a single machine or server.
Characteristics: Simple for small applications, but lacks scalability and can be difficult to manage as the application grows.
Example: A standalone desktop application that stores its data locally. (Less common in modern web development directly, but conceptually useful for understanding.)

Two-Tier Architecture:
Definition: Divides the application into two main tiers: the client tier and the server tier.
Client Tier: Handles the user interface and some application logic.
Server Tier: Handles data storage, retrieval, and some application logic.
Characteristics: Better separation of concerns than single-tier. The client directly communicates with the database server.
Drawbacks: The server can become a bottleneck if many clients try to access it simultaneously. Scalability issues.
Example: A simple web application where the browser (client) directly fetches data from a database server.

Multi-Tier Architecture (N-Tier Architecture):
Definition: Divides the application into more than two logical tiers, typically three (three-tier) or more. This is the most common and robust architecture for modern web applications.

Common Tiers:
Presentation Tier (Client Tier): The user interface, typically a web browser displaying HTML, CSS, and JavaScript. It sends requests to the application server.

Application Tier (Logic Tier/Middle Tier): Contains the business logic, processes requests from the presentation tier, interacts with the data tier, and prepares data for the client. This tier often runs on a web server or application server.

Data Tier: Stores and manages the application's data, typically a database server (e.g., MySQL, PostgreSQL, MongoDB). It responds to data requests from the application tier.

Characteristics:
Scalability: Each tier can be scaled independently.
Modularity: Changes in one tier are less likely to affect others.
Security: Better security as direct access to the database from the client is often prevented.
Maintainability: Easier to develop, maintain, and update different parts of the system.
Example: Most modern e-commerce sites, social media platforms, and enterprise applications use a multi-tier architecture.

Here's a diagram illustrating the different tiers:
![alt text](image-2.png)

1.5 HTTP Request and Response
HTTP (Hypertext Transfer Protocol) is the foundation of data communication for the World Wide Web. It's a request-response protocol between a client and a server.

HTTP Request:
When you type a URL into your browser or click a link, your browser (the client) sends an HTTP request to the web server.

A typical HTTP request consists of:
Request Line:

Method: The action to be performed (e.g., GET, POST, PUT, DELETE).
GET: Retrieves data from the server (most common for fetching web pages).
POST: Submits data to be processed to a specified resource (e.g., submitting a form).
PUT: Updates a resource.
DELETE: Deletes a resource.

URI (Uniform Resource Identifier): The path to the resource on the server (e.g., /index.html, /products/123).
HTTP Version: The version of the protocol being used (e.g., HTTP/1.1, HTTP/2).
Request Headers: Provide additional information about the request or the client (e.g., Host, User-Agent, Accept, Cookie).
Empty Line: Separates the headers from the message body.
Message Body (Optional): Contains data being sent to the server, primarily with POST and PUT requests (e.g., form data, JSON data).

HTTP Response:
After receiving and processing the request, the web server sends an HTTP response back to the client.
A typical HTTP response consists of:

Status Line:
HTTP Version: The version of the protocol used by the server.
Status Code: A three-digit number indicating the outcome of the request (e.g., 200 OK, 404 Not Found, 500 Internal Server Error).
Reason Phrase: A short, human-readable text explaining the status code.
Response Headers: Provide additional information about the response or the server (e.g., Content-Type, Content-Length, Server, Set-Cookie).
Empty Line: Separates the headers from the message body.
Message Body (Optional): Contains the requested resource (e.g., HTML content, an image, JSON data).
Here's a diagram illustrating the HTTP request-response cycle:
![alt text](image-3.png)

1.6 URL

URL (Uniform Resource Locator):
Definition: A URL is a specific type of URI that not only identifies a resource but also provides the means of locating the resource and retrieving it. It's essentially the address of a web resource.

Purpose: To specify how and where to access a resource on the Internet.

Components of a URL:
A typical URL has the following structure:
scheme://host:port/path?query#fragment

Scheme (Protocol): http:// or https:// (most common for web). Defines the protocol used to access the resource. Other examples include ftp://, mailto:, file:.

Host: [www.example.com](http://www.example.com). The domain name or IP address of the server hosting the resource.
Port (Optional): :80 or :443. The port number on the server where the web server is listening. HTTP defaults to port 80, HTTPS to port 443, so they are often omitted.

Path: /path/to/resource.html. Specifies the exact location of the resource on the server.
Query String (Optional): ?name=value&another=value. Used to send additional data to the server, often for dynamic content or search parameters. Starts with a ?, and parameters are separated by &.

Fragment (Optional): #section-id. Points to a specific section within an HTML document. The browser processes this part; it's not sent to the server.

Example:
[https://www.example.com:8080/products/electronics?category=laptops&brand=dell#specs](https://www.example.com:8080/products/electronics?category=laptops&brand=dell#specs)

Scheme: https
Host: [www.example.com](http://www.example.com)
Port: 8080
Path: /products/electronics
Query String: ?category=laptops&brand=dell
Fragment: #specs

1.7 Client-Side and Server-Side Scripting

Client-Side Scripting:
Definition: Code that runs directly within the user's web browser. It's executed on the client machine.
Purpose: Enhances user experience, adds interactivity, validates forms, manipulates the DOM (Document Object Model), and makes asynchronous requests to the server.
Languages: Primarily JavaScript. HTML and CSS are also client-side technologies, but JavaScript provides the dynamic scripting.

Characteristics:
Browser-dependent (may behave differently across browsers).
Visible to the user (source code can be viewed).
Faster execution for user interface elements as it doesn't require a round trip to the server.
Limited access to server resources or databases.
Example: A drop-down menu that appears when you hover over an item, form validation that checks if an email address is valid before submission, an image carousel.

Server-Side Scripting:
Definition: Code that runs on the web server before the web page is sent to the client's browser.
Purpose: Generates dynamic HTML, interacts with databases, handles user authentication, processes form submissions, manages sessions, and performs complex business logic.
Languages: PHP, Python (Django, Flask), Ruby (Ruby on Rails), Node.js (JavaScript), Java (Spring), C# (.NET).

Characteristics:
Independent of the client's browser.
Code is not visible to the user.
Can access server resources, databases, and file systems.
Requires a server to execute.
Slower for immediate UI interactions due to the network round trip.
Example: Fetching user-specific data from a database to display on a personalized dashboard, processing an online payment, logging in a user, generating a PDF report.

Here's a comparison:
![alt text](image-4.png)

1.8 Web Evolution (Web 1.0 → Web 3.0)
The web has undergone significant transformations since its inception, evolving through distinct phases.
Web 1.0 (The Static Web / Read-Only Web - ~1990s - early 2000s):

Characteristics:
Static Pages: Primarily consisted of static HTML pages. Content was largely read-only.
Information Portals: Websites were like digital brochures or online directories.
Limited Interactivity: Very little user interaction beyond clicking links.
Webmasters: Content was created and managed by a few webmasters.
One-Way Flow: Information flowed primarily from content creators to consumers.
Examples: Personal homepages (GeoCities, Angelfire), static corporate websites.
Web 2.0 (The Social Web / Read-Write Web - early 2000s - present):

Characteristics:
User-Generated Content: Users became active participants, creating and sharing content.
Interactivity: Richer user interfaces, AJAX, and dynamic content.
Social Networking: Rise of social media platforms, blogs, wikis, and forums.
Collaboration: Emphasis on collaboration and information sharing.
APIs: Extensive use of APIs to connect different web services.
Cloud Computing: Increased reliance on cloud infrastructure.
Examples: Facebook, Twitter, YouTube, Wikipedia, Amazon, Google Maps.


Web 3.0 (The Semantic Web / Decentralized Web - present & future):

Characteristics:
Decentralization: Moving away from centralized servers and data ownership. Powered by blockchain technology.
Semantic Web: Aims to make internet data machine-readable and understandable, enabling intelligent applications.
Artificial Intelligence (AI) & Machine Learning (ML): AI and ML will play a crucial role in processing and understanding data.
Ubiquitous Connectivity: Access across various devices (IoT, smart devices).
Personalization & Contextualization: More intelligent and personalized user experiences.
Privacy & Data Ownership: Greater control for users over their own data.
Technologies: Blockchain, Cryptocurrencies, NFTs, AI, Machine Learning, Decentralized Autonomous Organizations (DAOs).

Examples: Decentralized applications (dApps), metaverses, AI-powered virtual assistants, self-sovereign identity solutions. (Many aspects are still under development).

Here's a visual summary of Web Evolution:
![alt text](image-5.png)

---

