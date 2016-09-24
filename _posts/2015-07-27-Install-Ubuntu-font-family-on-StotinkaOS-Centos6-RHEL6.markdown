---
layout: post
title:  "Инсталиране на Ubuntu Font Family при StotinkaOS 6.6/RHEL6/CentOS6"
date:   2015-07-27 16:37:31
comments : true
categories: other
banner_image: stotinkaos.png
---

Лично аз много харесвам шрифтовете в пакета Ubuntu Font Family, и ги използвам като шрифтове по подразбиране на десктоп средата.
Ето как може да се инсталират при StotinkaOS 6.6/RHEL6/Centos6 : 

1.Свалете си шрифтовете от http://font.ubuntu.com/.
Аз предпочитам с wget - 
**wget http://font.ubuntu.com/download/ubuntu-font-family-0.80.zip**

2.Разархивирайте архива с unzip и копирайте в **/usr/share/fonts**.

3.Изпълнете командата **fc-cache**.


Готово. Вече шрифтовете могат да се използват от разни програми, като браузъри, терминални емулатори и др.


{% include disqus.html %}
