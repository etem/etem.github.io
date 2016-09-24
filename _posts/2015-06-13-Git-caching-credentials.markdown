---
layout: post
title:  "Кеширане на парола в Git"
date:   2015-06-13 22:17:31
comments : true
categories: other
banner_image: git.png
---

При всекидневно използване на Git не е много удобно да си пишете потребителя и паролата за GitHub при всеки push.
Има начин Git да кешира паролата ви за определен период от време.

За да включите опцията въведете следната команда в терминала : 

**git config --global credential.helper cache**

Това включва кеширането - по подразбиране за 15 минути.
Ако искате да промените тоя интервал въведете : 

**git config --global credential.helper 'cache --timeout=3600'**

Горната команда променя времето за кеширане на 1 час(3600 секунди).


{% include disqus.html %}
