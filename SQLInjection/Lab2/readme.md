Lab: SQL injection vulnerability allowing login bypass
This lab contains a SQL injection vulnerability in the login function.

To solve the lab, perform a SQL injection attack that logs in to the application as the administrator user.

Solution
Use Burp Suite to intercept and modify the login request.
Modify the username parameter, giving it the value: administrator'--
