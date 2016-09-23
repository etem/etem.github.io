---
layout: post
title:  "Ubuntu kernel 4.x Broadcom wireless fix"
date:   2016-01-27 16:32:31
comments : true
categories: linux
---

Днес при обновяване на ядрото на Ubuntu 14.04 LTS от 3.x до последното използвано във Wily 4.x ядро, безжичната карта на лаптопа ми - BCM43227 - спря да работи.
Оказа се че пакетът bcmwl-kernel-source в официалните хранилища не е съвместим с ядрата от 4-та версия.

След малко проучване установих че най-лесният вариант да се оправи проблемът, е да се инсталира пачнатият пакет от PPA хранилище : 

**sudo apt-get remove bcmwl-kernel-source**

**sudo add-apt-repository ppa:longsleep/bcmwl**

**sudo apt-get update**

**sudo apt-get install bcmwl-kernel-source**


За тези които използват Ubuntu с версия 15.04 и нагоре този проблем не би трябва да съществува.
