
### وب سرویس سامانه پیام کوتاه
 
این راهنما جهت سهولت در کار برنامه نویسانی طراحی شده است که قصد دارند سرویس پیامهای خود را به نرم افزار های کاربردی خود ارتباط دهند.
این شرکت در حال حاضر وب سرویس ارسال پیام کوتاه و وب سرویس ارسال پیام صوتی ارئه میکند.
روش های ارائه شده برای ارسال پیام کوتاه به شرح زیرمیباشد
1- وب سرویس REST
2- وب سرویس SOAP
3- ارسال از طریق URL
که از بین روش های ذکر شده این شرکت روش وب سرویس REST را پیشنهاد میدهد.
روش های ارائه شده برای ارسال پیام صوتی به شرح زیرمیباشد:
1- وب سرویس REST
### برخی ارور ها
برخی از ارور هایی که در وب سرویس ها داده میشود به شرح زیر میباشد.


<div dir="rtl">

کد خطا|توضیح|
-| - |
|erorr_login_user_not_found|چنین کاربری یافت نشد|
|error_login_not_like_username|نام کاربری مشکلی دارد مانند وجود فاصله|
|error_login_not_like_password|پسورد مشکلی دارد|
|error_login_not_like_accept|دسترسی شما مسدود شده است و یا کد تایید پیامکی را وارد نکرده اید|
|error_register_taken_email|چنین ایمیلی قبلا استفاده شده است|
|error_register_taken_user_username|نام کاربری قبلا اسفتاده شده است|
|error_register_taken_user_mobile|موبایل قبلا استفاده شده است|
|error_no_receiver|گیرنده های خالی میباشد|
|error_sender_number_is_not_allow|شماره ی ارسال کننده مجاز نمیباشد|
|error_long_request_uniqueid|طول کد یکتا بیشتر از حد مجاز است|
|error_sender_number_is_disable|شماره ی ارسال کننده غیرفعال میباشد|
|error_number_format_error|فرمت شماره ی گیرنده مشکل دارد|
|error_number_whois_error|شماره ی ارسال کننده اجراز هویت نشده است|
|error_sms_receiver_number_limit|تعداد گیرنده ها بیشتر از حد مجاز میباشد|
|error_sms_send_config_is_disable|ارسال از این پیش شماره موقتا غیر فعال میباشد|
|error_sms_price_not_found_for_admin|هزینه ی اراسال پیامک مدیر مشخص نمیباشد|
|error_sms_price_packageid_not_found_for_admin|پکیج قیمت مدیر یافت نشد|
|error_sms_price_not_found_for_user|هزینه ی اراسال پیامک برای کاربر مشخص نمیباشد|
|error_credit_admin_error|شارژ مدیر کم است|
|error_credit_admin_empty_error|هزینه ی ارسال برای مدیر اشتباه محاسبه شده است|
|error_credit_error|کمبود شارژ کاربر|

</div>

<div dir="rtl">

درگاه ها مقادیر ذکر شده در جدول برای تمامی متدهایی که پارامتر dargahha یا dargah دارند قابل استفاده میباشد

</div>


<div dir="rtl">


اپراتور مورد نظر|مقداری که باید استفاده شود|
-| - |
|3000 - مسیر اصلی|3000
|3000 - مسیر فرعی اول|30001
|erorrr|erorrr
|erorrr|erorrr
|3000 - مسیر فرعی دوم|30002
|erorrr|erorrr
|9000 - مسیر اصلی|9000
|50002 مسیر اصلی|50002
|آسانک اصلی|982100
|آرینتل - ارسال گروهی و بالک خدماتی|999800
|3000 - مسیر فرعی سوم|30003
|3000 - مسیر فرعی چهارم|30004
</div>

<div dir="rtl">

وضعیت پیامک ها : وضعیت پیامک ها در سیستم به شرح زیر میباشد.
</div>

<div dir="rtl">


معنا|عدد|
-| - |
|پیام یافت نشد - ممکن است پیام به آرشیو منتقل شده باشد|1-
|بدون وضعیت - ممکن است پیام تازه ارسال شده باشد و در انتظار دریافت وضعیت باشد|0
|رسیده به گوشی|1
|نرسیده به گوشی|2
|ارسال نشده به مخابرات|3
|ارسال شده به مخابرات - ممکن است پیام ها پس از مدت زمانی برای ارسال به آرشیو به این وضعیت تبدیل شوند|4
|لیست سیاه مخابرات - ممکن است به معنای بازگشت وجه نیز باشد|5
|ارسال شده به اپراتور پیامکی|8
|بازگشت هزینه به دلیل ترافیک مخابرات|9
|صف ارسال|10
|اسپم|11
|اکسپایر|12
|بدون روت|13
|ریجکت شده|14
|نرسیده به مخابرات|16
|بدون وضعیت دلیوربیس|17


</div>


<div dir="rtl">

### انتقال پیامک های دریافتی به آدرس
با استفاده از این سرویس پیامک دریافتی شما بلافاصله پس از دریافت به آدرسی که در تنظیمات مشخص کرده اید به صورت POST ارسال میشود.
تذکر تمامی پارامتر هایی که خود شما در آدرس قرار میدهید به صورت GET برای شما ارسال میشوند و فقط پارامتر های زیر که غیر قابل تغییر هستند به صورت POST ارسال میشوند!

</div>


<div dir="rtl">

نام پارامتر|توضیح|
-| - |
|from|شماره ی ارسال کننده ی پیامک مثلا 09132125459
|to|شماره ی دریافت کننده ی پیامک مثلا 3000569999
|note|متن پیامک مثال این یک تست است
|smsid|شناسه ی پیامک مثلا 1234567

</div>

<div dir="rtl">

### فرمت تاریخ
تمامی تاریخ ها بر اساس unix timestamp میباشد.ای تاریخ شامل یک عدد میباشد که از تاریخ January 1st, 1970 at UTC شروع شده است.


</div>


```
PHP	time() 
Python	import time; time.time()
Ruby	Time.now (or Time.new). To display the epoch: Time.now.to_i
Perl	time
Java	long epoch = System.currentTimeMillis()/1000;
C#	var epoch = (DateTime.UtcNow - new DateTime(1970, 1, 1, 0, 0, 0, DateTimeKind.Utc)).TotalSeconds;
Objective-C	[[NSDate date] timeIntervalSince1970]; (returns double) or NSString *currentTimestamp = [NSString stringWithFormat:@"%f", [[NSDate date] timeIntervalSince1970]];
C++11	double now = std::chrono::duration_cast<std::chrono::milliseconds>(std::chrono::system_clock::now().time_since_epoch()).count();
VBScript/ASP	DateDiff("s", "01/01/1970 00:00:00", Now())
AutoIT	_DateDiff('s', "1970/01/01 00:00:00", _NowCalc())
Delphi	Epoch := DateTimetoUnix(Now); Tested in Delphi 2010.
R	as.numeric(Sys.time())
Erlang/OTP	erlang:system_time(seconds). (version 18+), older versions: calendar:datetime_to_gregorian_seconds(calendar:universal_time())-719528*24*3600.
MySQL	SELECT unix_timestamp(now())
PostgreSQL	SELECT extract(epoch FROM now());
SQLite	SELECT strftime('%s', 'now');
Oracle PL/SQL	SELECT (CAST(SYS_EXTRACT_UTC(SYSTIMESTAMP) AS DATE) - TO_DATE('01/01/1970','DD/MM/YYYY')) * 24 * 60 * 60 FROM DUAL;
SQL Server	SELECT DATEDIFF(s, '1970-01-01 00:00:00', GETUTCDATE())
IBM Informix	SELECT dbinfo('utc_current') FROM sysmaster:sysdual;
JavaScript	Math.round(new Date().getTime()/1000.0) getTime() returns time in milliseconds.
Visual FoxPro	DATETIME() - {^1970/01/01 00:00:00} Warning: time zones not handled correctly
Adobe ColdFusion	<cfset epochTime = left(getTickcount(), 10)>
Go	time.Now().Unix()
Tcl/Tk	clock seconds
Unix/Linux Shell	date +%s
PowerShell	[int][double]::Parse((Get-Date (get-date).touniversaltime() -UFormat %s))
Other OS's 	Command line: perl -e "print time" (If Perl is installed on your system)
```


### مفاهیم کلی ارسال پیامک از طریق SOAP
با استفاده از وب‌سرویس این امکان برای شما وجود دارد که یک ارتباط هوشمند و دوطرفه با کاربران وب‌سایت یا نرم‌افزار خود برقرار کنید. به این ترتیب سیستم شما با توجه به نیاز می‌تواند از طریق سامانه پیامک ارسال کند، پیامک‌های دریافتی را از سامانه تحویل گرفته و تحلیل نماید، یا حتی به مدیریت پیامک‌های قبلی بپردازد.

سوپ (SOAP) مخفف Simple Object Access Protocol است. SOAP یک پادمان مبتنی بر XML است، برای رد و بدل کردن اطلاعات بین برنامه ها. اطلاعات در SOAP به صورت پیام (Message) و از طریق پادمان‏های موجود در اینترنت مانند HTTP منتقل می‏شود (SOAP در سایر پادمان ها، مانند SMTP یا MIME نیز قابل استفاده است). به زبان ساده‏تر، SOAP یک پادمان است برای دستیابی به یک سرویس ارایه شده در وب (Web Service). آخرین نسخه SOAP، نسخه 1.2 می‏باشد

### آدرس وب سرویس SOAP:
http://sms.persiafava.com/webservice/soap/smsService.php?wsdl
### آدرس راهنما شامل نام متد ها و پارامتر های ورودی و مقادیر خروجی به شرح زیر میباشد :
http://sms.persiafava.com/webservice/soap/smsService.php
### پیام های دریافتی
از این متد برای گرفتن لیست پیام های دریافتی استفاده می شود.


<div dir="rtl">


نام متد:sms_receive


</div>


<div dir="rtl">


پارامتر|نوع|توضیحات|مقادیر 
-| - | - | -
|username|string|نام کاربری مورد استفاده در سامانه پیامک||
|password|string|رمز عبور مورد استفاده در سامانه پیامک||
|number|string|شماره خط اختصاصی مورد استفاده در سامانه||
|catid|int|شناسه دسته بندی پیامک های دریافتی||
|start|int|از 1 شروع می شود|شناسه شروع لیست پیامک ها|
|perpage|int|تعداد پیامک های دریافتی در هر صفحه|30=پیش فرض|
|read|int|نوع خواندن|مهم نیست = 1- ، خوانده نشد = 0 ، خوانده شد = 1|
|order|string|نوع مرتب سازی|'ASC' = از اول به آخر 'DESC' = از آخر به اول

</div>

<div dir="rtl">

### ارسال پیامک
از این متد برای ارسال پیامک استفاده می شود.

نام متد:send_sms

</div>

<div dir="rtl">


پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|username|string|نام کاربری مورد استفاده در سامانه پیامک||
|password|string|رمز عبور مورد استفاده در سامانه پیامک||
|sender_number|ArrayOfString|شماره ارسال کننده در سامانه پیامک||
|receiver_number|ArrayOfString|شماره دریافت کننده پیامک||
|note|ArrayOfString|متن پیامک ارسالی||
|date|ArrayOfString|(تاریخ ارسال پیامک ( ارسال در آینده ) - این متغیر به صورت آرایه ارسال میشود و میتواند شامل یک یا بیش از یک تاریخ باشد)| 0=هم اکنون ارسال شود |
|request_uniqueid|ArrayOfString|(جهت جلوگیری از ارسال پیامک تکراری از منبع کد , میتوانید این متغیر را با یک عدد یا متن منحصر به فرد مقداردهی کنید . در صورت ارسال درخواست تکراری در پاسخ این متد smsid های قبلی ارسال خواهند شد)| 0=نیازی به چک کردن ندارد |
|flash|ArrayOfString|آیا پیامک به صورت فلش ارسال شود یا خیر| ok , no |
|onlysend|string|جهت ارسال سریع بدون وقفه در زمان ارسال پیامک ( ارسال پیامک با تاخیر 30 ثانیه به مشترک انجام خواهد شد)| ok , no ( ok == ارسال با تاخیر ) |



</div>


<div dir="rtl">

نمونه کد ارسال یک متن برای 2 گیرنده
</div>



```
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:ns1="sms_webservice_wsdl"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/"
xmlns:ns2="urn:sms_webservice_wsdl" SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/">
<SOAP-ENV:Body>
<ns1:send_sms>
<username xsi:type="xsd:string">username here</username>
<password xsi:type="xsd:string">password here</password>
<sender_number SOAP-ENC:arrayType="xsd:string[1]" xsi:type="ns2:ArrayOfString">
<item xsi:type="xsd:string">3000569999</item>
</sender_number>
<receiver_number SOAP-ENC:arrayType="xsd:string[1]" xsi:type="ns2:ArrayOfString">
<item xsi:type="xsd:string">+989126133361</item>
</receiver_number>
<note SOAP-ENC:arrayType="xsd:string[1]" xsi:type="ns2:ArrayOfString">
<item xsi:type="xsd:string">تست</item>
</note>
<date SOAP-ENC:arrayType="xsd:string[1]" xsi:type="ns2:ArrayOfString">
<item xsi:type="xsd:string">0</item>
</date>
<request_uniqueid SOAP-ENC:arrayType="xsd:string[1]" xsi:type="ns2:ArrayOfString">
<item xsi:type="xsd:string"></item>
</request_uniqueid>
<flash SOAP-ENC:arrayType="xsd:string[1]" xsi:type="ns2:ArrayOfString">
<item xsi:type="xsd:string">no</item>
</flash>
<onlysend xsi:type="xsd:string">ok</onlysend>
</ns1:send_sms>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```
<div dir="rtl">


### مفاهیم کلی ارسال پیامک از طریق REST
رست REST بهترین روش برای وب سرویس ها میباشد و در تمامی زبان های برنامه نویسی قابلیت پیاده سازی دارد

در این روش خروجی بر اساس JSON میباشد ( توضیحات بیشتر در مورد JSON)

در این روش شما میتوانید با یکی از متد های POST یا GET اطلاعات را برای وب سرویس ارسال نمایید

نمونه کد ارسال با استفاده از متد POST و استفاده از APIKEY

</div>


```

curl --location -k --request POST 'http://sms.persiafava.com/webservice/rest/sms_send' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'api_key=2:628fa6a500d3b' \
--data-urlencode 'receiver_number=09132125459' \
--data-urlencode 'sender_number=3000569999' \
--data-urlencode 'note_arr[]=hi' \
--data-urlencode 'date=0' \
--data-urlencode 'request_uniqueid=0' \
--data-urlencode 'flash=no' \
--data-urlencode 'onlysend=no' \
--data-urlencode 'show_faktor=no'

```

<div dir="rtl">

نمونه کد نظیر به نظیر با استفاده از متد POST و استفاده از APIKEY
</div>


```

curl --location -k --request POST 'http://sms.persiafava.com/webservice/rest/sms_send' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'api_key=2:628fa6a500d3b' \
--data-urlencode 'sender_number=3000569999' \
--data-urlencode 'note_arr[]=hi' \
--data-urlencode 'receiver_number[]=091321254591' \
--data-urlencode 'note_arr[]=hi1' \
--data-urlencode 'receiver_number[]=091321254592' \
--data-urlencode 'note_arr[]=hi2' \
--data-urlencode 'receiver_number[]=091321254593' \
--data-urlencode 'note_arr[]=hi3' \
--data-urlencode 'date=0' \
--data-urlencode 'request_uniqueid=0' \
--data-urlencode 'flash=no' \
--data-urlencode 'onlysend=no' \
--data-urlencode 'show_faktor=no'

```


<div dir="rtl">

نمونه پاسخ دریافتی برای نظیر به نظیر
</div>

```
{"result":true,"list":["2_63295d1d86c63_0","2_63295d1d86c63_1","2_63295d1d86c63_2"]}
```


<div dir="rtl">

آدرس وب سرویس رست به صورت زیر میباشد :

</div>


http://sms.persiafava.com/webservice/rest/

<div dir="rtl">


در تمامی فانکشن ها میتوانید به جای login_username و login_password از api_key استفاده نمایید.
</div>

api_key را از 
https://sms.persiafava.com/fullmode/webservice_setting.html
 میتوانید بدست آورید.



 api_key برای همیشه ثابت است و فقط برای وب سرویس REST استفاده میشود




```
http://sms.persiafava.com/webservice/rest/sms_send?note_arr[]=سلام&api_key=API_KEY&receiver_number=09132125459&sender_number=3000569999

```


برای پاسخ تمامی متد ها result با ۲ مقدار true و false وجود دارند که مقدار false نشانه ی ناموفق بودن عملیات است.به طور مثال وقتی نام کاربری و رمز عبور اشتباه باشد چنین خطایی دریافت خواهید کرد.


{"result":false,"error":"error_login_user_not_found"}


### دریافت اطلاعات کاربری
از این متد برای دریافت اطلاعات کاربری و شماره های اختصاصی و میزان شارژ استفاده می شود.

نام متد:user_info
آدرس مورد استفاده :


http://sms.persiafava.com/webservice/rest/user_info?

<div dir="rtl">


پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|login_username|string|نام کاربری مورد استفاده در سامانه پیامک||
|login_password|string|رمز عبور مورد استفاده در سامانه پیامک||

</div>



مثال :

```
http://sms.persiafava.com/webservice/rest/user_info?login_username=USERNAME&login_password=PASSWORD
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/user_info?login_username=USERNAME&login_password=PASSWORD HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```

نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است


```
{"result":true,"list":{"username":"admin_USERNAME","fullname":"ارسال","email":"myemailt@yahoo.com","mobile":"09132125459","cash":"3212509","date":"1389\/5\/5 00:46","date_expire":"1394\/2\/24 00:00"},"number":{"result":true,"list_user":[{"number":"3000569999","order":"shop_serial,label_reply,tahlilgar,bime,mobile_control"},{"number":"3000569999","order":""}]}}
```
### ارسال پیامک
از این متد برای ارسال پیامک استفاده می شود.

نام متد:sms_send
آدرس مورد استفاده :
http://sms.persiafava.com/webservice/rest/sms_send?

<div dir="rtl">


پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|login_username|string|نام کاربری مورد استفاده در سامانه پیامک||
|login_password|string|رمز عبور مورد استفاده در سامانه پیامک||
|receiver_number|string|شماره دریافت کننده پیامک که شماره ها باعلامت کاما , از هم جدا شده باشند||
|clientids|ArrayOfString|شناسه پیامک برای دریافت دلیوری که میتوانید به صورت آرایه ارسال نمایید||
|sender_number|string|شماره ارسال کننده در سامانه پیامک||
|note_arr|string|متن پیامک ارسالی میتواند به صورت استرینگ ارسال شود||
|note_arr|ArrayOfString|متن پیامک ارسالی میتواند به صورت آرایه ارسال شود||
|date|string|تاریخ ارسال پیامک ( ارسال در آینده )|0=هم اکنون ارسال شود|
|request_uniqueid|string|جهت جلوگیری از ارسال پیامک تکراری از منبع کد , میتوانید این متغیر را با یک عدد یا متن منحصر به فرد مقداردهی کنید . در صورت ارسال درخواست تکراری در پاسخ این متد smsid های قبلی ارسال خواهند شد|0=نیازی به چک کردن ندارد|
|flash|string|آیا پیامک به صورت فلش ارسال شود یا خیر|ok , no|
|onlysend|string|جهت ارسال سریع بدون وقفه در زمان ارسال پیامک ( ارسال پیامک با تاخیر 30 ثانیه به مشترک انجام خواهد شد)|ok , no (ok==send delay)|
|show_faktor|string|عدم ارسال و فقط نمایش میزان هزینه|ok , no|
|tb_name_in_smsid|string|در صورت ارسال این پارامتر شناسه پیامک های شما حاوی اطلاعات بیشتری است و برای دریافت دلیوری باید از متد sms_deliver_tb_name_in_smsid استفاده نمایید|ok|


</div>



مثال :
```
http://sms.persiafava.com/webservice/rest/sms_send?note_arr[]=سلام&login_username=USERNAME&login_password=PASSWORD&receiver_number=09132125459&sender_number=3000569999
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/sms_send?note_arr=test&login_username=USERNAME&login_password=PASSWORD&receiver_number=09132125459&sender_number=3000569999 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```

نمونه پاسخ : در این پاسخ '788137_5fcc745d14604_0' شناسه ی پیامک در سیستم ما میباشد که برای دلیوری به آن احتیاج دارید
مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است
{"result":true,"list":['788137_5fcc745d14604_0']}

به تعداد گیرنده ها به شما شناسه ی پیامک داده خواهد شد که شناسه هابا علامت کاما , از هم جدا شده اند مانند :

{"result":true,"list":['788137_5fcc745d14604_0','788137_5fcc745d14604_1']}

مثال با api_key :

```
http://sms.persiafava.com/webservice/rest/sms_send?note_arr[]=سلام&api_key=API_KEY&receiver_number=09132125459&sender_number=3000569999
```

اتصال وب سرویس به سیستم حسابداری هلو
از این متد برای ارسال پیامک استفاده می شود.تمامی پارامتر ها به صورت POST برای آدرس ارسال میشود

![Image description]((https://sms.persiafava.com/webservice/api_files/holo_0.jpg))
![Image description](https://sms.persiafava.com/webservice/api_files/holo_1.jpg)
![Image description](https://sms.persiafava.com/webservice/api_files/hollo_4.jpg)
![Image description](https://sms.persiafava.com/webservice/api_files/hollo_2.jpg)
![Image description](https://sms.persiafava.com/webservice/api_files/hollo_5.jpg)
image 1 to 5

درگاه : sms.persiafava.com

لینک ارسال :
http://sms.persiafava.com/webservice/rest/sms_send?


نام کاربری : نام کاربری ورود به سامانه ارسال پیامک

رمز عبور : رمز عبور ورود به سامانه ارسال پیامک

فرستنده : خط اختصاصی سامانه ارسال پیام کوتاه خود

پس از واردنمودن اطلاعات بالا در قسمت تنظیمات مدیریتی، کامپیوتر متصل به اینترنت را انتخاب و تنظیمات را ذخیره نمایید.

پس از ایجاد درگاه ارسال پیامک sms.persiafava.com می بایست به قسمت تنظیمات پیشرفته در همان تنظیمات مدیریتی رفته و اطلاعات آن را تغییر دهید:

ء Username را به عبارت login_username تغییر دهید.

مقدار password را به مقدار login_password تغییر دهید.

عبارت مربوط به TO را به receiver_number به روز رسانی کنید.

مقدار from می بایست کاملا تغییر کرده و sender_number شود.

در انتها mesage را به note_arr تغییر دهید.

سپس تنظیمات را به روز رسانی نموده و در زمان ارسال پیامک درگاه sms.persiafava.com را انتخاب نمایید.

برای بررسی ارسال نیز به تنظیمات مدیریتی رفته و تقویم کاری را انتخاب نمایید.

ایجاد تقویم زده و تنظیم رخداد کاری را انتخاب کنید و در زمان ارسال درگاه را به صورت گفته شده قراردهید.

جهت بررسی گزارش های ارسال نیز به قسمت کاربران رفته و مدیریت دریافت پیامک کاربران را مشاهده نمایید.

### وضعیت پیامک

از این متد برای اطلاع از وضعیت پیامک های ارسال شده استفاده می شود.
متد sms_deliver_online نیز دقیقا مانند همین متد میباشد و تنها تفاوت آن این است که sms_deliver_online در همان لحظه از اپراتور نهایی ارسال کننده ی پیامک وضعیت پیامک شما را دریافت میکند اما sms_deliver وضعیت ها را هر ۳۰ دقیقه یک بار به روز رسانی میکند و در واقع نتایج بررسی های قبلی را به شما نمایش میدهد

نام متد:sms_deliver
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/sms_deliver?



<div dir="rtl">

پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|dargah|string|علامت درگاه ها که قبلا توضیح داده شده است|مانند 3000|
|smsid|ArrayOfString|شناسه های پیامک های ارسالی که میتوانید به صورت آرایه ارسال نمایید||
|archive_year|Int|برای جستجو در آرشیو سال ارسال پیامک مانند 1400 ارسال گردد||
|archive_month|Int|برای جستجو در آرشیو ماه ارسال پیامک مانند 3 ارسال گردد||

</div>

مثال :

```
http://sms.persiafava.com/webservice/rest/sms_deliver?smsid[]=92943981&smsid[]=92943982&dargah=3000
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/sms_deliver?smsid[]=92943981&smsid[]=92943982&dargah=3000 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : در این پاسخ 92943981 شناسه ی پیامک در سیستم ما میباشد که 5 برای دلیوری آن داده شده است
عدد ۵ به معنای بلک لیست میباشد
در صورتی که در جدول جاری جستجو میکردید و عدد -1 را به عنوان دلیوری دریافت کردید باید در آرشیو جستجو نمایید

{"result":true,"list":{"92943981":"5","92943982":"1"}}

### وضعیت پیامک
از این متد برای اطلاع از وضعیت پیامک های ارسال شده استفاده می شود.
متد sms_deliver_online نیز دقیقا مانند همین متد میباشد و تنها تفاوت آن این است که sms_deliver_online در همان لحظه از اپراتور نهایی ارسال کننده ی پیامک وضعیت پیامک شما را دریافت میکند اما sms_deliver وضعیت ها را هر ۳۰ دقیقه یک بار به روز رسانی میکند و در واقع نتایج بررسی های قبلی را به شما نمایش میدهد

نام متد:sms_deliver_tb_name_in_smsid
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/sms_deliver_tb_name_in_smsid?

<div dir="rtl">

پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|smsid|ArrayOfString|شناسه های پیامک های ارسالی که میتوانید به صورت آرایه ارسال نمایید||

</div>

```
http://sms.persiafava.com/webservice/rest/sms_rest_sms_deliver_tb_name_in_smsid?smsid[]=92943981&smsid[]=92943982
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/sms_rest_sms_deliver_tb_name_in_smsid?smsid[]=92943981&smsid[]=92943982 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : در این پاسخ 92943981 شناسه ی پیامک در سیستم ما میباشد که 5 برای دلیوری آن داده شده است
عدد ۵ به معنای بلک لیست میباشد.

در صورتی که در جدول جاری جستجو میکردید و عدد -1 را به عنوان دلیوری دریافت کردید باید در آرشیو جستجو نمایید.

{"result":true,"list":{"92943981":"5","92943982":"1"}}


curl --location -k --request POST 'http://crmsms.ariantel.ir/webservice/rest/sms_deliver_tb_name_in_smsid' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'smsid[]=999810@1401@10@27_293675_0@+989355090501' \
--data-urlencode 'smsid[]=999810@1401@10@27_293675_0@+989355090502' \
--data-urlencode 'smsid[]=999810@1401@10@27_293675_0@+989355090503'



ایجاد گروه جدید در دفترتلفن
از این متد برای ایجاد گروه جدید در دفترتلفن استفاده می شود.

نام متد:user_cat_add
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/user_cat_add?

<div dir="rtl">

پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|login_username|string|نام کاربری مورد استفاده در سامانه پیامک||
|login_password|string|رمز عبور مورد استفاده در سامانه پیامک||
|title|string|عنوان گروه||

</div>

مثال :

```
http://sms.persiafava.com/webservice/rest/user_cat_add?login_username=USERNAME&login_password=PASSWORD&title=دوستان
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/user_cat_add?login_username=USERNAME&login_password=PASSWORD&title=دوستان HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```

نمونه پاسخ : addedid شناسه ی گروه جدید ایجاد شده در سیستم ما میباشد.
مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است.

{"result":true,"addedid":"160335"}

نمونه پاسخ عملیات ناموفق :

{"result":false,"error":"error_complete_all"}


### دریافت گروه های دفترتلفن
از این متد برای دریافت لیست گروه های دفتر تلفن استفاده می شود.

نام متد:user_cat_list
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/user_cat_list?

<div dir="rtl">

پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|login_username|string|نام کاربری مورد استفاده در سامانه پیامک||
|login_password|string|رمز عبور مورد استفاده در سامانه پیامک||
|page_number|Int|شماره ی صفحه||
|perpage|Int|تعداد نمایش در نتایج|از 1 شروع می شود|

</div>

مثال :

```
http://sms.persiafava.com/webservice/rest/user_cat_list?login_username=USERNAME&login_password=PASSWORD&page_number=1&perpage=30
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/user_cat_list?login_username=USERNAME&login_password=PASSWORD&page_number=1&perpage=30 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```

نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

```
{"result":true,"list":[{"date":"1481012960","date_fa":"1395\/9\/16 11:59","id":"156487","number":"1942","title":"علیپور"},{"date":"1475328506","date_fa":"1395\/7\/10 16:58","id":"153034","number":"130","title":"مراتب 2"}]}
```

### مشخصات یک گروه از دفتر تلفن

از این متد برای دریافت مشخصات یک گروه از دفتر تلفن استفاده می شود.

نام متد:user_cat_info
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/user_cat_info?

<div dir="rtl">

پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|login_username|string|نام کاربری مورد استفاده در سامانه پیامک||
|login_password|string|رمز عبور مورد استفاده در سامانه پیامک||
|id|Int|شناسه ی گروه||


</div>


```
http://sms.persiafava.com/webservice/rest/user_cat_info?login_username=USERNAME&login_password=PASSWORD&id=156487
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/user_cat_info?login_username=USERNAME&login_password=PASSWORD&id=156487 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```

نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

{"result":true,"list":{"id":"156487","userid":"48","title":"علیپور","date":"1481012960","number":"1942","adminid":"1","receive_catid":"0","parentid":"0"}}

نمونه پاسخ عملیات ناموفق :

{"result":false,"error":"error_not_found"}

### اضافه کردن شماره ی جدید به دفترتلفن

از این متد برای اضافه کردن شماره ی جدید به دفترتلفن استفاده می شود.

نام متد:sms_number_add
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/sms_number_add?


مقادیر|توضیحات|نوع|پارامتر 
-| - | - | -
||نام کاربری مورد استفاده در سامانه پیامک|string|login_username
||رمز عبور مورد استفاده در سامانه پیامک|string|login_password
||شناسه ی گروه|Int|catid
||شماره موبایل|string|number
||اسم و فامیل|string|fullname
|1,2,3|چک شدند برای جلوگیری از ثبت تکراری 1- در صورتی ثبت شود که فقط در همین بخش این شماره قبلا ثبت نشده باشد 2- در صورتی ثبت شود که این شماره قبلا در هیچ بخشی ثبت نشده باشد 3- در همه ی شرایط ثبت شود|string|repeat
|1=مرد , 2=زن|جنسیت|string|gender
||اسم و فامیل لاتین|string|fullname_en
|1=مرد , 2=زن|جنسیت برای لاتین|string|gender_en
|true,false|چک شود درصورتی که در بلک لیست بود اضافه نشود در صورتی که مقدار "true" ارسال شود چک نمیشود پیش فرض false میباشد|string|blacklist_no_check
```
http://sms.persiafava.com/webservice/rest/sms_number_add?login_username=USERNAME&login_password=PASSWORD&catid=156487&repeat=3&number=09132125459&fullname=تست&gender=1&fullname_en=test&gender_en=1&blacklist_no_check=true
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/sms_number_add?login_username=USERNAME&login_password=PASSWORD&catid=156487&repeat=3&number=09132125459&fullname=تست&gender=1&fullname_en=test&gender_en=1&blacklist_no_check=true HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

{"result":true,"addedid":"35719269"}

نمونه پاسخ عملیات ناموفق :

{"result":false,"error":"شماره نامعتبر میباشد \n\t\t\t[کد۰]\n\t\t\t"}
{"result":false,"error":" شماره ی xxxxx قبلا در بخش های دیگر ثبت شده است"}
{"result":false,"error":"بخش انتخاب شده مربوط به شما نمیباشد."}

### دریافت شماره های دفترتلفن
از این متد برای دریافت لیست شماره های دفتر تلفن استفاده می شود.

نام متد:sms_number_list
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/sms_number_list?


<div dir="rtl">


پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|login_username|string|نام کاربری مورد استفاده در سامانه پیامک||
|login_password|string|رمز عبور مورد استفاده در سامانه پیامک||
|page_number|Int|شماره صفحه|از 1 شروع میشود|
|perpage|Int|تعداد نمایش در نتایج||
|catid|Int|شماره ی بخش دفتر تلفن|برای فیلتر کردن نتایح|
|fullname|string|اسم و فامیل فارسی|برای فیلتر کردن نتایح|
|number|Int|شماره تلفن|برای فیلتر کردن نتایح|


</div>


```
http://sms.persiafava.com/webservice/rest/sms_number_list?login_username=USERNAME&login_password=PASSWORD&page_number=1&perpage=30
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/sms_number_list?login_username=USERNAME&login_password=PASSWORD&page_number=1&perpage=30 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

```
{"result":true,"list":[{"id":"36819915","userid":"48","fullname":"09357746152","number":"+989357746152","date":"1501585658","catid":"147633","gender":"0","fullname_en":"","gender_en":"0","json_config":""},{"id":"36585956","userid":"48","fullname":"حسن خواجه","number":"+989389994672","date":"1499673540","catid":"147633","gender":"2","fullname_en":"khaje","gender_en":"2","json_config":""},{"id":"24888553","userid":"48","fullname":"+989360006291","number":"+989360006981","date":"1464249061","catid":"147633","gender":"0","fullname_en":"","gender_en":"0","json_config":""}],"count":0}
```
### به روز کردن تعداد شماره های گروه های دفترتلفن
از این متد برای به روز کردن تعداد شماره های گروه های دفتر تلفن استفاده می شود.

نام متد:sms_number_update
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/sms_number_update?


پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|catid|Int|شماره ی بخش دفتر تلفن||

```
http://sms.persiafava.com/webservice/rest/sms_number_update?catid=30
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/sms_number_update?catid=30 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

```
{"result":true,"list":"30","count":"69"}
```

### لیست پیامک های دریافتی

از این متد برای لیست پیامک های دریافتی استفاده می شود.

نام متد:sms_receive_list
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/sms_receive_list?


مقادیر|توضیحات|نوع|پارامتر 
-| - | - | -
||نام کاربری مورد استفاده در سامانه پیامک|string|login_username
||رمز عبور مورد استفاده در سامانه پیامک|string|login_password
|از 1 شروع میشود|شماره ی صفحه|Int|page_number
||تعداد نمایش در نتایج	|Int|perpage
|در صورتی که نیاز به فیلتر کردن بر اساس این پارامتر ندارید پارامتر را ارسال ننمایید|شماره گروه پیامکهای دریافتی|Int|catid
|1=خوانده شده ها, 0=خوانده نشده ها ,در صورتی که خالی ارسال شود تمامی پیام ها را میدهد|نوع خوانده شدن پیامک|Int|read
|درصورتی که بیشتر از 1 خط اختصاصی دارید ارسال نمایید. در غیر این صورت نیاز به ارسال این پارامتر نمیباشد.در صورت عدم ارسال این پارامتر پیام های دریافتی کلیه خطوط اختصاصی کاربر شما در نتایج ظاهر خواهند شد.|شماره دریافت کننده ی پیام|Int|number
|در صورتی که نیاز به فیلتر کردن بر اساس این پارامتر ندارید پارامتر را ارسال ننمایید.|شناسه ی کلمه ی کلیدی|Int|labelid
|در صورت قرار دادن این پارامتر تعداد نتایج در count به شما نمایش داده خواهد شد در صورتی که لیست پیام های دریافتی را نیاز دارید این پارامتر را ارسال ننمایید|فقط تعداد را نمایش بده.|Int|count
|در صورت قرار دادن این پارامتر پیامهای دارای id بزرگتر از این عدد به شما نمایش داده خواهد شد.|نمایش نتایج بزرگتر از این شناسه|Int|fromid

مثال :
```
http://sms.persiafava.com/webservice/rest/sms_receive_list?login_username=USERNAME&login_password=PASSWORD&page_number=1&perpage=30
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/sms_receive_list?login_username=USERNAME&login_password=PASSWORD&page_number=1&perpage=30 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

```
{"result":true,"list":[{"id":"1227955","sender_number":"09132125459","receiver_number":"3000569999","date":"1493483544","date_fa":"1396\/2\/9 21:02","catid":"0","read":"0","note":"خانم شیرانی"},{"id":"1227938","sender_number":"09300706012","receiver_number":"3000569999","date":"1493481719","date_fa":"1396\/2\/9 20:31","catid":"0","read":"0","note":"داداشی اینقد بچه کوچیک اونجا بود مشکل کند ذهنی و عقب افتادگی داشتن اصن ..."}]}
```

### تغییر وضعیت خواندن پیام های دریافتی

از این متد برای تغییر وضعیت خوانده شدن پیام های دریافتی استفاده می شود.

نام متد:sms_receive_change_read
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/sms_receive_change_read?

<div dir="rtl">

پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|login_username|string|نام کاربری مورد استفاده در سامانه پیامک||
|login_password|string|رمز عبور مورد استفاده در سامانه پیامک||
|id|ArrayOfString|شناسه ی پیامک ها به صورت آرایه||
|read|Int|وضعیت جدید||

</div>


```
http://sms.persiafava.com/webservice/rest/sms_receive_change_read?login_username=USERNAME&login_password=PASSWORD&read=1&id[]=156487
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/sms_receive_change_read?login_username=USERNAME&login_password=PASSWORD&read=1&id[]=156487 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

{"result":true,"list":{"id":"156487","userid":"48","title":"علیپور","date":"1481012960","number":"1942","adminid":"1","receive_catid":"0","parentid":"0"}}

نمونه پاسخ عملیات ناموفق :

{"result":false,"error":"error_not_found"}

### لیست کلمات کلیدی
از این متد برای دریافت لیست کلمات کلیدی مورد استفاده در منشی پیامک و مسابقه و نظرسنجی استفاده می شود.

نام متد:label_list
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/label_list?

مقادیر|توضیحات|نوع|پارامتر 
-| - | - | -
||نام کاربری مورد استفاده در سامانه پیامک|string|login_username
||رمز عبور مورد استفاده در سامانه پیامک|string|login_password
|از 1 شروع میشود|شماره ی صفحه|Int|page_number
||تعداد نمایش در نتایج	|Int|perpage
|0,1|وضعیت|Int|state
|پس از مثال جدول اعداد و مفاهیم قرار داده شده است|نوع کلمه ی کلیدی|Int|kind
|مثلا شناسه ی نظرسنجی اصلی ایجاد شده|شناسه ی رکورد مرتبط|Int|refferid
||شماره ی دریافت کننده|string|number

```
http://sms.persiafava.com/webservice/rest/label_list?login_username=USERNAME&login_password=PASSWORD&page_number=1&perpage=30
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/label_list?login_username=USERNAME&login_password=PASSWORD&page_number=1&perpage=30 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

```
{"result":true,"list":[{"id":"34860","label":"5","title":"تست","adminid":"1","userid":"48","kind":"3","refferid":"470","date":"1383648729","state":"0","number":"3000569999","date_start":"1383652260","date_end":"1383735060","repeat":"1","hit":"0","note":"تست","catid":"0","catid_delete":"0","date_fa":"1392\/8\/14 14:22"}],"count":1}
```
مفهوم label کلمه ی کلیدی مورد نظر میباشد
مفهوم count تعداد دفعات استفاده از این کلمه توسط کاربران میباشد
مفهوم kind موجود در پاسخ در جدول زیر آمده است

<div dir="rtl">


مفهوم|علامت اختصاص یافته|
-| - |
|منشی پیامک|1|
|نظرسنجی|2|
|مسابقه|3|
|پیشنهاد|4|

</div>



### ایجاد کلمات کلیدی
از این متد برای ایجاد کلمات کلیدی مورد استفاده در منشی پیامک و مسابقه و نظرسنجی استفاده می شود.

نام متد:label_new
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/label_new?


مقادیر|توضیحات|نوع|پارامتر 
-| - | - | -
||نام کاربری مورد استفاده در سامانه پیامک|string|login_username
||رمز عبور مورد استفاده در سامانه پیامک|string|login_password
|از|عنوان در نظر گرفته شده برای این کلمه ی کلیدی|string|title
||کلمه کلیدی مورد نظر|string|label
|0,1|متن پاسخ|String|note
|0=فقط ۱ پاسخ از کاربر دریافت شود|تعداد دریافت پاسخ از یک شماره|Int|repeat
|پس از مثال جدول اعداد و مفاهیم قرار داده شده است|نوع کلمه ی کلیدی|Int|kind
|مثلا شناسه ی نظرسنجی اصلی ایجاد شده|شناسه ی رکورد مرتبط|Int|refferid
||شماره ی دریافت کننده|string|number
|0=بدون محدودیت زمانی 1=در بازه زمانی مشخص شده فعال باشد|محدودیت زمانی|Int|time_limit	
||شروع محدودیت زمانی بر اساس unix timestamp	ء|BigInt|date_start	
||پایان محدودیت زمانی بر اساس unix timestamp	ء|BigInt|date_end	
||شماره رکورد گروه دفترتلفن برای ذخیره ی شماره در دفترچه تلفن|Int|catid	
||شماره رکورد گروه دفترتلفن برای حذف شماره از دفترچه تلفن|Int|catid_delete
|0=خیر (پیش فرض) , 1=بلی|ارسال متن پس از دریافت پیامک|Int|reply

مثال :

```
http://sms.persiafava.com/webservice/rest/label_new?note=ok&login_username=USERNAME&login_password=PASSWORD&title=test&label=1&reply=ok&kind=1&repeat=2&number=3000569999
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/label_new?note=ok&login_username=USERNAME&login_password=PASSWORD&title=test&label=1&reply=ok&kind=1&repeat=2&number=3000569999 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

```
{"result":true,"addedid":"32908"}
```

### ویرایش کلمات کلیدی
از این متد برای ویرایش کلمات کلیدی مورد استفاده در منشی پیامک و مسابقه و نظرسنجی استفاده می شود.

نام متد:label_edit
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/label_edit?


مقادیر|توضیحات|نوع|پارامتر 
-| - | - | -
||نام کاربری مورد استفاده در سامانه پیامک|string|login_username
||رمز عبور مورد استفاده در سامانه پیامک|string|login_password
||شناسه ی کلمه ی کلیدی ای که میخواهید آن را ویرایش کنید|Int|id
||عنوان در نظر گرفته شده برای این کلمه ی کلیدی|string|title
||کلمه کلیدی مورد نظر|string|label
|0,1|متن پاسخ|String|note
|0=فقط ۱ پاسخ از کاربر دریافت شود|تعداد دریافت پاسخ از یک شماره|Int|repeat
|پس از مثال جدول اعداد و مفاهیم قرار داده شده است|نوع کلمه ی کلیدی|Int|kind
|مثلا شناسه ی نظرسنجی اصلی ایجاد شده|شناسه ی رکورد مرتبط|Int|refferid
||شماره ی دریافت کننده|string|number
|0=بدون محدودیت زمانی 1=در بازه زمانی مشخص شده فعال باشد|محدودیت زمانی|Int|time_limit	
||شروع محدودیت زمانی بر اساس unix timestamp	ء|BigInt|date_start	
||پایان محدودیت زمانی بر اساس unix timestamp	ء|BigInt|date_end	
||شماره رکورد گروه دفترتلفن برای ذخیره ی شماره در دفترچه تلفن|Int|catid	
||شماره رکورد گروه دفترتلفن برای حذف شماره از دفترچه تلفن|Int|catid_delete
|0=خیر (پیش فرض) , 1=بلی|ارسال متن پس از دریافت پیامک|Int|reply

```
http://sms.persiafava.com/webservice/rest/label_edit?id=123¬e=ok&login_username=USERNAME&login_password=PASSWORD&title=test&label=1&reply=ok&repeat=2&number=3000569999
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/label_edit?note=ok&id=123&login_username=USERNAME&login_password=PASSWORD&title=test&label=1&reply=ok&repeat=2&number=3000569999 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

```
{"result":true}
```

### حذف کلمه ی کلیدی

از این متد برای حذف کلمه ی کلیدی استفاده می شود.

نام متد:label_remove
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/label_remove?

<div dir="rtl">


پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|login_username|string|نام کاربری مورد استفاده در سامانه پیامک||
|login_password|string|رمز عبور مورد استفاده در سامانه پیامک||
|id|Int|شناسه ی کلمه ی کلیدی||

</div>

مثال :

```
http://sms.persiafava.com/webservice/rest/label_remove?login_username=USERNAME&login_password=PASSWORD&id=156487
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/label_remove?login_username=USERNAME&login_password=PASSWORD&id=156487 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

{"result":true}

نمونه پاسخ عملیات ناموفق :

{"result":false,"error":"error_not_found"}

### لینک ورود یک بار مصرف

از این متد برای ایجاد لینک ورود مدت دارد یک بار مصرف استفاده می شود.

نام متد:user_once_login
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/user_once_login?


مقادیر|توضیحات|نوع|پارامتر 
-| - | - | -
||نام کاربری مورد استفاده در سامانه پیامک|string|login_username
||رمز عبور مورد استفاده در سامانه پیامک|string|login_password
|مقدار پیش فرض 1 میباشد بدین معنا که لینک تولید شده فقط تا ۲۴ ساعت بعد امکان استفاده دارد|تعداد روز معتبر بودن لینک|Int|expire

مثال :

```
http://sms.persiafava.com/webservice/rest/user_once_login?login_username=USERNAME&login_password=PASSWORD&expire=2
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/user_once_login?login_username=USERNAME&login_password=PASSWORD&expire=2 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

```
{"result":true,"url":"http:\/\/sms123.ir\/user_once_login.php?id=2&md5=XXXXXXX&token=XXXXXXXXXXXXXXXXX"}
```

### اسامی مورد استفاده برای ارسال های شهری و منطقه ای

از این متد برای دریافت اسامی شهرهای و مناطق کدپستی برای ارسال های منطقه ای استفاده می شود.

نام متد:sms_bank_list
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/sms_bank_list?


مقادیر|توضیحات|نوع|پارامتر 
-| - | - | -
|postal_code = برای اسامی کدپستی همراه اول ,etebari = شماره های اعتباری همراه اول ,daemi = شماره های دایمی همراه اول|نوع بانک درخواستی	|string|bank_type
|در صورتی که bank_type=etebari یا bank_type=daemi باشد|شماره رکورد استان , برای دریافت لیست شهر های یک استان|Int|OstnCode

مثال :

```
http://sms.persiafava.com/webservice/rest/sms_bank_list?bank_type=postal_code
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/sms_bank_list?bank_type=postal_code HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

```
{"result":true,"bank":{"tehran":"تهران","karaj":"کرج","esfahan":"اصفهان","mashhad":"مشهد","khorasan":"خراسان","shiraz":"شیراز","kordestan":"کردستان","gilan":"گیلان","ardebil":"اردبیل","tabriz":"تبریز","tabriz_2":"تبریز جدید","yazd_abarkoh":"یزد-ابرکوه","yazd_ardakan":"یزد-اردکان","yazd_bafgh":"یزد-بافق","yazd_mehriz":"یزد-مهریز","yazd_meybod":"یزد-میبد","yazd_taft":"یزد-تفت","yazd_yazd":"یزد-یزد","shahrekord":"شهرکرد","bandarabas":"بندرعباس","khoramabad":"خرم آباد","ahvaz":"اهواز","kerman":"کرمان","kermanshah":"کرمانشاه","zanjan":"زنجان","orumie":"ارومیه","ghom":"قم","hamedan":"همدان"}}
```
مثال برای دریافت لیست استان ها :
```
http://sms.persiafava.com/webservice/rest/sms_bank_list?bank_type=daemi
```
مثال برای دریافت لیست شهر های استان اصفهان :

```
http://sms.persiafava.com/webservice/rest/sms_bank_list?bank_type=daemi&OstnCode=30
```
### اسامی مورد استفاده برای ارسال های شهری و منطقه ای

از این متد برای دریافت اسامی شهرهای و مناطق کدپستی برای ارسال های منطقه ای استفاده می شود.

نام متد:sms_bank_count
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/sms_bank_count?

<div dir="rtl">


پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|bank_type|string|نوع بانک درخواستی|postal_code = برای اسامی کدپستی|
|postalcode_city|string|اسم لاتین شهر درخواستی| در صورتی که bank_type=postal_code باشد |
|postalcode|Int|کدپستی مورد نظر|در صورتی که bank_type=postal_code باشد|

</div>

مثال :

```
http://sms.persiafava.com/webservice/rest/sms_bank_count?bank_type=postal_code&postalcode_city=esfahan&postalcode=81556
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/sms_bank_count?bank_type=postal_code&postalcode_city=esfahan&postalcode=81556 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```
نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است
number نشاندهنده تعداد شماره های موجود میباشد

```
{"result":true,"bank_type":"postal_code","number":"4888"}
```
### ارسال های شهری و منطقه ای
از این متد برای ارسال های منطقه ای استفاده می شود.

نام متد:sms_bank_send
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/rest/sms_bank_send?


مقادیر|توضیحات|نوع|پارامتر 
-| - | - | -
||نام کاربری مورد استفاده در سامانه پیامک|string|login_username
||رمز عبور مورد استفاده در سامانه پیامک|string|login_password
|postal_code = برای اسامی کدپستی همراه اول ,etebari = شماره های اعتباری همراه اول ,daemi = شماره های دایمی همراه اول|نوع بانک درخواستی	|string|bank_type
|در صورتی که bank_type=postal_code باشد|اسم لاتین شهر درخواستی|string|postalcode_city
|در صورتی که bank_type=postal_code باشد|کدپستی مورد نظر|Int|postalcode
|در صورتی که bank_type=etebari یا bank_type=daemi باشد|شماره رکورد استان|Int|OstnCode
|در صورتی که bank_type=etebari یا bank_type=daemi باشد|شماره رکورد شهر|Int|CityCode
||شروع تعداد از این رکورد|Int|record_start
||تعداد کل گیرنده ها|Int|receiver_count
||شماره ی ارسال کننده|Int|sender_number
||متن پیامک|string|note

مثال :
```
http://sms.persiafava.com/webservice/rest/sms_bank_send?note=چجپ&bank_type=etebari&OstnCode=1&CityCode=102&record_start=3&receiver_count=1&sender_number=3000569999
```
```
*   Trying 192.168.1.102...
* Connected to sms.persiafava.com (192.168.1.102) port 80 (#0)
> GET /webservice/rest/sms_bank_send?note=چجپ&bank_type=etebari&OstnCode=1&CityCode=102&record_start=3&receiver_count=1&sender_number=3000569999 HTTP/1.1
Host: sms.persiafava.com
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Server: Apache/2
< Connection: close
```

نمونه پاسخ : مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است
smsid شناسه ی پیامک های ارسال شده میباشد

```
{"result":true,"bank_type":"etebari","smsid":[9719137]}
```

### ارسال پیامک
از این متد برای ارسال پیامک استفاده می شود.تمامی پارامتر ها به صورت GET برای آدرس ارسال میشود

نام متد:send_sms
آدرس مورد استفاده :

http://sms.persiafava.com/send_via_get/send_sms.php?

مقادیر|توضیحات|نوع|پارامتر 
-| - | - | -
||نام کاربری مورد استفاده در سامانه پیامک|string|username
||رمز عبور مورد استفاده در سامانه پیامک|string|password
||شماره دریافت کننده پیامک که شماره ها باعلامت کاما , از هم جدا شده باشند|string|receiver_number
||شماره ارسال کننده در سامانه پیامک|string|sender_number
||متن پیامک ارسالی میتواند به صورت استرینگ ارسال شود|string|note
|0=نیازی به چک کردن ندارد|جهت جلوگیری از ارسال پیامک تکراری از منبع کد , میتوانید این متغیر را با یک عدد یا متن منحصر به فرد مقداردهی کنید . در صورت ارسال درخواست تکراری در پاسخ این متد smsid های قبلی ارسال خواهند شد|string|request_uniqueid
|ok , no|آیا پیامک به صورت فلش ارسال شود یا خیر|string|ersal_flash
|ok , no|	جهت ارسال سریع بدون وقفه در زمان ارسال پیامک ( ارسال پیامک با تاخیر 30 ثانیه به مشترک انجام خواهد شد)|string|onlysend

مثال :
```
http://sms.persiafava.com/send_via_get/send_sms.php?note=سلام&username=USERNAME&password=PASSWORD&receiver_number=09132125459&sender_number=3000569999
```

نمونه پاسخ : در این پاسخ 92943923 شناسه ی پیامک در سیستم ما میباشد که برای دلیوری به آن احتیاج دارید
مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

92943923

به تعداد گیرنده ها به شما شناسه ی پیامک داده خواهد شد که شناسه هابا علامت کاما , از هم جدا شده اند مانند :

92943981,92943982

### دریافت وضعیت پیامک

از این متد برای ارسال پیامک استفاده می شود.تمامی پارامتر ها به صورت GET برای آدرس ارسال میشود

نام متد:sms_deliver
آدرس مورد استفاده :

http://sms.persiafava.com/send_via_get/send_sms.php?

<div dir="rtl">

پارامتر|نوع|توضیحات|مقادیر
-| - | - | -
|dargah|string|علامت درگاه ها که قبلا توضیح داده شده است|مانند 3000|
|smsid|ArrayOfString|شناسه های پیامک های ارسالی که میتوانید به صورت آرایه ارسال نمایید||

</div>


```
http://sms.persiafava.com/send_via_get/send_sms.php?smsid[]=92943981&smsid[]=92943982&dargah=3000
```

نمونه پاسخ : در این پاسخ 92943981 شناسه ی پیامک در سیستم ما میباشد که 5 برای دلیوری آن داده شده است
عدد ۵ به معنای بلک لیست میباشد
Array ( [0] => 5 [1] => 1 )

### نمونه کدها با زبان های برنامه نویسی مختلف

در تمامی نمونه کد های قرار گرفته اطلاعات زیر به صورت پیش فرض قرار گرفته که برای استفاده باید آنها را تغییر دهید :

دامین سرویس دهنده : sms321.ir ( این دامین را با دامین سایتی که پنل ارسال پیامک را از آن تهیه کرده اید در کد ها جایگزین کنید )

نام کاربری : USERNAME

رمز عبور : PASSWORD

شماره ی ارسال کننده : 3000569999

شماره ی دریافت کننده : 09132125459

متن ارسال : سلام

### وب سرویس به زبان PHP

```
https://sms.persiafava.com/webservice/theme/file/php.txt
https://sms.persiafava.com/webservice/theme/file/php.zip

### کامند لاین لینوکس

https://sms.persiafava.com/webservice/theme/file/linux.txt

### اندروید

https://sms.persiafava.com/webservice/theme/file/android.txt

### وب سرویس به زبان C#

https://sms.persiafava.com/webservice/theme/file/csharp.txt

### وب سرویس به زبان Asp.net

https://sms.persiafava.com/webservice/theme/file/asp.txt

### وب سرویس به زبان دلفی

https://sms.persiafava.com/webservice/theme/file/delphi.txt

### وب سرویس به زبان جاوا

https://sms.persiafava.com/webservice/theme/file/java.txt

### ارسال پیامک از اکسس

https://sms.persiafava.com/webservice/theme/file/access.txt

### ارسال پیامک از پایتون

https://sms.persiafava.com/webservice/theme/file/python.txt

### ارسال پیامک در postman

https://sms.persiafava.com/webservice/theme/file/sms.postman_collection.json
https://sms.persiafava.com/webservice/theme/file/postman.mp4
```

### ارسال پیام صوتی

از این متد برای ارسال پیام صوتی استفاده می شود.

نام متد:send
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/vms/api.php


مقادیر|توضیحات|نوع|پارامتر 
-| - | - | -
||نام کاربری مورد استفاده در سامانه پیامک|string|login_username
||رمز عبور مورد استفاده در سامانه پیامک|string|login_password
|send|برای ارسال پیام صوتی مقدار send را وارد نمایید|string|api
||شماره دریافت کننده پیامک که شماره ها باعلامت کاما , از هم جدا شده باشند|string|receiver_number
|0=نیازی به چک کردن ندارد|جهت جلوگیری از ارسال پیام تکراری از منبع کد , میتوانید این متغیر را با یک عدد یا متن منحصر به فرد مقداردهی کنید . در صورت ارسال درخواست تکراری در پاسخ این متد smsid های قبلی ارسال خواهند شد|string|uniqid
|yek|کانال ارسال پیام صوتی در حال حاضر مقدار yek مورد قبول است|string|kind
||توضیحات برای درج در امور مالی	|string|billing_note
||فايل ارسالي انكود شده بصورت multipart/form-data	ء|File|fileToUpload

نمونه کد PHP :

```
<?
$file_name_with_full_path = realpath('test.wav'); //مسیر فایل صوتی
$post = array('login_username' => 'payamak21',//نام کاربری
    'login_password' => 'password',//رمز عبور
    'api' => 'send',//متد ارسال پیام
    'uniqid' => '',
    'kind' => 'yek',//کانال ارسال 
    'receiver_number' => '09132125459,03132382731', //شماره ها را با کاما میتوانید جدا کنید
    'billing_note' => 'test',//توضیحات برای خودتان
    'fileToUpload'=> curl_file_create($file_name_with_full_path));
$ch = curl_init();
curl_setopt($ch, CURLOPT_URL,'http://sms.persiafava.com/webservice/vms/api.php');
curl_setopt($ch, CURLOPT_POSTFIELDS, $post);
curl_setopt($ch, CURLOPT_RETURNTRANSFER,1);
$result=curl_exec ($ch);
curl_close ($ch);
print_r( json_decode( $result )); 
?>
```

نمونه پاسخ : در این پاسخ 4 شناسه ی پیام صوتی در سیستم ما میباشد که برای دلیوری به آن احتیاج دارید
مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

{"result":true,"list":"4"}

### احراز هویت صوتی

از این متد برای احراز هویت از طریق تماس صوتی استفاده می شود.

نام متد:otp
آدرس مورد استفاده :

http://sms.persiafava.com/webservice/vms/api.php


مقادیر|توضیحات|نوع|پارامتر 
-| - | - | -
||نام کاربری مورد استفاده در سامانه پیامک|string|login_username
||رمز عبور مورد استفاده در سامانه پیامک|string|login_password
|otp|برای احراز هویت صوتی مقدار otp را وارد نمایید|string|api
||شماره دریافت کننده|string|receiver_number
|0=نیازی به چک کردن ندارد|جهت جلوگیری از ارسال پیام تکراری از منبع کد , میتوانید این متغیر را با یک عدد یا متن منحصر به فرد مقداردهی کنید . در صورت ارسال درخواست تکراری در پاسخ این متد smsid های قبلی ارسال خواهند شد|string|uniqid
|yek|کانال ارسال پیام صوتی در حال حاضر مقدار yek مورد قبول است|string|kind
||توضیحات برای درج در امور مالی|string|billing_note
||کدی که برای کاربر به صورت صوتی پخش میشود|Int|otp_code


نمونه کد PHP :

```
<?
$post = array('login_username' => 'payamak21',//نام کاربری
    'login_password' => 'password',//رمز عبور
    'api' => 'otp',//متد ارسال احراز هویت صوتی
    'clientid' => '',
    'kind' => 'yek',//کانال ارسال
    'receiver_number' => '09132125459', //شماره ها
    'billing_note' => 'test',//توضیحات برای خودتان
    'otp_code'=> 123456);
$ch = curl_init();
curl_setopt($ch, CURLOPT_URL,'http://sms.persiafava.com/webservice/vms/api.php');
curl_setopt($ch, CURLOPT_POSTFIELDS, $post);
curl_setopt($ch, CURLOPT_RETURNTRANSFER,1);
$result=curl_exec ($ch);
curl_close ($ch);
print_r( json_decode( $result ));
?>
```

نمونه پاسخ : در این پاسخ 4 شناسه ی احراز هویت صوتی در سیستم ما میباشد که برای دلیوری به آن احتیاج دارید
مقدار result برابر true میباشد که نشاندهنده ی موفق بودن عملیات است

{"result":true,"list":"4"}

