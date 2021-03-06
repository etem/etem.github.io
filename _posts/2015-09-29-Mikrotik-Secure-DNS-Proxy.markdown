---
layout: post
title:  "Настройка и подсигуряване на локално DNS Proxy при MikroTiK RouterOS "
date:   2015-09-29 15:55:31
comments : true
categories: mikrotik
---

MikroTiK RouterOS предоставя една много полезна и лесна за настройване функция - а това е че устройството може да работи като локален DNS сървър/прокси за нашата мрежа.
Ползите са осезаеми - от по-бързото решаване на заявките, вследствие от кеширането и възможността да имате ваши статични записи за устройствата.

Самото настройване е много лесно : 

<pre><code>
ip dns set allow-remote-requests=yes servers=8.8.8.8 cache-size=4096
</code></pre>

Горната команда включва DNS проксито задава 8.8.8.8 за DNS сървър, към който устройството ще се обръща за заявки и настройва размера на кеша на 4096KiB, като по-подразбиране е 2048KiB.

Всичко изглежда добре но има един важен детайл. Ако нямате филтриращи правила във вашият firewall, по-подразбиране проксито отговаря на всички DNS заявки независимо откъде те идват. Това крие известни рискове, най-големият от който е DNS Amplification атаката.

Един от начините да предотвратим това е просто да забраним DNS заявките от външни мрежи. За това се нуждаем от следните 2 правила в /ip firewall filter:

<pre><code>
add chain=input action=drop protocol=tcp in-interface=!ether2 dst-port=53

add chain=input action=drop protocol=udp in-interface=!ether2 dst-port=53

</code></pre>

Ако приемем че ether2 е порта към вътрешната мрежа,следните две правила отхвърлят всички DNS заявки които идват от портове различни от ether2. Нуждаем се от 2 правила за всеки протокол - tcp и udp, понеже DNS използва и двата.

Също така може да посочите от кой точно порт заявките да бъдат отхвърлени.


{% include disqus.html %}
