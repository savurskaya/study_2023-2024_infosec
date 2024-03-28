---
## Front matter
title: "Лабораторная работа №4"
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

Получение практических навыков работы в консоли с расширенными атрибутами файлов.

# Выполнение лабораторной работы

1. От имени пользователя guest определите расширенные атрибуты файла:

![lsattr /home/guest/dir1/file1](image/1.png){#fig:001 width=90%}

2. Установите командой chmod 600 file1 на файл file1 права, разрешающие чтение и запись для владельца файла.

![chmod 600 file1](image/2.png){#fig:002 width=90%}

3. Попробуйте установить на файл /home/guest/dir1/file1 расширенный атрибут a от имени пользователя guest:

![chattr +a /home/guest/dir1/file1](image/3.png){#fig:003 width=90%}

4. Зайдите на третью консоль с правами администратора либо повысьте свои права с помощью команды su. Попробуйте установить расширенный атрибут a на файл /home/guest/dir1/file1 от имени суперпользователя:

![chattr](image/4.png){#fig:004 width=90%}

5. От пользователя guest проверьте правильность установления атрибута:

![lsattr /home/guest/dir1/file1](image/5.png){#fig:005 width=90%}

6. Выполните дозапись в файл file1 слова «test» командой:

![echo "test" /home/guest/dir1/file1](image/6.png){#fig:006 width=90%}

7. После этого выполните чтение файла file1 командой:

![cat /home/guest/dir1/file1](image/7.png){#fig:007 width=90%}

8. Попробуйте удалить файл file1 либо стереть имеющуюся в нём информацию командой:

![echo "abcd" > /home/guest/dirl/file1](image/8.png){#fig:008 width=90%}

9. Попробуйте установить на файл file1 права, например, запрещающие чтение и запись для владельца файла.

![chmod 000 file1](image/9.png){#fig:009 width=90%}

10. Снимите расширенный атрибут с файла /home/guest/dirl/file1 от имени суперпользователя командой

![chattr -a /home/guest/dir1/file1](image/10.png){#fig:010 width=90%}

11. Повторите ваши действия по шагам, заменив атрибут «a» атрибутом «i».

![chattr -i /home/guest/dir1/file1](image/11.png){#fig:011 width=90%}


# Выводы

Мы приобрели необходимые навыки работы в консоли с расширенными атрибутами файлов.
