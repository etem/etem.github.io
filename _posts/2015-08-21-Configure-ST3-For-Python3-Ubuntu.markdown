---
layout: post
title:  "Конфигуриране на Python3 build system при ST3 - Ubuntu"
date:   2015-08-21 09:38:31
comments : true
categories: other
banner_image: stotinkaos.png
---

Отскоро започнах да пиша изцяло на Python3 както се препоръчва и смених Sublime Text версия 2 със 3.
Това което забелязах е че при билдване на кода ST3 все пак използва версията на python по подразбиране в системата - в случая 2.7.9 при Ubuntu.
Понеже няма готова build система за специално за Python3 и се наложи да създам такава.

Ако се сблъскате със същия проблем това което трябва да направите е следното : 

Отваряте ST3 и от Tools > Build System избирате New Build System.
Ще ви отвори подпрозорец със шаблон за нова build система.
Изтрийте шаблона и въведете следния код : 

<pre><code>{
    "cmd": ["/usr/bin/python3", "-u", "$file"],
    "file_regex": "^[ ]*File \"(...*?)\", line ([0-9]*)",
    "selector": "source.python",
    "encoding": "utf8",
    
}</code></pre>