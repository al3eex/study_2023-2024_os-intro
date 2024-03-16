---
## Front matter
lang: ru-RU
title: Лабораторная №4
subtitle: Отчёт-презентация
author:
  - Захаров А.П.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 9 марта 2024

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis

## Fonts
mainfont: PT Sans
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9

header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'

---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Захаров Александр Петрович
  * студент
  * Российский университет дружбы народов
  * [a.zaxapov@yandex.ru](mailto:a.zaxapov@yandex.ru)

:::
::::::::::::::

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
