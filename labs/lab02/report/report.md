---
## Front matter
title: "Отчет по лабораторной работе №2"
subtitle: "Основы информационной безопасности"
author: "Назармамадов Умед Джамшедович"

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

Получение практических навыков работы в консоли с атрибутами файлов, закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux

# Задание

1. Работа с атрибутами файлов
2. Заполнение таблицы "Установленные права и разрешённые действия" (см. табл. 2.1)
3. Заполнение таблицы "Минимальные права для совершения операций" (см. табл. 2.2)

# Теоретическое введение

Операционная система — это комплекс программ, предназначенных для управления ресурсами компьютера и организации взаимодействия с пользователем. [1]

Права доступа определяют, какие действия конкретный пользователь может или не может совершать с определенным файлами и каталогами. С помощью разрешений можно создать надежную среду — такую, в которой никто не может поменять содержимое ваших документов или повредить системные файлы. [2].

# Выполнение лабораторной работы

Создаём пользователя guest и задаём пароль (рис. [-@fig:001]).

![Создаём пользователя](image/18.jpg){#fig:001 width=70%}

Входим под guest

![Входим](image/19.jpg){#fig:001 width=70%}

Где мы находимся и домашний каталог

![домашний каталог](image/20.jpg){#fig:001 width=70%}

Кто мы и какие группы

![группы](image/21.jpg){#fig:001 width=70%}

Сверяем с /etc/passwd

![Сверяем](image/22.jpg){#fig:001 width=70%}

Смотрим /home и права на подкаталоги

![Смотрим](image/23.jpg){#fig:001 width=70%}

Расширенные атрибуты lsattr по /home

![Расширенные атрибуты](image/24.jpg){#fig:001 width=70%}

Создаём dir1 и смотрим права+атрибуты

![Создаём dir1](image/25.jpg){#fig:001 width=70%}

Снимаем все права с dir1

![Снимаем все права](image/26.jpg){#fig:001 width=70%}

Пробуем создать файл в закрытой dir1

![Пробуем создать файл](image/27.jpg){#fig:001 width=70%}

Эксперименты для Табл. 2.1 (разрешено/запрещено)

![Табл. 2.1](image/28.jpg){#fig:001 width=70%}

Дальше меняем права и пробуем операции. Примеры тестов (записывай в табл. «+»/«−»):

![меняем права](image/29.jpg){#fig:001 width=70%}

![меняем права](image/30.jpg){#fig:001 width=70%}

![меняем права](image/31.jpg){#fig:001 width=70%}

# Выводы

Были получены практические навыки работы в консоли с атрибутами файлов, закреплены теоретические основы дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux.

# Список литературы{.unnumbered}

[1] Операционные системы: https://blog.skillfactory.ru/glossary/operaczionnaya-sistema/

[2] Права доступа: https://codechick.io/tutorials/unix-linux/unix-linux-permissions
