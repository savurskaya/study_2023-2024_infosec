---
## Front matter
title: "4 этап индивидуального проекта"
subtitle: "Основы информационной безопасности"
author: "Савурская Полина"

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
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Этап 4. Использование nikto. Установка nikto.

# Задание

nikto — базовый сканер безопасности вебсервера. Он сканирует и обнаруживает уязвимости в веб-приложениях, обычно вызванные неправильной конфигурацией на самом сервере, файлами, установленными по умолчанию, и небезопасными файлами, а также устаревшими серверными приложениями.

# Выполнение лабораторной работы

Перед установкой Nikto на ОС macOS и Windows необходимо проверить наличие Perl:

![perl -v](image/1.png){#fig:001 width=90%}

Далее установим Nikto. Для установки в системах, основанных на deb (Ubuntu, Debian, Linux Mint), достаточно выполнить команду:

![sudo apt -y install nikto](image/2.png){#fig:002 width=90%}

В дистрибутивах, основанных на rpm (Red Hat Enterprise Linux, CentOS/Fedora, Mandriva Linux), необходимо выполнить команду:

![sudo dnf -y install nikto](image/3.png){#fig:003 width=90%}

Для проверки корректной установки в терминале введем:

![nikto](image/4.png){#fig:004 width=90%}

# Выводы

Мы установили nikto.


