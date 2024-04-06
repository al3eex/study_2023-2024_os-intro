---
## Front matter
title: "Лабораторная работа №8"
subtitle: "Ознакомление с файловой системой Linux, её структурой, именами и содержанием каталогов."
author: "Захаров Александр Петрович"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
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
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Ознакомление с файловой системой Linux, её структурой, именами и содержанием каталогов. Приобретение практических навыков по применению команд для работы с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.

# Задание

Ознакомится с файловой системой Linux (или UNIX подобных систем).

Отработать практические навыки по применению команд для работы с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.

# Выполнение лабораторной работы

## Пункт 1

Выполнил все примеры из первой части работы.

![выполнение примеров 1](image/lab7-1-1.png){#fig:001 width=70%}

![выполнение примеров 2](image/lab7-1-2.png){#fig:002 width=70%}

![выполнение примеров 3](image/lab7-1-3.png){#fig:003 width=70%}

## Пункт 2

### Описание команд

1. Скопировал файл `/usr/local/include/idn-free.h` в домашний каталог и назвал его `equipment` командой `cp /usr/local/include/idn-free.h ~/equipment`,

2. Создал каталог `~/ski.plases` командой `mkdir ~/ski.plases`,

3. Переместил `equipment` в `ski.places` командой `mv equipment ski.places`,

4. Переименовал `equipment` в `equiplist` командой `mv ski.plases/equipment ski.plases/equiplist`,

5. Создал файл `touch abc1` с именем `abc1` и скопировал его в каталог `cp abc1 ski.plases/equiplist2` переименовав в `equiplist2`,

6. Создал подкаталог `equipment` в `ski.plases` командой `mkdir ski.plases/equipment`,

7. Переместил файлы `equiplist, equiplist2` в подкаталог `ski.plases/equiplist2` командой `mv ski.plases/equiplist ski.plases/equiplist2 ski.plases/equipment`,

8. Создал директорию `newdir`: `mkdir newdir`, и переместил её в `ski.plans`, переименовав в `plans` командой `mv newdir ski.plases/plans`

### Иллюстрация для выполнения пункта 2

![№7.2](image/lab7-2.png){#fig:004 width=70%}

## Пункт 3

### Описание необходимых команд

1. Создал недостающие файлы и директории:
    * `touch my_os feathers`
    * `mkdir australia play`

2. Для приведения файла `my_os` к нужному виду используются команды: 
    * `chmod u+x my_os`
    * `chmod u-w my_os`

3. Для приведения файла `feathers` к нужному виду используется команда `chmod g+w feathers`,

4. Для приведения директории `australia` к нужному виду используется команда `chmod go-x australia`. Сочетание `go-x` убирает право на запуск файла сразу у группы `(g)` и прочих `(o)`, 

5. Для приведения директории `play` к нужному виду используется команда `chmod go-r play`

### Иллюстрация выполнения команд

![модификация `my_os, feathers, australia`](image/lab7-3-1.png){#fig:005 width=70%}

![модификация `play`](image/lab7-3-2.png){#fig:006 width=70%}

![Результат](image/lab7-3-3.png){#fig:007 width=70%}

## Пункт 4

### Порядок выполнения задания №7.4

1. Просмотрел содержимое файла: `cat /etc/passwd`

2. Скопировал `feathers` в `file.old`: `cp feathers file.old`

3. Переместил `file.old` в `play`: `mv file.old play`

4. Сделал каталог `fun` и скопировал в него каталог `play`: 
    * `mkdir fun`
    * `cp -r play fun`

5. Переместил каталог `fun` в `play` и назвал его `games`: `mv fun play/games`

1. Лишил всех права на чтение файла `feathers`: `chmod guo-r feathers`

1. При выполнении команды: `cat feathers` получил ответ `cp: feathers: Permission denied`, т.к. в предыдущем пункте закрыл всем право на чтение.

1. То же самое (`cp: feathers: Permission denied`) произошло при выполнении команды `cp feathers feather_copy`

1. Вернул всем права на чтение файла `feathers`: `chmod guo+r feathers`

1. Лишил всех права на выполнение каталога `play`: `chmod guo-x play`

1. Получил ответ `cd: play: Permission denied`, при выполнении `cd play`, т.к. закрыл всем доступ к этому каталогу.

1. Вернул право на выполнение `play`: `chmod guo+x play`

### Иллюстрации для выполнения

![вывод файла `/etc/passwd`](image/lab7-4-1.png){#fig:008 width=70%}

![модификации прав владения и чтения](image/lab7-4-2.png){#fig:009 width=70%}

## Пункт 5

Прочитал `man` для `mount, fsck, newfs_apfs, kill`.

Краткая характеристика:

* `mount` --- используется для подключения файловой системы к локальной директории,  

* `fsck` --- утилита для проверки целостности и исправления проблем с файловой системой в интерактивном режиме,

* `mkfs` (на Mac OS это `newfs_тип-файловой-системы`) --- создаёт файловую систему указанного типа,

* `kill` --- используется для выключения запущенных процессов по id.

Моё выполнение:

![№7.5](image/lab7-5.png){#fig:010 width=70%}

# Выводы

Вовремя выполнения лабораторной работы я впóлне ознакомился с файловой системой Linux, её структурой, именами и содержанием каталогов. Приобрёл практические навыки работы с командами `chmod` и освоил продвинутое пользование командами `mv, cp`.