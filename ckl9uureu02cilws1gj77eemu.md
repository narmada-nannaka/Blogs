## How Gmail and WordPress Login works

Most of us login into emails, social networking sites with our own credentials. The concept of logging helps to display the information which is only customized for that particular user. This customization helps to improve sales for any company, however there is more than sales in this logging sequence. The most important thing is different websites use different approaches to handle the logging sequences.

This post mainly discusses how gmail and wordpress.com handle the layout and interaction sequence for logging in.

[![gmail](../../uploads/2013/03/gmail1-1.jpg?w=300)](https://narmadanannaka.com/wp-content/uploads/2013/03/gmail1-1.jpg)

First when gmail page is loaded, it uses a javascript to check the version of the browser and OS being used by the user, later it tries to calculate the round-trip for one pixel image to know the speed of the internet connection being used by the user. Once the page loads fully one can find the URL has the part: https://www.google.com/accounts/ServiceLoginAuth?service=mail which means it is pointing to the mail service in the google looking forward to authenticate the service is available for the user. Divs and forms are used by gmail for the layout purpose and posts the input to the server to authenticate the user.[![login](../../uploads/2013/03/login-1.jpg?w=300)](https://narmadanannaka.com/wp-content/uploads/2013/03/login-1.jpg)<span style="font-style: inherit; line-height: 1.625;">Once the user is verified, logging takes place. It loads the appropriate page of the user by pointing to the appropriate service by setting the session id and cookies. It later uses the AJAX web requests to start loading all the mails, labels and channels for the user.</span>

[![logged](../../uploads/2013/03/logged-1.jpg?w=300)](https://narmadanannaka.com/wp-content/uploads/2013/03/logged-1.jpg)

As session is maintained in the browser, even though if we try to open gmail in another page, it gives opens our gmail account rather than displaying the login page as shown above. This same session is maintained even though multiple browsers are used.

When it comes to WordPress, it doesn’t use the global session variables to keep track of the logins, it is stateless. It uses the cookies to store this information.

[![wp](../../uploads/2013/03/wp-1.jpg?w=300)](https://narmadanannaka.com/wp-content/uploads/2013/03/wp-1.jpg)

The above is the login page for wordpress site which uses divs and form inputs for the username and password fields in the layout. The placeholders are used to display the content in the text boxes provided for username and password as shown in the image.

There is more to explore into the architecture of logging for these sites, this is just a drop in the ocean.

References: http://www.sajithmr.me/gmail-architecture