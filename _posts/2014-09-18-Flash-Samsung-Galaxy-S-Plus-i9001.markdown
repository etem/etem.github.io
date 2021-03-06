---
layout: post
title:  "Флашване на Samsung Galaxy S Plus i9001"
date:   2014-08-09 11:39:31
comments : true
categories: android
banner_image: android/cover.png
---

Открай време се каня да флашна един S Plus, понеже работи прекалено бавно и доста често се държи неадекватно. Най-накрая му излезе късметът :)
Понеже не успях да намеря никакви ръководства за инсталиране на Android KitKat на български език в интернет, ще се постарая да напиша елементарно ръководство.

<span style="color: red">Внимание! Това е сравнително елементарна процедура, но все пак винаги има риск телефонът да се прецака до крайна степен(bricked). Не поемам отговорност за повредени устройства. Правете това на собствен риск!</span>

Преди да започнете ще трябва да си свалите някои файлове от интернет. А те са :

[Easy Root for i9001](http://forum.xda-developers.com/showthread.php?t=1253707)(Незадължителен ако вече сте root-нали телефона си)

[CWM Recovery v6.0.4.9](http://d-h.st/nQK)

[Cyanogen Mod 11 by ADC-Team Release 12](http://forum.xda-developers.com/showthread.php?t=2579431)

[Google Apps for Android KitKat](http://d-h.st/users/dhacker29?fld_id=27426)(Свалете си това което е най-актуално)


Подгответе предварително файловете като ги копирате директно в SD картата, без да ги слагате в папки.
Процедурата е сравнително лесна, и се състои от следните стъпки :

**1**.Съветвам ви ако имате документи или някакви данни на телефона да ги запазите някъде, например да ги копирате на компютъра, понеже флашването на ОС  по всяка вероятност ще ви затрие данните.

**2**.Нужно условие е телефона да е root-нат. С Easy Root това става много лесно:

Рестартирате телефона и задържете едновременно бутона за включване и бутона за увеличаване на звука.
Задържате докато не видите логото на Samsung и след това отпускате. Телефонът влиза в Recovery режим и от там с помощта на бутоните избирате опцията **apply update from sdcard**. След това от менюто посочвате Easy Root for i9001.zip и потвърждавате с Yes, и изчаквате да ви изпише че архива е инсталиран.

**3**.Флашване на Recovery Manager-а, който е един вид специален интерфейс през който се бърникат неща като инсталиране на външни програми, хард ресет на телефона и др. Флашването на стоковият Recovery Manager е задължително условие за да може да се извърши инсталирането на новата операционна система.
Трябва пак да влезете в Recovery Mode с бутона за включване и и увеличаване на звука. След това изчиствате телефона с **Wipe Data/Factory Reset и Wipe cache partition**.
След като свърши чистенето пак през **apply update from sdcard** посочвате архива на CWM(CWM_6.0.4.9_*). След успешна инсталация рестартирате през **Reboot Now** и телефонът вече има инсталиран новото CWM Recovery.

**4**.Инсталиране на самата ОС(Android 4.4.2). Изключвате телефона отново и чрез същата комбинация от бутони влизате в Recovery Manager-а, който след инсталацията на CWM ще е доста променен.
Чистете кеша с **Wipe Data/Factory Reset** и **Wipe cache partition**.
Чрез опцията **Install zip from sdcard** избирате имиджа на на мода, който го свалихте(CM11-0.-2014***).

Изчаквате няколко минути докато се инсталира и след успешна инсталация пак през същата опция избирате да се инсталира Google Apps(gapps архива). Рестартирате и честито вече имате най-новата версия на андроид за i9001, който всъщност е мод на Cyanogen.

Ето едно видео в което е показано как се прави с разликата че там вече има инсталиран CWM Recovery, и модът, който е даден при линковете на видеото не проработи при мен :

[![Flash Samsung Galaxy](http://img.youtube.com/vi/__9HpKcxlyg/0.jpg)](http://www.youtube.com/watch?v=__9HpKcxlyg)


{% include disqus.html %}
