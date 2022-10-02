<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel Base Project

Laravel Base Project is a a upgraded version of Laravel Framework. We have designed custom functions which makes your work easy & efficient. We have multiple extra ordinary functionalities which could be perform by writing a single line of code, as such:

- Simple and Fast
- Advance Logger & Throttle api limits.
- Automated Mailing system.
- Auto encryption & Decryption(For texts & requests both)
- Standered Fuctions for thrid parties.
- Standered methods for notifications & errors.
- Writing provisions for master & salve type of Databases.
- All posible types of database drivers avilability.

## Installation & setup

- > Download the project from our [Git repository](https://www.laravel.com/).
- > Extract the project to particular folder.
- > Open <img src="https://img.shields.io/badge/Terminal------blue" alt="Terminal"> inside of project folder & run a this command : <img src="https://img.shields.io/badge/composer%20update-%20-lightgrey" alt="composer update">
- > Once composer installed successfully, copy ***`.env.example`*** file and paste it as ***`.env`***  file.
- > Again run another command <img src="https://img.shields.io/badge/php%20artisan%20key%3Agenerate-%20-lightgrey" alt="php artisan key:generate"> to generate a new key in ***`.env`*** file.
- > Now All set Everything is up to date.
- > Now you can run the project using a command <img src="https://img.shields.io/badge/php%20artisan%20serve-%20-lightgrey" alt="php artisan serve">

## Helpers

Helper is a way which helpes you to access [documentation](https://miheer-mantra.gitbook.io/documentation/) as fast.
- > Install helper using command <img src="https://img.shields.io/badge/php%20artisan%20create%3Ahelper-%20-lightgrey" alt="php artisan create:helper">
- > It will `create` a new fab <img src="https://ourimagehosting.com/images/2022/10/01/image.png" alt="fab" width="35px" hieght="35px">
- > Install helper using command <img src="https://img.shields.io/badge/php%20artisan%20delete%3Ahelper-%20-lightgrey" alt="php artisan delete:helper">
- > It will `delete` a this  fab <img src="https://ourimagehosting.com/images/2022/10/01/image.png" alt="fab" width="35px" hieght="35px">

## Advance Logger

This function provides you advance logging system.
To get this logger go to following repository ***`___dir___/storage/logs/logger/`*** and you can see all the logged of the days is stored.

**How to implement :**
- >Go to repo ***`___dir___/storage/logs/logger/`*** 
- >Go to file of particular date.
- >File formated as (For REQUESTED DATA) : **`date___LOG_Request.txt`**
- >File formated as (For RESPONCE DATA) : **`date___LOG_Responce.txt`**
- >Details are store in the given ways : 
    - >**`_Date_   /   _Time_  /  _Url_    /   _IP_Address_    /    _Req_Methods_  /   _Req_Datas_     /   _Header_Data_`**

## Api Throttle Limits

This function newly introduced in laravel base project which is designed to limit yours apis throttles as such.
This works for `API ROUTES` only.

**How to implement :**
- >Go to ***`___dir___/public/config.json`***  file and set your limit in integer form.
- >To check number of throttles of particuler api routes go to ***`___dir___/storage/Throttle`*** open api files as such.
- >File formated as : **`file_name___date___THROTTLE.txt`**

## E-mail

**Step : 1 - Configer mailer records**
- >Go to file ***`___dir___/notify/email/config.json`***
- >Files all the details correct over there from you mail provider in the following way given below : 
    - `{   `

        `"SMTPDebug":"3",`

        `"SMTPSecure":"tls",`

        `"SMTPHost":"smtp.mailtrap.io",`

        `"SMTPPort":"2525",`

        `"Username":"example@example.com",`

        `"Password":"___e1a750518f307c___",`

        `"Sendername":"example@example.com"`

       `}`

**Step : 2 - Email Templates**
- > There are two ways to use templates
    - >**FIRST : DEFAULT THEMES**
        - In this method we provides you auto created templates which you can use
        - To get these templates go to ***`___dir___/storage/notifyTheme/default/`*** and you will get multiples files overthere, which are pre-created themes

    - >**SECOND : CUSTOM THEME**
        - In this method you can create custom themes in side of ***`___dir___/storage/notifyTheme/custom/`***(If custom folder not available there you can create one)

    - >**MUST READ :**
        - If you want to replace any thing section in the email template dynamically ***`(like : Header,Footer,Body,Banner,Button,Link etc)`*** you can make a key in place of that section as : **`__ __SECTION-NAME__ __`** (Both side double underscore).  

**Step : 3 - Configer Email**
- >Go to ***`___dir___/storage/notifyTheme/notifications.json`***
- >Define you email in such ways

`"N-10001":{
        "NOTIFICATION_CODE":"N-10001",

        "NOTIFICATION_TYPE":"email",

        "RECIEVER":"miheerpnd@gmail.com",

        "TEMPLATE_SECTION":"default",

        "TEMPLATE_NAME":"otp_view.html",

        "EMAIL_SUBJECT":"Hello miheer",

        "EMAIL_BODY":{

            "title":"Laravel",

            "welcome":"Hi, there",

            "message":"Your otp for <a>email@email.com </a> is :",

            "otp":"000000",

            "link":"http://www.laravel.com/",

            "notice":"You have received this mandatory service announcement to update you about important changes to Laravel or your account.",

            "contact":"Laravel LLC<br>1600 Amphitheatre Parkway<br> Mountain View, CA, 231303<br>India",

            "banner":"https://cdn.icon-icons.com/icons2/2699/PNG/512/laravel_logo_icon_170314.png"

        }

    }`

Each keys is required expect details inside `EMAIL_BODY` key those are replacable data from template as Header,footer etc

If you want replace data of `EMAIL_SUBJECT`or`EMAIL_BODY`dynamically with php variables place them as `{$KEY_NAME}`