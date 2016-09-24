---
layout: post
title:  "Инсталиране на Google Calendar indicator в Ubuntu 14.04"
date:   2014-10-16 11:39:31
comments : true
categories: linux
banner_image: calendar/calendar.png
---

Една добра новина за тези които използват Google Calendar и Ubuntu.
Вече има програма, която е и индикатор и клиент за услугата Google Calendar. Програмата поддържа доста опции измежду които са :

1. Синхронизация с Google Calendar(най-важното). Като вие избирате през колко време да се синхронизира.

2. Позволява да добавяте и редактирате записи които също се синхронизират с гугълския календар.

3. Позволява нотификации на работния плот. Подсеща ви с pop-up съобщения като наближи време за определено събитие в календара.


За съжаление все още има доста бъгове. Например при мен понякога се случва да крашне преди нотификация. Но като се има предвид че доста хора го използват се надявам че скоро бъговете ще бъдат отстранени.

При Ubuntu и деривативите му може да се инсталира чрез PPA:


**sudo add-apt-repository ppa:atareao/atareao**

**sudo apt-get update**

**sudo apt-get install calendar-indicator**


Ето малко снимки на самата програма:

![cl1](https://github.com/etem/etem.github.io/raw/master/assets/images/calendar/1.png)
![cl2](https://github.com/etem/etem.github.io/raw/master/assets/images/calendar/2.png)


Източник :
[WebUpd8](http://www.webupd8.org/2013/11/google-calendar-indicator-020-released.html)

{% include disqus.html %}
