

Introduction to SQL Injection

- SQL Injection (SQLi) is a web application injection vulnerability that occurs when an attacker injects malicious SQL statements into an application's input field
- This occurs when a web application does not properly validate user input, allowing an attacker to inject SQL code/queries that can manipulate the database or gain access to sensitive information
- For example, suppose a website has a login form that accepts a username and password. If the website does not properly validate the user's input, and attacker could enter a malicious SQL statement into the username field that would allow them to bypass the login process and gain access to the website's data.
- SQLi attacks can have serious consequences, including the theft of sensitive data, unauthorized access to sensitive systems, and even full system compromise.
- Complex web applications generally use a database for storing data, user credentials or statistics.
- Content Management Systems (CMSs), as well as simple web pages, can connect to relational databases such as MySQL, MSSQL, SQL Server, Oracle, PostgreSQL and other.
- To interact with databases, entities such as system operators, programmers, applications and web applications use the Structured Query Language(SQL).
- The term "SQL Injection" was coined by Jeff Forristal, also known as "Rain Forest Puppy", in a paper he presented at the DefCon 8 conference in 2000.
- Types of SQL Injection Vulnerabilities:
![[Pasted image 20250818115359.png]]


In-Band SQL Injection

- the attacker injects malicious SQL code into the web application and receives the results of the attack through the same channel used to submit the code

![[Pasted image 20250818115844.png]]

In-band SQL injection can be further divided into 2 subtypes/exploitation techniques:
- Error-based SQL injection: In error-based SQL injection, the attacker injects SQL code that causes the web application to generate an error message. The error message can contain valuable information about the database schema or the contents of the database itself, which the attacker can use to further exploit the vulnerability
- Union-based SQL injection: In union-based SQL injection, the attacker uses the UNION operator to combine the results of two or more SQL queries into a single result set. By manipulating the inject SQL code, the attacker can extract data from the database that they are not authorized to access.

Blind SQL Injection

Blind SQL Injection is a type of SQL injection attack where an attacker can exploit a vulnerability in a web application that does not directly reveal information about the database or the results of the injected SQL query
In this type of attack, the attacker injects malicious SQL code into the application's input field, but the application does not return any useful information or error message to the attacker in the response
The attacker typically uses various techniques to infer information about the database, such as time delays or Boolean logic
The attacker may inject SQL code that causes the application to delay for a specified amount of time, depending on the result of a query.
Blind SQLi can be further divided into 2 subtypes:
- Boolean-based SQLi: in this type of attack, the attacker exploits the application's response to boolean conditions to infer information about the database
- Time-based Blind injection: In this type of attack, the attacker exploits the application's response time to infer information about database. The attacker sends a malicious SQL query to the application and measures the time it takes for the application to respond

![[Pasted image 20250818122901.png]]


Out-of-band SQL Injection

Out of band SQLi is the least common type of SQLi attack. It involves an attacker exploiting a vulnerability in a web application to extract data from a database using a different channel, other than the web application itself.

![[Pasted image 20250818123227.png]]

