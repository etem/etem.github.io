---
layout: post
title:  "Промяна на цветовете в bash"
date:   2014-06-29 11:39:31
comments : true
categories: linux
banner_image: bash-cover.png
---


След малко ровене открих как да променя цветовете в bash на различни Линукс дистрибуции.
За пример аз използвам Ubuntu Server 14.04 LTS и CentOS 6.5.Доколкото разбрах тази опция автоматично е спряна в Debian базираните дистрибуции.
Нужното условие е да премахнете отметката # пред `force_color_promt=yes` във вашия `~/.bashrc` файл. В зависимост от терминалния емулатор(Guake, Gnome Terminal) може да проработи и без да се премахне отметката но, в повечето случаи това ще е нужно. Можете да редактирате вашия(за всеки потребител е отделен!) ~/.bashrc файл с някой вграден текстов редактор, който работи в терминала като например nano или vim.

В Debian и Ubuntu базираните дистрибуции това може да се изпълни с командата:


`sudo nano ~/.bashrc`

След като отворите въпросния файл с nano,натиснете `Ctrl+W` за търсене и напишете `force`. След като редактора намери реда със съвпадението премахнете отметката за коментар (#).
Можете много лесно да направите ваша цветова схема за bash в [Bashrc Generator][bashrc]. Сайтът ще ви предостави код подобен на този:

`export PS1="\[\e[00;33m\]\u\[\e[0m\]\[\e[00;37m\]@\h:\[\e[0m\]\[\e[00;36m\][\w]:\[\e[0m\]\[\e[00;37m\] \[\e[0m\]"`

Който трябва да копирате вътре във файла ~/.bashrc,за предпочитане в края. След като направите всички промени във въпросния файл, натиснете Ctrl+X и Enter за запаметяване на промените. Честито вече разполагате с цветен терминал :) Може да изпробвате промените веднага като се релогнете отново в системата. Ето го резултатът при мен:

![bash](https://github.com/etem/etem.github.io/raw/master/assets/images/bash.png)

[bashrc]: http://bashrcgenerator.com

{% include disqus.html %}
