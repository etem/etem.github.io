---
layout: post
title:  "Xorg вместо Wayland при Fedora 25"
date:   2017-06-16 11:39:00
comments : true
categories: linux
---

В последната версия на Fedora - 25, дисплей сървърът по подразбиране е Wayland compositor вместо Xorg. Което е разбираемо понеже това се планираше от много време насам. 

[Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) е сравнително нов протокол разработван последните няколко години именно с целта да замени изцяло [X/X11](https://en.wikipedia.org/wiki/X_Window_System) в близко бъдеще.

Разбира се както при всеки нов софтуер и тука се срещат дребни бъгове и проблеми. 
Единия от тях е че някои програми просто не работят коректно под Wayland.
Например последната версия на GNS3 - 2.0 и VMware Virtual Network Editor са неизползваеми при Fedora 25.

Добрата новина е, че Xorg все пак е инсталиран в системата, дори и да не се използва подразбиране. 

Включването му става много лесно. За целта трябва да се отвори файла **/etc/gdm/custom.conf** и да се махне коментара пред **WaylandEnable=false** : 

![wayland](https://github.com/etem/etem.github.io/raw/master/assets/images/wayland.png)


Превключването към Xorg е става след рестарт или Log-out на потребителя и избор на опция **Gnome on Xorg** при Log-in.  




{% include disqus.html %}
