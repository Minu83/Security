


Web Application  Architecture

- Web application architecture refers to the structure and organization of components and technologies used to build a web application
- It defines how different parts of the application interact with each other to deliver its functionality, handle user requests and manage data
- A well-designed web application architecture is crucial for ensuring scalability, maintainability and security
- Before performing a security assessment on a web application, it is vitally important to know how web applications work with regards to the underlying architecture.

Client-Server Model

Web applications are typically built on the client-server model. In this architecture, the web application is divided into two main components:
**Client**: the client represents the user interface and user interaction with the web application. In the front-end of the application that users access through their web browsers. The client is responsible for displaying the web pages, handling user input, and sending requests to the server for data or actions.
**Server**: The server represents the back-end of the application. It processes client requests, executes the application's business logic, communicates with databases and other services and generates responses to be sent back to the client.

![[client-server model.png]]



==Web Application Components==

**User Interface(UI)** - The user interface is the visual presentation of the web application seen and interacted with by users. It includes elements such as web pages, forms, menus, buttons and other interactive components.

**Client-Side Technologies** - Client-Side technologies, such as HTML, CSS and JavaScript are used to create the user interface and handle within the user's web browser.

**Server-Side Technologies** - Server-side technologies, such as programming languages(e.g. PHP, Python, Java, Ruby) and frameworks, are used to implement the application's business logic, process requests from clients, access databases and generate dynamic content to be sent back to the client.

**Databases** - Databases are used to store and manage the web application's data. They store user information, content, configurations, and other relevant data required for the application's operation.

**Application Logic** - The application logic represents the rules and procedures that govern how the web application functions. It includes authentication, data validation, security checks, and other business rules.

**Web** **Servers** - Web servers handle the initial request from clients and serve the client-side components, such as static files(HTML, CSS, JavaScript) to the users.

**Application Servers** - Application servers execute the server side code and handle the dynamic processing of client requests. They communicate with databases, perform business logic and generate dynamic content.

