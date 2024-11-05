

Introduction to SQL Injection

- SQL Injection (SQLi) is a web application injection vulnerability that occurs when an attacker injects malicious SQL statements into an application's input field
- This occurs when a web application does not properly validate user input, allowing an attacker to inject SQL code/queries that can manipulate the database or gain access to sensitive information
- For example, suppose a website has a login form that accepts a username and password. If the website does not properly validate the user's input, and attacker could enter a malicious SQL statement into the username field that would allow them to bypass the login process and gain access to the website's data.
- SQLi attacks can have serious concequonces, including the theft of sensitive data, unauthorized access to sensitive systems, and even full system compromise.
- Complex web applications generally use a database for storing data, user credentials or statistics.
- Content Management Systems (CMSs), as well as simple web pages, can connect to relational databases such as MySQL, MSSQL, SQL Server, Oracle, PostgreSQL and other.
- To interact with databases, entities such as system operators, programmers, applications and web applications use the Structured Query Language(SQL).
- The term "SQL Injection" was coined by Jeff Forristal, also known as "Rain Forest Puppy", in a paper he presented at the DefCon 8 conference in 2000.
- 