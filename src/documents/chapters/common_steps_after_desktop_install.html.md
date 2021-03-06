---
layout: article
chapter: لینوکس روزمره 
order: 16
title: قدم های مرسوم بعد از نصب لینوکس دسکتاپ
---


گاهی ممکن است یک سایت یا سند یا حتی برنامه به اجبار سعی در استفاده از یک فونت خاص داشته باشد. مثلا به این اسکرین شات نگاه کنید:

<img src=/images/sina_blog.png>

تیتر صفحه با صفحه کلید عربی (احتمالا در ویندوز) تایپ شده که به جای «ک» از «ك» و به جای «ی» از «ي» استفاده می‌کند. همچنین طراح به اجبار به صفحه گفته از فونت Tahoma استفاده کند که یک فونت ویندوزی است. برای درست دیدن این صفحه در مرحله اول باید از طراح و نویسنده خواست که از استانداردهای فارسی استفاده کنند و در مرحله دوم،‌ برای حل موقتی مشکل (در اصل برای اضافه کردن امکان نمایش فارسی حروف عربی) باید فونت‌های استاندارد ویندوز را به سیستم اضافه کرد.

در اوبونتو بسته‌ای به نام ubuntu-restricted-extras که مجموعه ای است از ابزارهایی که به علت مجوزهای محدود کننده‌ای که شرکت‌های سازنده روی آن ها گذشته‌اند نمی‌توانند روی سی دی اصلی اوبونتو عرضه شوند. بگذارید نگاهی به محتویات آن بیندازیم:

jadi@jubung:~$ aptitude show ubuntu-restricted-extras 
Package: ubuntu-restricted-extras        
New: yes
State: installed
Automatically installed: no
Version: 57
Priority: optional
Section: multiverse/metapackages
Maintainer: Michael Vogt <michael.vogt@ubuntu.com>
Architecture: amd64
Uncompressed Size: 30.7 k
Depends: ubuntu-restricted-addons
Recommends: ttf-mscorefonts-installer, unrar, gstreamer0.10-plugins-bad-multiverse, libavcodec-extra-53
Conflicts: ubuntu-restricted-extras
Description: Commonly used restricted packages for Ubuntu
 This package depends on some commonly used packages in the Ubuntu multiverse repository. 
 
 Installing this package will pull in support for MP3 playback and decoding, support for various other audio formats (GStreamer plugins), Microsoft fonts, Flash plugin,
 LAME (to create compressed audio files), and DVD playback. 
 
 Please note that this does not install libdvdcss2, and will not let you play encrypted DVDs. For more information, see
 https://help.ubuntu.com/community/RestrictedFormats/PlayingDVDs 
 
 Please also note that packages from multiverse are restricted by copyright or legal issues in some countries. See http://www.ubuntu.com/ubuntu/licensing for more
 information.
آنطور که این دستور می‌گوید، این بسته حاوی پشتیبانی از فرمت mp3 و فرمت‌های صوتی تصویری دیگر، پشتیبانی از فونت‌های مایکروسافت، فلش و پخش دی وی دی است. پس احتمالا با نصب آن، مشکل ما حل خواهد شد.

sudo apt-get install ubuntu-restricted-extras
به عنوان یک نکته اضافی ، خوب است بدانیم که هر کاربر گنو/لینوکس می‌تواند با ساخت پوشه‌ای به اسم fonts. در خانه خودش ( home folder ) و کپی کردن هر فونتی که لازم دارد درون آن و خروج و ورود مجدد به سیستم، به آن فونت‌ها دسترسی داشته باشد. مثلا کپی کردن فایل tahoma.ttf و tahomab.ttf می تواند مشکل وب سایت بالا و بقیه سایت‌هایی که از فونت تاهوما استفاده می‌کنند را حل کند.

**توجه: ** هر فایل که در گنو/لینوکس و سیستم‌های یونیکسی که با نقطه شروع شود،‌ در حالت عادی مخفی است و به کاربر نمایش داده نمی شود. در براوزر فایل گنوم (ناتیلوس) می‌توانید با فشردن Ctrl+H فایل‌های مخفی را ببینید.
