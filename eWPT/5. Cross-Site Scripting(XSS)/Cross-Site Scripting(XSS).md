
Cross-Site Scripting(XSS) is a client-site web vulnerability that allows attackers to inject malicious scripts into web pages
This vulnerability is typically caused by a lack of input sanitization/validation in web applications
Attackers leverage XSS vulnerabilities to inject malicious code into web applications. Because XSS is a client side vulnerability, these scripts are executed by the victims browser
XSS vulnerabilities affect web applications that lack input validation and leverage client-side scripting languages live Javascript, Flash, CSS etc
XSS vulnerabilities/attacks are typically sorted into 2 main categories:
 - stored/persistent
 - reflected
XSS attacks are typically exploited for the following objectives:
- Cookies stealing/Session hijacking - Stealing cookies from users with authenticated sessions, allowing you to login as other users by leveraging the authentication information contained with a cookie
- Browser exploitation - Exploitation of browser vulnerabilities
- Keylogging - Logging keyboard entries made by the other users on a web application
- Phishing - Injecting fake login forms into a webpage to capture them


Stored XSS

- Is a vulnerability where an attacker is able to inject Javascript code into a web application's database or source code via an input that is not sanitized

![[Pasted image 20250320101647.png]]


Reflected XSS

Reflected/non-persistent cross-site scripting is the most common form of XSS and involves tricking a victim into clicking a specially crafted link (with an XSS payload) to the vulnerable website
When the victim clicks on the link the website includes the XSS payload as part of the response back to the victims browser, where the payload is executed

![[Pasted image 20250320102056.png]]


JavaScript Primer


