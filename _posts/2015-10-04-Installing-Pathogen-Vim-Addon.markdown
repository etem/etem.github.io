---
layout: post
title:  "Инсталиране на Pathogen-Vim и Airline чрез Pathogen"
date:   2015-10-04 16:08:31
comments : true
categories: linux
---

Pathogen за ViM е плъгин който помага за лесното управляване на вашият vim 'runtimepath' като добавя в него всяка директория под ~/.vim/bundle което на практика улеснява значително инсталирането на външни плъгини.

За да инсталирате Pathogen изпълнете : 

<pre><code>
mkdir -p ~/.vim/autoload ~/.vim/bundle && \
curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim

</code></pre>

За да проработи плъгина е нужно да добавите следния ред във вашият ~/.vimrc файл:

<pre><code>
execute pathogen#infect()
</code></pre>

Pathogen вече е готов за работа и ще се зарежда при стартиране на Vim.
За да инсталирате други плъгини е нужно да ги поставите в директорията ~/.vim/bundle/.Ще дам пример с Vim-airline.


<h3>Инсталиране на Vim-Airline чрез Pathogen</h3>


За да инсталирате Vim-Airline и изобщо всеки друг плъгин чрез Pathogen е нужно просто да копирате плъгина в ~/.vim/bundle/ директорията:

<pre><code>
git clone https://github.com/bling/vim-airline ~/.vim/bundle/vim-airline
</code></pre>

Pathogen ще се погрижи за зареждането и.По подразбиране лентите за състоянието(statuslines) в Airline са скрити.За да промените това е нужно да добавите **set laststatus=2** във вашият ~/.vimrc файл.
Също така може да промените темата по подразбиране с :AirlineTheme molokai например.Това ще промени темата за едно стартиране.За да я направите по-подразбиране е нужно да добавите **let g:airline_theme='molokai'** във вашият ~/.vimrc файл.

Можете да видите наличните теми от [тук](https://github.com/bling/vim-airline/wiki/Screenshots)


**Забележка!**За да се изобразят специалните символи е нужно да имате инсталирани [Powerline](https://github.com/powerline/fonts) шрифтове и командата **let g:airline_powerline_fonts = 1** във vimrc файла ви.