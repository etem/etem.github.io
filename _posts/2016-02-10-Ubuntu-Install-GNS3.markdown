---
layout: post
title:  "GNS3 - Инсталация под Ubuntu"
date:   2016-02-10 10:23:31
comments : true
categories: linux
banner_image: networking/gns.png
---

Доскоро най-актуалният готов пакет на GNS3 за Ubuntu беше с версия 0.86.За да се използват версии от 1 нагоре беше нужно да се компилира от сорс код.
Някой най-накрая е решил да ни спести мъките и е пуснал PPA с готови пакети за GNS3, който за мое учудване се обновява редовно.

Мисля че няма нужда да обяснявам предимствата на пакетната система пред ръчното компилиране.

За да инстаталирате GNS3(версия 1.4.1 е актуалната в момента) от PPA въведете следните команди : 

<pre><code>
sudo add-apt-repository ppa:gns3/ppa
sudo apt-get update
sudo apt-get install gns3-gui
</code></pre>

Заедно с последната команда ще се инсталират и зависимостите като qemu,vpcs и други.


{% include disqus.html %}
