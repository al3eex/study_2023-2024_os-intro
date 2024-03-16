---
## Front matter
title: "Лабораторная работа №4"
subtitle: "git-flow"
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

Разобраться в работе git-flow, релизах и продвинутой работе с branch-ингом.

# Задание

Выполнить работу для тестового репозитория, Преобразовать рабочий репозиторий в репозиторий с git-flow и conventional commits.

# Выполнение лабораторной работы

## Шаг 1

Продемонстрировал установку `node, pnmp, git-flow`, создал репозиторий git-extended и сделал первый коммит.

![создание git-extended и первый коммит](image/1.png){#fig:001 width=70%}

## Шаг 2
Редактирование package.json

![Редактирование package.json](image/2.png){#fig:002 width=70%}

## Шаг 3

Создал релиз версии 1.0.0 с помощью `git flow`.

![первый релиз 1.0.0](image/3.png){#fig:003 width=70%}

## Шаг 4
Создал feature-branch с помощью git flow и сделал merge в develop ветку.

![feature-branch и merge в develop](image/4.png){#fig:004 width=70%}

## Шаг 5
Создал релиз версии 1.2.3 с помощью `git flow`.

![первый релиз 1.2.3](image/5.png){#fig:005 width=70%}

# Выводы

Во время выполнения лабораторной работы я углубил свои знания экосистемы git и научился продвинутому пользованию релизами и ветками разработки.
