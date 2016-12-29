---
layout: post
title:  "Nautilus enable Backspace key"
date:   2016-12-29 20:23:31
comments : true
categories: linux
---

Може би сте забелязали че в последните версии на Gnome Nautilus/Files е премахната опцията за връщане към горната горната директория чрез натискане на Backspace. 

Не знам кой и как решил че това вече няма да се използва но идеята никак не ми хареса :) 

След доста търсене успях да намеря решение на проблема. А то се състои от това да се инсталира добавка за Nautilus - [Nautilus Python](https://wiki.gnome.org/Projects/NautilusPython).

&nbsp;

Инсталира се с командите : 

**apt-get install python-nautilus** за Debian/Ubuntu


**dnf install nautilus-python-1.1-10.fc24.x86_64** за Fedora 


Тази добавка ни позволява да инсталираме и използваме допълнителни Python скриптове към Nautilus. 

&nbsp;

В случая ни ще го използваме за инсталирането на още един допълнителен [Python скрипт](https://github.com/riclc/nautilus_backspace), който ще ни върне Backspace клавиша.


Свалете скрипта Backspace.py и го поставете в ~/.local/share/nautilus-python/extensions/. Рестартирайте Nautilus - **killall nautilus** и Backspace трябва да работи отново. 




