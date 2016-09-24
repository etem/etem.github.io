---
layout: post
title:  "Инсталиране на SublimeText3 при StotinkaOS/CentOS6/RHEL6"
date:   2015-09-01 14:28:31
comments : true
categories: linux
banner_image: st3.png
---

Днес ми се наложи да инсталирам ST3 на StotinkaOS, и видях че готови пакети има само за Ubuntu.За останалите дистрибуции се предлага tar.gz архив който трябва вие ръчно да инсталирате.

Започнете като си отворите един терминал и си свалите архива : 

**wget** http://c758482.r82.cf2.rackcdn.com/sublime_text_3_build_3083_x32.tar.bz2  за 32 битовата и 

**wget** http://c758482.r82.cf2.rackcdn.com/sublime_text_3_build_3083_x64.tar.bz2 за 64 битовата версия.  


Разархивирайте архива:  

**tar vxjf sublime_text_3_build_*.tar.bz2**  




С администраторски права преместете новосъздадената папка **sublime_text_3** на по подходящо място - например /opt/ :  


**sudo mv sublime_text_3 /opt/**  






Създайте symlink на изпълнимия файл на програмата в /usr/bin:  


**sudo ln -s /opt/sublime_text_3/sublime_text /usr/bin/sublime_text**  






Вече може да изпълнявате програмата от терминала с командата **sublime_text**. 






За да създадете десктоп икона е нужно да редактирате някои полета на файла /opt/sublime_text_3/sublime_text.desktop. Отворете файла с някой текстов редактор и променете полетата **Exec** и **Icon** по следния начин : 

**Exec=/opt/sublime_text_3/sublime_text %F**

**Icon=/opt/sublime_text_3/Icon/32x32/sublime-text.png**





Накрая копирате файла /opt/sublime_text_3/sublime_text.desktop в ~/Desktop/ и сте готови за работа :) 
Може да се наложи да излезете и пак да влезете в системата(Log Out & Log In),  за да се визуализира иконката коректно.


{% include disqus.html %}
