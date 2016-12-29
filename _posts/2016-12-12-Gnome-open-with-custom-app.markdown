---
layout: post
title:  "Gnome3 open file with custom application"
date:   2016-12-29 20:23:31
comments : true
categories: linux
---

Доколкото видях при Fedora, Gnome 3.22 не предоставя опция "open with custom application" при отваряне на файл.
Единствената опция е да изберете програма от даден списък.

Проблемът е че ако програмата е инсталирана от сорс код, или някакъв друг начин извън пакетната система, има голяма вероятност системата да не я "вижда" и съответно да не е добавена в този списък. 

В случая при мен това е Sublime Text 3 инсталирана ръчно при Fedora 25.

Решението е да се постави .desktop файл за програмката в ~/.local/share/applications/. 

Примерно съдържание на файла при ST3 :

Version=1.0
Type=Application
Name=Sublime Text
GenericName=Text Editor
Comment=Sophisticated text editor for code, markup and prose
Exec=/usr/local/sublime_text_3/sublime_text %F 
Terminal=false
MimeType=text/plain;
Icon=/usr/local/sublime_text_3/Icon/128x128/sublime-text.png
Categories=TextEditor;Development;
StartupNotify=true
Actions=Window;Document;

