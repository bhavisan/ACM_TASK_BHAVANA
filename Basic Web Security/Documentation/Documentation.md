In the Tasks/ Identifying Issues folder, I have used several methods for identifying security issues. Here are some common issues that I noticed and how they could be solved:

1. Improper Input Validation:

      Improper Input Validation occurs when user inputs has not been properly sanitized before processing and it can make it vulnerable to SQL injections and Cross Site Scripting (XSS). Not properly validating user inputs can allow attackers to inject malicious content or perform unauthorized actions.

   This can occur when user input fields are not properly formatted, for instance, allowing special characters in username or password. Or, it can occur when application cannot handle input that is too large or too small which allows overload and crash.

   One way to prevent security vulnerabilities is to parametrize queries instead of directly embedding user input into SQL query.

   Another point is to ensure passwords are never stored as plain text, but rather as hashes.

   Ensure the special characters are rendered as text and not executable code by using functions like 'htmlspecialchars'. If the special characters are rendered as executable code, we can easily conduct SQL injections or XSS.

   EXAMPLES:

   <i> SELECT * FROM users WHERE username = 'admin' OR '1'='1'; </i>
   
   <i> <script>alert('Hacked!');</script> </i>


2. Exposing Sensitive Information in Page Source:

    For one of the bugs in CSRF, I was able to manipulate transferring amount into a particular account because the page source contained sensitive information. Sensitive information such as account numbers and transfer amounts were exposed in the page source.

   A solution to CSRF is to generate a unique token for each user session and include it in forms. This ensures that requests made without the correct token can be rejected.

    <i> session_start(); </i>

    <i> $_SESSION['csrf_token'] = bin2hex(random_bytes(32));</i>


  Set the SameSite attribute for cookies to Lax or Strict to prevent the browser from sending cookies along with cross-site requests. This minimizes the risk of CSRF attacks by ensuring that requests made from other origins cannot include the user's authentication cookies.

3. 
