---
layout: post
title:  "Как да проверим коя версия на SATA поддържа компютъра"
date:   2015-06-06 13:10:31
comments : true
categories: linux
banner_image: satalogo.png
---


Най-честата причина за проверка на SATA версията е преди да закупим нов хард или SSD диск. Различните версии на SATA са с различни скорости, така че ако компютърът ви поддържа стара версия няма да може да се възползвате напълно от  възможностите на най-новите SSD дискове.

Например ако компютърът ви поддържа версия SATA 2 3Gb/s и му инсталирате SSD със SATA 3 6Gb/s, то той все пак ще работи, но на по-ниската скорост.

За да проверите версията на SATA при Debian,Ubuntu и техните деривативи, трябва да имате инсталиран пакета **smartmontools**.
След като го инсталирате изпълнете : 

**sudo smartctl -a /dev/sda &#124; grep "SATA"** 

/*Не го копирайте директно - няма да върне нищо*/


Ще ви изпише съобщение подобно на това :

`SATA Version is:  SATA 2.6, 3.0 Gb/s`



{% include disqus.html %}
