General Methodology for pentesting applications:
1. Map the application: visit the application, learn how it works, find end points, differnet input vectors that talk to the database
2. If talking to database, use SQL characters
3. Check if its vulnerable to SQL injection and inject payloads

   
- SQL Injection
- XSS - ability to execute arbitrary javascript on a user's browser. We have access to user's session and all information and authentication associated with that.
    1. Reflected XSS: reflects the attack directly as a result of HTTP request
    2. Stored XSS: attack is stored in a database and launched when user visits a certain page
    3. DOM XSS: input corrupts the way javascript is manipulating the DOM

Sink = method or function that causes malicious JS to be injected into a page
.innerHTML sink = script tag won't be executed. 
jQuery is recognised by $ (selector)

In order for a CSRF to be possible:
- A relevant action: change a users email
- Cookie - based session handling: session cookie
- No unpredictable request parameters

Cross Site Request Forgery: is an attack where the attacker causes the victim user to carry out an action unintentionally while the user is authenticated. (User has to already be logged in)

Finding CSRF Vulnerabilities:
Black box: URL and credentials - Map the application - check the conditions
White box: source code - identify the framework 
