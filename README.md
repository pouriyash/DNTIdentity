﻿<div dir="rtl">


سفارشی سازی ASP.NET Core Identity 1.1 
=======



![dnt-identity-02](/src/ASPNETCoreIdentitySample/wwwroot/images/dnti02.png)



![dnt-identity-01](/src/ASPNETCoreIdentitySample/wwwroot/images/dnti01.png)



دارای قسمت‌های 
------
ثبت نام به همراه تائید ایمیل، لاگین، برگه‌ی اطلاعات کاربری، تنظیمات کاربری، تغییر کلمه‌ی عبور، بازیابی کلمه‌ی عبور، اعتبارسنجی دو مرحله‌ای توسط ایمیل، مدیریت کاربران و نقش‌های ثابت. مدیریت سطوح دسترسی پویای به صفحات و مشاهده‌ی لاگ خطاهای برنامه.



با امکانات
----------
* اضافه کردن Remote validationها به قسمت‌های ثبت نام، تغییر کلمه‌ی عبور، بازیابی کلمه‌ی عبور و تنظیمات کاربری
* پیاده سازی امکان ویرایش تنظیمات کاربری به همراه آپلود تصویر شخص و فیلدهای سفارشی مانند تاریخ تولد، مکان و امثال آن 
* پیاده سازی کامل قسمت‌های ارسال ایمیل و همچنین پشتیبانی از تهیه‌ی قالب‌های ایمیل توسط Razor Views
* پیاده سازی مدیریت نقش‌های ثابت سیستم
* پیاده سازی جزئیات مدیریت کاربران به همراه جستجوی آن‌ها
* پیاده سازی سطوح دسترسی پویای به صفحات مختلف سایت به کمک ویژگی جدید پالیسی در ASP.NET Core
* پیاده سازی مفهوم Security Trimming جهت عدم نمایش لینک‌هایی که کاربر جاری به آن‌ها دسترسی پویا ندارد
* پیاده سازی ویجت کاربران آنلاین
* پیاده سازی ویجت تولدهای امروز با سفارشی سازی موجودیت و همچنین سرویس مدیریت کاربران سایت



سفارشی سازی تنظیمات کلاینت
--------
* استفاده از بوت استرپ 3 راست به چپ
* استفاده از قلم فارسی مناسب
* تنظیم Unobtrusive jQuery Ajax & Validation
* تنظیم Bundling & minification اسکریپت‌ها و شیوه‌نامه‌ها



سفارشی سازی لایه‌های برنامه
------
* جدا سازی کامل لایه‌ها به همراه تزریق وابستگی‌ها و پیاده سازی الگوی واحد کار
* انتقال تمام مباحث مدیریت کاربران به یک Area جدید به نام Identity جهت سهولت استفاده‌ی از آن در سایر برنامه‌ها



سفارشی سازی لایه‌ها‌ی دسترسی به داده‌ها و موجودیت‌ها
--------
* سفارشی سازی موجودیت‌های Identity جهت افزودن خواصی بیشتر و همچنین تغییر نوع کلید اصلی جداول به int
* DbContext مورد استفاده، به لایه‌ی مخصوص خود انتقال یافته و همچنین تنظیمات Migrations نیز از برنامه‌ی اصلی وب خارج و به این لایه منتقل شده‌اند.
* سفارشی سازی کامل DbContext برنامه جهت افزودن امکان استفاده‌ی از بانک‌های اطلاعاتی مختلف، سفارشی سازی نام جداول Identity، افزودن Shadow properties ویژه‌ی ثبت جزئیات کاربر ثبت کننده و ویرایش کننده‌ی رکوردها، به همراه IP‌ و زمان تغییرات.
* یک دست سازی ی و ک ثبت شده‌ی توسط EF Core با سفارشی سازی Change Tracker آن 



سفارشی سازی لایه‌ی سرویس‌های Identity
--------
* پیاده سازی متد Seed جهت افزودن کاربر ادمین و همچنین نقش آن به سیستم در اولین بار اجرای برنامه
* سفارشی سازی تمام سرویس‌های توکار Identity مانند مدیریت کاربران و نقش‌ها
* سفارشی سازی مدیریت Claims جهت افزودن مسیر تصویر شخص جهت کاهش رفت و برگشت به بانک اطلاعاتی
* سفارشی سازی نرمال ساز ایمیل‌ها و همچنین نام کاربری جهت اعمال یک دست سازی به ایمیل‌هایی یکسان با چند نوع قابل قبول مانند ایمیل‌های جی‌میل
* پیاده سازی یک Ticket Store مبتنی بر بانک اطلاعاتی جهت کاهش اندازه‌ی کوکی‌های حاصل از تعریف سطوح دسترسی پویای به صفحات مختلف برنامه
* سفارشی سازی اعتبارسنجی کلمات عبور برنامه جهت عدم قبول مواردی ساده و یا قابل حدس
* تدارک یک لاگر پیاده سازی شده‌ی با EF Core جهت ثبت خطاهای برنامه به همراه صفحه‌ای مدیریتی مخصوص جهت مشاهده‌ی این خطاها
* پیاده سازی سرویس ذخیره سازی سابقه‌ی کلمات عبور کاربران و ارائه‌ی اخطارهای لازم به آن‌ها
* سفارشی سازی طول عمر توکن صادر شده‌ی جهت تائید ایمیل شخص در حین ثبت نام که به صورت پیش فرض تنها یک روز است
* انتقال تمام تنظیمات Identity و برنامه به یک فایل json، جهت سهولت تغییر آن‌ها بدون نیازی به تغییری در برنامه
* تهیه‌ی یک رجیستری جهت سهولت افزودن تمام تنظیمات تزریق وابستگی‌های سفارشی سازی شده‌ی برنامه توسط یک متد در کلاس آغازین آن



بومی سازی
-------
* فارسی بودن تمام قسمت‌های برنامه به همراه کلیه‌ی خطاها و اخطارهای توکار Identity



آزمون‌های واحد
------
* تهیه و تنظیم کامل زیر ساخت نوشتن آزمون‌های واحد درون حافظه‌ای EF Core به کمک فریم ورک MS Test



------------------------------------------------------------------------------------------------------


جزئیات و توضیحات بیشتر این موارد را می‌توانید در گروه [ASP.NET Core Identity](http://www.dotnettips.info/search/label/asp.net%20core%20identity) پیگیری نمائید.


</div>