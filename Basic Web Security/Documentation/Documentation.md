In the Tasks/ Identifying Issues folder, I have used several methods for identifying security issues. Here are some common issues that I noticed and how they could be solved:

1. Improper Input Validation:

      Improper Input Validation occurs when user inputs has not been properly sanitized before processing and it can make it vulnerable to SQL injections and Cross Site Scripting (XSS). Not properly validating user inputs can allow attackers to inject malicious content or perform unauthorized actions.

   This can occur when user input fields are not properly formatted, for instance, allowing dangerous special characters in username or password. Or, it can occur when application cannot handle input that is too large or too small which allows overload and crash.

   One way to prevent security vulnerabilities is to parametrize queries instead of directly embedding user input into SQL query.

Normally;
      username = "admin' OR '1'='1'"
      query = "Select * from users where username = '" + username + "'";

Here the query becomes: Select * from users where username = 'admin' OR '1' = '1';
Since 1 = 1 is always true, all users are returned. 

Instead, we use:
      username = "admin' OR '1'='1'"
      query = "Select * from users where username = %s";

Here the database treats  'admin' OR '1' = '1' as string rather than SQL code

   Another point is to ensure passwords are never stored as plain text, but rather as hashes.

   Ensure the special characters are rendered as text and not executable code by using functions like 'htmlspecialchars'. If the special characters are rendered as executable code, we can easily conduct SQL injections or XSS.

   EXAMPLE:
   
   <i> <script>alert('Hacked!');</script> </i>


3. Exposing Sensitive Information in Page Source:

    For one of the bugs in CSRF, I was able to manipulate transferring amount into a particular account because the page source contained sensitive information. Sensitive information such as account numbers and transfer amounts were exposed in the page source.

   A solution to CSRF is to generate a unique token for each user session and include it in forms. This ensures that requests made without the correct token can be rejected.

    <i> session_start(); </i>

    <i> $_SESSION['csrf_token'] = bin2hex(random_bytes(32));</i>


 Preventing CSRF Vulnerabilities:
 1. Primary Defense: Use CSRF tokens - these are unpredictable (long, random string), tied to user's session, validated before the relevant action is executed.
 2. SameSite Cookies: it is an attribute that can be used to control whether cookies are submitted in cross - site requests. Can be set to Strict, Lax or None.
     - Strict: Cookies will only be sent if the request originates from the same site.
     - Lax: Cookies will be sent with top - level navigation to the site
     - None but Secure: Cookies are sent with all requests but only over HTTPS.

