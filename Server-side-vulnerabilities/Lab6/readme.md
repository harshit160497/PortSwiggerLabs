Lab: User ID controlled by request parameter with password disclosure

This lab has user account page that contains the current user's existing password, prefilled in a masked input.

To solve the lab, retrieve the administrator's password, then use it to delete the user carlos.

You can log in to your own account using the following credentials: wiener:peter


Solution-
Log in using the supplied credentials and access the user account page.
Change the "id" parameter in the URL to administrator.
View the response in Burp and observe that it contains the administrator's password.
Log in to the administrator account and delete carlos.
