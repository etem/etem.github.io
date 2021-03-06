---
layout: post
title:  "Ubuntu GPG error"
date:   2014-07-01 11:39:31
comments : true
categories: linux
banner_image: apt-get.jpg
---

Поради някаква причина понякога се случва системата инцидентно да затрие някой от ключовете за хранилищата. Тогава най-вероятно при въвеждане на **sudo apt-get update** ще видите горното съобщение за грешка :

![PGPFirst](https://github.com/etem/etem.github.io/raw/master/assets/images/PGPFirst.jpg)

Решението е просто:
От браузъра отваряте [Ubuntu Keyserver](http://keyserver.ubuntu.com/). Тук може да търсите ключове за всички официални хранилища на Ubuntu. В полето **Search String** въвеждате номера на липсващия ключ като поставяте **0x** преди него. В моя случай ключът беше 9A2FD067A2E3EF7B и въведох в полето за търсене 0x9A2FD067A2E3EF7B:

![PGP1](https://github.com/etem/etem.github.io/raw/master/assets/images/PGP1.png)

След като системата ви изпише намерените резултати, в полето uuid ще видите името на хранилището за което търсите ключ. В моя случай това е Launchad PPA for GNS3. Под полето uuid след надписа **sig** ще видите още един линк идентификатор на вашия ключ. След отворите линка ще видите код подобен на този:

![PGP2](https://github.com/etem/etem.github.io/raw/master/assets/images/PGP2.png)

Копирайте целия текст с изключение на първия ред(удебеленият шрифт, който започва с Public Key Server) и го запаметете в някакъв текстов файл, например с името **key1** в десктопа. Отворете един терминал и отидете в десктопа с командата **cd /home/$USER/Desktop/**

След това въведете командата:
**sudo apt-key add key1**

При успешен резултат ще получите отговор : OK от системата. За да изпробвате дали всичко работи въведете : **sudo apt-get update** в терминала. Ако не получите съобщението за грешка значи всичко работи!

П.П.Това решение би трябва да работи при всички Ubuntu базирани дистрибуции като Linux Mint, Lubuntu, Xubuntu, Kubuntu и подобни.

{% include disqus.html %}
