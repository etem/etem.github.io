---
layout: post
title:  "Радио през конзолата.Музика за душата и админите :)"
date:   2014-10-16 12:39:31
comments : true
categories: linux
banner_image: radio/cover.png
---

Знаехте ли че може да се слуша радио през конзолата?
Благодарение на Конзолно Радио на [Ивайло Кузев](https://plus.google.com/u/0/+IvayloKuzev/posts) това е много лесно и приятно.
Програмата представлява шел скрипт който използва Mplayer за пускане на плейлистите.Можете да избирате между над 40 български радиостанции като се поддържа добавяне на станция по ваш избор.
Също така програмата може да записва стриймове в mp3 файл.

При Ubuntu програмата може да се инсталира чрез командите :

**echo "deb http://dl.bintray.com/etem/deb /" | sudo tee -a /etc/apt/sources.list**

**sudo apt-get update**

**sudo apt-get install konzolno-radio**


След инсталация може да извикате програмата с командата **konzolno-radio**.
За да видите списък с поддържаните радиа може да извикате програмата с опция **-l** : 

![radio1](https://github.com/etem/etem.github.io/raw/master/assets/images/radio/radio1.png)


За да пуснете определена радиостанция просто задайте опция **-p** и номера на станцията при извикване на програмата.
Например ако искате да слушате радио N-Joy,то командата ще е **konzolno-radio -p 7** :

![radio2](https://github.com/etem/etem.github.io/raw/master/assets/images/radio/radio2.png)


Списък с поддържаните опции може да видите при извикване с опция **-h**.
За повече информация,инсталация при други системи или за връзка с автора може да погледнете в [oфициалният сайт](http://ivoarch.github.io/konzolno-radio/) на програмата.