---
layout: post
title:  "Промяна на режима на cpufreq в Ubuntu"
date:   2015-05-20 16:25:31
comments : true
categories: linux
---
    
Има един досаден бъг при cpuqfreq под Ubuntu Mate а може би и другите разновидности на Ubuntu и той се състои в това че cpufreq винаги работи в режим на управление "ondemand".
Даже и да въведете команда която променя режима след рестарт в rc.local,след него се стартира скриптът /etc/init.d/ondemand и връща governor на "ondemand".

Решението се оказа малко грубо но много просто.
Въвеждате серията от команди за настройване на режима в /etc/rc.local : 

**echo powersave >  /sys/devices/system/cpu/cpu1/cpufreq/scaling_governor**

**echo powersave >  /sys/devices/system/cpu/cpu0/cpufreq/scaling_governor**


Естествено ако процесорът ви е 4-ядрен ще трябват още 2 команди за другите ядра.Също така заменяте "powersave" с режима който искате да работи процесорът като performance,conservative и др.

След това забранявате изпълнението на "ondemand" като махате правата за изпълнение : 

**sudo chmod -x /etc/init.d/ondemand**


Вече със сигурност няма как да се изпълни скрипта :) 