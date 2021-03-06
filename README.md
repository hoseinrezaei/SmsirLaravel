<p align="center"><img src="https://www.sms.ir/wp-content/themes/sms.ir/assets/img/final-sms-logo.png"></p>

<p align="center">Official Laravel Package for sms.ir</p>



[![Latest Stable Version](https://poser.pugx.org/ipecompany/smsirlaravel/v/stable)](https://packagist.org/packages/ipecompany/smsirlaravel)
[![Total Downloads](https://poser.pugx.org/ipecompany/smsirlaravel/downloads)](https://packagist.org/packages/ipecompany/smsirlaravel)
[![Monthly Downloads](https://poser.pugx.org/ipecompany/smsirlaravel/d/monthly)](https://packagist.org/packages/ipecompany/smsirlaravel)
[![License](https://poser.pugx.org/ipecompany/smsirlaravel/license)](https://packagist.org/packages/ipecompany/smsirlaravel)



<a align="center" href="https://www.sms.ir/%D8%AE%D8%AF%D9%85%D8%A7%D8%AA/%D9%88%D8%A8-%D8%B3%D8%B1%D9%88%DB%8C%D8%B3/%D8%A7%D8%B1%D8%B3%D8%A7%D9%84-%D9%BE%DB%8C%D8%A7%D9%85%DA%A9-laravel/">آموزش فارسی نصب و استفاده از پکیج ارسال پیامک لاراول</a>


رفع مشکل نصب پکیج sms.ir بر روی laravel 5.8
با این روش میتوانید بر روی نسخه 5.8 laravel به راحتی این پیکج رو نصب کنید


<a align="center" href="https://hosein-rezaei.ir">اصلاح شده توسط حسین رضایی</a>

Website :
<a align="center" href="http://hosein-rezaei.ir">hosein-rezaei.ir</a>

Email :
hosein.rezaei72@gmail.com

در فایل env تمامی موارد را به شکل زیر که توضیح داده شده است اصلاح نمایید
بجای "-" از "_" استفاده نمایید

Hi, if you have an account in sms.ir, you can use this package for laravel

----------


How to install:
-------------

    composer require hoseinrezaei/smsirlaravel:dev-master
    php artisan vendor:publish
    php artisan migrate

> **Setup:**

add this line to your app.php providers:
ipecompany\smsirlaravel\SmsirlaravelServiceProvider::class,

and add this line to your app.php aliases:
'Smsirlaravel' => ipecompany\smsirlaravel\SmsirlaravelFacade::class,


> After publish the package files you must open smsirlaravel.php in config folder and set the api-key, secret-key and your sms line number.
> 

> **Like this:**

	'webservice-url' => env('SMSIR-WEBSERVICE-URL','https://ws.sms.ir/'),
	'api-key' => env('SMSIR_API_KEY','Your sms.ir api key'),
	'secret-key' => env('SMSIR_SECRET_KEY','Your sms.ir secret key'),
	'line-number' => env('SMSIR_LINE_NUMBER','Your sms.ir line number'
> 
> Note:

you can set the keys and line number in your .env file

> **like this:**

> SMSIR_WEBSERVICE_URL=https://ws.sms.ir/

> SMSIR_API_KEY=your api-key

> SMSIR_SECRET_KEY=your secret-key

> SMSIR_LINE_NUMBER=1000465******



Methods:
-------------

> Smsirlaravel::send()

> Smsirlaravel::credit()

> Smsirlaravel::getLines()

> Smsirlaravel::addToCustomerClub()

> Smsirlaravel::deleteContact();

> Smsirlaravel::sendToCustomerClub();

> Smsirlaravel::addContactAndSend();

> Smsirlaravel::sendVerification();

> Smsirlaravel::ultraFastSend();

> Smsirlaravel::getSentMessages();

> Smsirlaravel::getReceivedMessages();

