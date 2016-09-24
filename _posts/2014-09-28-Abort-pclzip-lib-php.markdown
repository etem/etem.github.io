---
layout: post
title:  "Abort pclzip.lib.php : Missing zlib extensions"
date:   2014-09-08 11:39:31
comments : true
categories: other
banner_image: php/php.png
---

Твърде вероятно е да видите горното съобщение за грешка, ако използвате Apache2 с някоя CMS система като е107, или Wordpress, и използвате версия 5.5.9 на PHP.
Появява се най-вече като ъплоудвате теми или плъгини, които са .zip архив и трябва да се разархивират след ъплоуда. Проблемът е бъг във версия 5.5.9 на PHP. Решението е просто:

Първоначално се уверете че имате Zlib подръжка като извикате phpinfo.php. Доколкото знам тя е разрешена по подразбиране при повечето случаи.
Ако използвате Ubuntu 14.04 Server може да обновите PHP-то много лесно чрез PPA:

**sudo add-apt-repository ppa:ondrej/php5**

**sudo apt-get update**

**sudo apt-get upgrade**

**sudo apt-get install php5**


След изпълнение на горните команди и рестарт на сървъра ще свършат главоболията със zlib екстеншъна на PHP :)

{% include disqus.html %}
