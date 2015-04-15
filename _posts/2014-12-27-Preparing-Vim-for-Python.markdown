---
layout: post
title:  "Подготвяне на vim за програмиране на Python"
date:   2014-12-27 12:39:31
comments : true
categories: linux python
---

Всеки Linux потребител рано или късно открива топлата вода - ViM(Vi Improved).
Както се знае vim е един от двата най-велики текстови редактори под Linux.
Другият е Emacs.
За пълната история на vim и неговите възможности може да прочетете [тук](http://bg.wikipedia.org/wiki/Vim).

С подходящите плъгини може да превърнете vim от текстообработваща програма към пълнофункционално IDE с подръжка на syntax highlight,autoindent и autocomplete.
Например аз използвам vim като IDE за програмиране на Python.

Като за начало едно от най-важните неща за един програмист на Python е autoindent-a.
Това практически е автоматичното наместване на кода навътре след дефиниция на функция,клас,цикъл и подобни.

За да накарате vim да разбере Python-ския стил на писане добавете следния код във вашия ~/.vimrc файл(Ако няма създадете такъв):


**syntax on filetype indent plugin on**

**set tabstop=8**

**set expandtab**

**set shiftwidth=4**

**set softtabstop=4**


След това идва ред на code autocompletion,или просто казано автоматичното довършване на кода,ако това е правилният превод.
Безспорно фаворитът ми в тази област е [YouCompleteMe](https://github.com/Valloric/YouCompleteMe).

При Ubuntu деривативите може да го инсталирате супер лесно,с командите :

**sudo apt-get install vim**

**sudo apt-get install vim-youcompleteme**

**apt-get install vim-addon-manager**

**vam install youcompleteme**


Ето и снимка от въпросната добавка :

![vimpython](https://github.com/etem/etem.github.io/raw/master/assets/images/vimpython.png)


И трето,не по-маловажно е цветовата схема.Вероятно vim ще използва някаква цветова схема по подразбиране,но вие също може да изберете такава.
Наличните цветови схеми може да видите с командата :

**:colorscheme + Tab**

При всяко натискане на Tab ще видите имената на различни цветови схеми.За да запазите избраната цветова схема по подразбиране добавете командата + цветовата схема във вашият .vimrc файл.
Например :

**colorscheme elflord**

И така вашият vim вече е готов за програмиране на Python :)