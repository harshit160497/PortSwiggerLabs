Lab: User ID controlled by request parameter, with unpredictable user IDs

LAB
Not solved
This lab has a horizontal privilege escalation vulnerability on the user account page, but identifies users with GUIDs.

To solve the lab, find the GUID for carlos, then submit his API key as the solution.

You can log in to your own account using the following credentials: wiener:peter

Solution-
Find a blog post by carlos.
Click on carlos and observe that the URL contains his user ID. Make a note of this ID.
Log in using the supplied credentials and access your account page.
Change the "id" parameter to the saved user ID.
Retrieve and submit the API key.
