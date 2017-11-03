---
layout: post
title:  "Sublime Text3 Cyrillic encoding fix"
date:   2016-04-06 15:47:31
comments : true
categories: other
---

Днес ми се наложи да отворя текстов файл който съдържа кирилска кодировка(в случая на руски език) със ST3, и видях че програмата изобразява буквите неправилно.

Решението е просто - добавя се опцията **"fallback_encoding": "Cyrillic (Windows 1251)"** във файла с настройките на потребителя - **Settings** - **User**.

Примерна снимка на конфигурираните настройки : 

![cl1](https://github.com/etem/etem.github.io/raw/master/assets/images/enc.png)


{% include disqus.html %}
