---
layout: post
title:  "Конфигуриране на хибридна графика при Ubuntu 14.04.Nvidia Prime."
date:   2014-11-20 12:39:31
comments : true
categories: linux
banner_image: nvidia/cover.png
---

Ако използвате лаптоп с хибридна графика(вградена и дискретна видеокарта) в комбинация с Ubuntu 14.04 или някой негов дериватив, то тогава тази статия е за вас.


Та какво представлява Nvidia Optimus технологията? Както се подразбира това е технология на изобретена от Nvidia, която се използва главно в лаптопи и ноутбуци.
Целта и е да превключва между две видеокарти в една система, според изискванията на ресурси на приложението което ще се изпълнява.


За пример мога да дам моята конфугирация на Acer Aspire 5742zg. Лаптопът идва с две видеокарти, едната вградена в процесора Intel P6200, която изисква малко енергия и съответно е по-слаба, а другата Nvidia Geforce 610M, която е много по-мощна и съответно изисква повече енергия. Какво става на практика когато използвате лаптопа?
Когато стартирате игра или приложение, което не изисква много ресурси от страна на видеокартата, например някоя по-малка игра, то тя се изпълнява от вградената видеокарта.
При изпълняване на приложение или игра, която изисква много голяма изчислителна мощност от страна на видеото, то тогава тя се превключва за изпълнение от по-мощната видеокарта, без това да се усеща от потребителя.

Както се досещате цялото това нещо е направено със замисъла да се пести енергия. Особено при преносимите компютъри където това е от голямо значение.

<span style="color: red">Важно! За разлика от Windows, при Линукс дистрибуциите драйверите все още не са перфектни и превключването на видеокартите не се случва автоматично.
Също така след като превключите трябва да се излезете (Log out) и пак да влезете в системата за да има ефект.</span>

Софтуерът при Ubuntu и другите Линукс дистрибуции, който позволява да се случва превключването е Nvidia Prime. За да работи обаче са нужни няколко условия:

1.Трябва да изберете драйвера на Nvidia от менюто Additional Drivers, няма да работи ако сте избрали Nouveau драйвера.

![nvidia1](https://github.com/etem/etem.github.io/raw/master/assets/images/nvidia/nvidia1.png)


2.Ако по някаква случайност сте инсталирали пакета bumblebee трябва да го премахнете :

**sudo apt-get --purge remove bumblebee***


3.Инсталирайте Nvidia Prime с командата :

**sudo apt-get install nvidia-prime**

След това рестартирайте и отворете Nvidia X Server Settings :

![nvidia2](https://github.com/etem/etem.github.io/raw/master/assets/images/nvidia/nvidia2.png)

Както виждате вече имате избор за превключване между двете видеокарти.

Не е задължително но за ваше улеснение бих препоръчал инсталирането на Nvidia Prime Indicator, който е един индикатор в горния панел и показва коя видеокарта се използва в момента.
Също така може да се превключва и чрез него.
Ето какво представлява :

![nvidia3](https://github.com/etem/etem.github.io/raw/master/assets/images/nvidia/nvidia3.png)


Можете да го инсталирате чрез PPA:

**sudo add-apt-repository ppa:nilarimogard/webupd8**

**sudo apt-get update**

**sudo apt-get install prime-indicator**


Може да се наложи да рестартирате за да се появи индикаторът.
Честито вече може да превключвате между видеокартите в Ubuntu.

{% include disqus.html %}
