---
# Front matter
title: "Отчёт по лабораторной работе"
subtitle: "Лабораторная работа 3"
author: "Дзугаева Лилия Владславовна"

# Generic otions
lang: ru-RU

# Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

# Pdf output format
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
### Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Misc options
indent: true
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage  # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей.

# Задание

Лабораторная работа подразумевает работу с виртуальной машиной _VirtualBox_ операционной системы _Linux_, дистрибутив _Centos_, с консолью и атрибутами файлов для групп пользователей.

# Выполнение лабораторной работы

1. В установленной при выполнении предыдущей лабораторной работы операционной системе создаю учётную запись пользователя _guestt_ и _guest2_ - задаю имя пользователя и пароль. (рис. 1)

![рис. 1. Создание новых учетных записей](image/1.jpg){ #fig:001 width=70% }

2. Добавляю пользователя _guest2_ в группу _guestt_. (рис. 2)

![рис. 2. Добавление пользователя в группу](image/2.jpg){ #fig:001 width=70% }

3. Осуществляю вход в систему от двух пользователей на двух разных консолях: _guestt_ на первой консоли и _guest2_ на второй консоли.  (рис. 3)

![рис. 3. Вход в систему от двух пользователей](image/3.jpg){ #fig:001 width=70% }

4. Для обоих пользователей командой pwd определяю директорию, в которой я нахожусь. Вывод директории _root_. Сравниваю её с приглашениями командной строки. (рис. 4)

![рис. 4. Определение директории](image/4.jpg){ #fig:001 width=70% }

5. Уточняю имя моего пользователя, его группу, кто входит в неё и к каким группам принадлежит он сам. Определяю командами _groups guestT_ и _groups guest2_, в какие группы входят пользователи _guestt_ и _guest2_. Сравниваю вывод команды groups с выводом команд _id -Gn_ и _id -G_. (рис. 5-7)

![рис. 5. Определение имени пользователя](image/5.jpg){ #fig:001 width=70% }
![рис. 6. Определение группы](image/5.1.jpg){ #fig:001 width=70% }
![рис. 7. Сравнение выводов](image/5.2.jpg){ #fig:001 width=70% }

6. Сравниваю полученную информацию с содержимым файла _/etc/group_. Просмотрите файл командой _cat /etc/group_ (рис. 8)

![рис. 8. Сравнение информации с содержимым файла](image/6.jpg){ #fig:001 width=70% }

7. От имени пользователя _guest2_ выполняю регистрацию пользователя _guest2_ в группе _guestt_ командой _newgrp guest_ (рис. 9)

![рис. 9. Регистрация пользователя в группе](image/7.jpg){ #fig:001 width=70% }

8. Таблица "Минимальные права для совершения операций от имени пользователей
входящих в группу".

| Операция | Минимальные права на директорию | Минимальные права на файл | 
|-|-|-|
| __Создание файла__ | __-__ | __+__ |
| __Удаление файла__ | __-__ | __-__ |
| __Чтение файла__ | __+__ | __+__ | 
| __Запись в файл__ | __-__ | __-__ | 
| __Переименовывание файла__ | __-__ | __+__ | 
| __Создание поддиректории__ | __+__ | __-__ |
| __Удаление поддиректории__ | __-__ | __-__ |   

# Выводы

Приобрела практические навыки работы в консоли с атрибутами файлов, закрепила теоретические основы дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux.

# Список литературы{.unnumbered}

::: {#refs}
:::
