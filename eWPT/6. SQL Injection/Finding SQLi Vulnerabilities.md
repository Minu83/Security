
Common injectable fields:
- Login forms: the username and password fields in a login form are common targets for SQL injection attacks
- Search boxes: input fields used for searching within an application are potential targets for SQLi
- URL parameters: web applications often use URL parameters to pass data between pages
- Form fields: Any input fields in forms, such as registration forms, contact  forms, or comment fields
- Hidden fields: Hidden fields in HTML forms can be susceptible to SQLi attacks
- Cookies: in some cases, cookies contains user data or session information may be used in SQL queries.

Identifying SQ injection vulnerabilities:

Manual Testing

- Manual testing with malicious input: try injecting SQL statements or special characters into input fields such as forms, search boxes or URL parameters
- Error-based testing: Submitting intentionally malformed input to trigger SQL errors can reveal underlying database errors or SQL statements being executed
- 