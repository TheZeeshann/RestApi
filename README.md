# REST API SYSTEM

This API is developed using the PHP Slim Framework, In this api you can use thease feature.

* Create an account (An email verification will be sent to user email address when they rgistered an account)
* Login into account (User can login into their account when they will successfully verified their account)
* Send Email Verification Code (You can add a feature that user can send email verifcation code again to their email address)
* Update Password (User can update password, An email will also be send when they succesfully changed their password)


## Feauter Explanation

To use this project's feature, you need to make changes only in `Constants.php` file, and that's it.

Set your database connection's information.
```bash
//Database Connection
define('DB_NAME', 'socialcodia');    //your database username
define('DB_USER', 'root');          //your database name
define('DB_PASS', '');              //your database password
define('DB_HOST', 'localhost');     //your database host name
```

And you also need to make change in website section of `Constants.php` file.

```bash

//Website Information
define('WEBSITE_DOMAIN', 'http://api.socialcodia.ml');               //your domain name
define('WEBSITE_EMAIL', 'socialcodia@gmail.com');                    //your email address
define('WEBSITE_EMAIL_PASSWORD', 'password');                        //your email password
define('WEBSITE_EMAIL_FROM', 'Social Codia');                        // your website name here
define('WEBSITE_NAME', 'Social Codia');                              //your website name here
define('WEBSITE_OWNER_NAME', 'Umair Farooqui');                      //your name, we will send this name with email verification mail.

```

## Register An Account

To Create An Account, Accept only post request with three parameter
* Name
* Email
* Password

The end point is to Create or Register an accout is `createUser`

<b>Full Demo Url</b> <a href="http://api.socialcodia.ml/createUser">http://api.socialcodia.ml/createUser</a>


An email verification will be send to user email address when they registered an account into the system.

In verification email the verification link will be like this.

```bash

    http://api.socialcodia.ml/verifyEmail/wdpWwmufazmit4Py2aYd7MsocialcodiavknYY3bKxS7okyO9NgpYTmufazmiTGsocialcodiaE=/$2y$10$GWEv1cnJo2YdGbmo4mrwA.LNsocialcodiai4sj8.EdxIZuyWX3fjRHEiBrBX2S

```
* Domain Name : (` http://api.socialcodia.ml/ `)
* End Point (` verifyEmail `)
* Encypted User Email (` wdpWwmufazmit4Py2aYd7MsocialcodiavknYY3bKxS7okyO9NgpYTmufazmiTGsocialcodiaE= `)
* Encypted Code ( `$2y$10$GWEv1cnJo2YdGbmo4mrwA.LNsocialcodiai4sj8.EdxIZuyWX3fjRHEiBrBX2S` )

<p align="center">
    <img src="https://i.imgur.com/AGeCYFR.png" >
</p>

<b>Full Demo Url</b> <a href="http://api.socialcodia.ml/verifyEmail/wdpWwmufazmit4Py2aYd7MsocialcodiavknYY3bKxS7okyO9NgpYTmufazmiTGsocialcodiaE=/$2y$10$GWEv1cnJo2YdGbmo4mrwA.LNsocialcodiai4sj8.EdxIZuyWX3fjRHEiBrBX2S">http://api.socialcodia.ml/verifyEmail/wdpWwmufazmit4Py2aYd7MsocialcodiavknYY3bKxS7okyO9NgpYTmufazmiTGsocialcodiaE=/$2y$10$GWEv1cnJo2YdGbmo4mrwA.LNsocialcodiai4sj8.EdxIZuyWX3fjRHEiBrBX2S</a>


## Send Email Verification Code Again

To Send The Email Verification Code again, Accept only post request with only one parameter
* Email

User can make the send email verification link code if there email address is not verified yet.

The end point of send email verification code is `updatePassword`

<b>Full Demo Url</b> <a href="http://api.socialcodia.ml/updatePassword">http://api.socialcodia.ml/updatePassword</a>


## Login Into Account

To Login into Account, Accept only post request with two parameter
* Email
* Password

The end point of login is `login`

<b>Full Demo Url</b> <a href="http://api.socialcodia.ml/login">http://api.socialcodia.ml/login</a>


## Update Account Password

To update or changed the current password, Accept only post request with three parameter
* Email
* Password
* newPassword

The end point of update password is `updatePassword`

<b>Full Demo Url</b> <a href="http://api.socialcodia.ml/updatePassword">http://api.socialcodia.ml/updatePassword</a>

an verification code will be sent to user email address when they successfull updated their password.

### At the end

you don't need to worry about that things, you need to change the code in `Constants.php` Php

That's it! Now go build something cool.
