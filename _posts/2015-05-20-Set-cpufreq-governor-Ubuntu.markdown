---
layout: post
title:  "Промяна на режима на cpufreq в Ubuntu"
date:   2015-05-20 16:25:31
comments : true
categories: linux
---
    
По подразбиране cpufreq в Ubuntu, а може и би деривативите на Debian работи под режим "ondemand". Поради някаква причина понякога може да се наложи да го промените.
Например искате процесорът винаги да работи на максимална честота.
Вариантите ви са два. Единият е да инсталирате **rcconf** и чрез него да забраните изпълнението на "ondemand" при стартиране на системата.


Вторият вариант е малко груб но много прост.
Въвеждате серията от команди за настройване на режима в /etc/rc.local : 

 &nbsp;

**echo powersave >  /sys/devices/system/cpu/cpu1/cpufreq/scaling_governor**

**echo powersave >  /sys/devices/system/cpu/cpu0/cpufreq/scaling_governor**

 &nbsp;


Естествено ако процесорът ви е 4-ядрен ще трябват още 2 команди за другите ядра. Също така заменяте "powersave" с режима който искате да работи процесорът като performance, conservative и др.

След това забранявате изпълнението на "ondemand", като махате правата за изпълнение : 


**sudo chmod -x /etc/init.d/ondemand**


Скриптът вече със сигурност няма как да се изпълни :) 

{% include disqus.html %}
