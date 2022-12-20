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

Helper is a way which helpes you to access [documentation](https://github.com/MiheerMantraLabs/Documentary/) as fast.
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


## Custom Errors

This funtion is to help you to organise your errors and customs for any kind of issues.
You can define them once having any ID and use them again and again by ID only.
First,

- >Go to ***`___dir___/public/storage/errorTheme/errors.json`***  file and set your Error there with their ids.

To use  it simply call a function 

        ERROR('E-10001');

where,

***`E-10001`*** = `is error id` <sup>( required)<sup>



## Api Throttle Limits

This function newly introduced in laravel base project which is designed to limit yours apis throttles as such.
This works for `API ROUTES` only.

**How to implement :**
- >Go to ***`___dir___/public/config.json`***  file and set your limit in integer form.
- >To check number of throttles of particuler api routes go to ***`___dir___/storage/Throttle`*** open api files as such.
- >File formated as : **`file_name___date___THROTTLE.txt`**

## E-mail

**Step : 1 - Configer mailer records**
- >Go to file ***`.env`***
- >Files all the details correct over there from you mail provider in the following way given below : 

        MAIL_MAILER=smtp
        MAIL_HOST=smtp.mailtrap.io
        MAIL_PORT=2525
        MAIL_USERNAME=8497962f81a386
        MAIL_PASSWORD=e1a750518f307c
        MAIL_ENCRYPTION=tls


**Step : 2 - Email Templates**
- > There are two ways to use templates
    - >**FIRST : DEFAULT THEMES**
        - In this method we provides you auto created templates which you can use
        - To get these templates go to ***`___dir___/resources/emailThemes/`*** and you will get multiples files overthere, which are pre-created themes

    - >**MUST READ :**
        - If you want to replace any thing section or variable in the email template dynamically ***`(like : Header,Footer,Body,Banner,Button,Link,name,details etc)`*** you can make a key in place of that section as : **`{!!SECTION-NAME!!} or {!!VARIABLE-NAME!!}`** .  



**Step : 3 - Configer Email**
- >Go to ***`___dir___/storage/notifyTheme/notifications.json`***
- >Define you email in such way with a notification key like this `"N-10001":{ YOUR_CODE_HERE }`

Notification Config Code

    "N-10001":{
        "TYPE":"email",
        "VIEW":"emailThemes.otp_view",
        "SUBJECT":"Hello ${name}",
        "BODY":{
            "title":"Laravel",
            "welcome":"Hi, ${name}",
            "messages":"Your otp for <a>email@email.com </a> is :",
            "otp":"000000",
            "link":"http://www.laravel.com/",
            "notice":"You have received this mandatory service announcement to update you about important changes to Laravel or your account.",
            "contact":"Laravel LLC<br>1600 Amphitheatre Parkway<br> Mountain View, CA, 231303<br>India",
            "banner":"https://cdn.icon-icons.com/icons2/2699/PNG/512/laravel_logo_icon_170314.png"
        }
    }
    

Each keys is required expect details inside `EMAIL_BODY` key those are replacable data from template as Header,footer.name,details,keys etc

If you want replace data of `EMAIL_SUBJECT`or`EMAIL_BODY`dynamically with php variables place them as `${KEY_NAME}`




**Step : 5 - Send Email**

Once you finished all the steps & after previewing the email theme you are readdy to send the email now.

To send the email we have a funtion ***`SendNofityMail()`***

    SendNofityMail('TO','NOTIFICATION_ID',array(
        "otp" => $otp,
        "name" => $name
    ));

where,

***`to`*** = `to whome you want to send the message` <sup>( required)<sup>


***`notification_id`*** = `JSON NOTIFICATION ID (ex-N-10001)` <sup>( required)<sup>


***`array() with keys`*** = `replacement of php variables or sections from json in email (ex-{$key_names})`


## Pusher Notification

**SEND PUSHER NOTIFICATION**

First Go To [Pusher](https://pusher.com/) and register your account & register your project there, and go to `dashboard/Get Started` & check for the function to **server** code using PHP. <img src="https://ourimagehosting.com/images/2022/10/03/image.png" hieght="20px" width="50px" alt="php-select">

<sup>Must read : Do not run the given composer command....</sup>

- >Go to file ***`___dir___/notify/pusher/config.php`***
- >Paste Your Pusher Server Code There.

To Send Call Function **`SendNotifyPush()`**

    SendNotifyPush("message","channel","event");

where,

***`message`*** = `Notification message to be sent` <sup>( required)<sup>

***`channel`*** = `you can change custom channal if you want to..`

**`event`** = `you can change custome event if you want to...`



**RECIEVE PUSHER NOTIFICATION**

First Go To [Pusher](https://pusher.com/) and register your account & register your project there, and go to `dashboard/Get Started` & check for the function to **subscribe** code using Javascript. <img src="https://ourimagehosting.com/images/2022/10/03/image08454e00213b9b41.png" hieght="20px" width="50px" alt="php-select">

- >Copy Javascript Subscribe function both scripts.
- >Customise them accrodingly.
- >Paste in the blade page where you want to recieve notification.


## Send SMS

- >Go to file ***`___dir___/notify/sms/config.php`***
- >Paste Your SMS API Integration Code There.

To Send Call Function **`SendNofitySms()`**

    SendNotifyPush(array());

where,

***`array`*** = `This is a set of array in case if you want to send any value over there.`


## Encrypt & Decrypt

**How To Encrypt Data**

To Encrypt the data pass you data through a function **`text_encrypt("Your Text Goes Here")`**

    TEXT_ENCRYPT("Hello World!");

**How To Decrypt Data**

To decrypt the data pass you data through a function **`text_decrypt("Your Encrypted Text Goes Here")`**

    TEXT_DECRYPT("0nR8web9T0mvcpXx");

## APP_ENV (.env) saperation & configuration

**How to change `.env` to `.env.APP_ENV` file while using development**

While development to testing or any thing if you want to change .env file you just need to run a simple command php artisan <img src="https://img.shields.io/badge/php%20artisan%20config%3Acache%20----env%3Dproduction-%20-lightgrey" alt="php artisan config:cache --env=testing
">

Here In the given command you just need to specify the env file.

<sup>Must read : When sending to product to production server you have to use .env file only, for that you can change your specific env file to .env file & previous .env file to any other like .env.example</sup>



## Use Any Possible Databases

We have povided all dbs possible drivers in ***`___dir___/config/database.php`***

- >To Change Database, go to ***`___dir___/config/database.php`***
- >Customise following and you can add more drivers for multi databases.
- >Replace db connection from **`default' => env('DB_CONNECTION', 'mysql')`**

For Example 

    default' => env('DB_CONNECTION', 'mysql') <=====> default' => env('DB_CONNECTION', 'mongodb')

- >Provide credentials in <sup>***`.env`***</sup> file
- >All set.

**Thank you so much to accessing our documentary**