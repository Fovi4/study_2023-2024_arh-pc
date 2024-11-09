---
## Front matter
title: "Отчёт по лабораторной работе №5"
subtitle: "Дисциплина: Архитектура компьютера"
author: "Мутаев Муртазаали Магомедович"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Приобретение практических навыков работы в Midnight Commander. Освоение инструкций языка ассемблера mov и int.

# Задание

1. Работа в Midnight Commander
1. Подключение внешнего файла in_out.asm
1. Задания для самостоятельной работы

# Выполнение лабораторной работы

## Работа в Midnight Commander

Первым делом я открыл Midnight Commander и создал в каталоге *work/arch-pc/lab05* файл *lab5-1.asm* (рис. [-@fig:001]).

![Создание файла в MC](image/Снимок экрана от 2024-11-07 13-52-55.png){#fig:001 width=70%}

Далее я открыл его с помощью клавиши F4 и ввел туда код из методички (рис. [-@fig:002]).

![Код №1](image/Снимок экрана от 2024-11-07 13-53-03.png){#fig:002 width=70%}

Затем создал исполняемый файл и запустил программу. Мне выдало такой результат (рис. [-@fig:003]):

![Результат №1](Снимок экрана от 2024-11-07 16-15-53.png{#fig:003 width=70%}

Программа ожидала ввода текста с клавиатуры, а после ввода программа выключалась.

## Подключение внешнего файла in_out.asm

Я скачал файл *in_out.asm* из ТУИС'a и переместил его в каталог, в котором я работаю. После этого я скопировал файл lab5-1.asm и назвал его *lab5-2.asm* (рис. [-@fig:004]):

![in_out.asm](image/Снимок экрана от 2024-11-07 13-55-48.png){#fig:004 width=70%}

Далее я вставил в файл код из методички, подключив скачаный файл (рис. [-@fig:005]):

![Код №2](image/Снимок экрана от 2024-11-07 14-00-22.png){#fig:005 width=70%}

Опять же, создал исполняемый файл, запустил программу и вот, что мне выдало (рис. [-@fig:006]):

![Результат №2](image/Снимок экрана от 2024-11-07 14-24-50.png){#fig:006 width=70%}

Так же, как и в первый раз, программа ожидала ввода текста.

После этого я заменил sprintLF на sprint, и вот, что мне выдало (рис. [-@fig:007]):

![Результата №2.1](image/Снимок экрана от 2024-11-07 14-28-08.png){#fig:007 width=70%}

В отличие от первой программа, эта давала мне вписать текст с клавиатуры на той же строчке, что и выведенный текст.

## Задания для самостоятельной работы

Передо мной стояла задача изменить 2 вышесделанные программы таким образом, чтоб они выводили на экран то, что я введу с клавиатуры. Ну я это и сделал. Вот первая программа (рис. [-@fig:008]):

![Код №3](image/Снимок экрана от 2024-11-07 16-24-01.png){#fig:008 width=70%}

Я вставил код вывода текста на экран и заменил msg на buf1 (рис. [-@fig:009]):

![Результат №3](image/Снимок экрана от 2024-11-07 16-25-07.png){#fig:009 width=70%}

Вот вторая (рис. [-@fig:010]):

![Код №3.2](image/Снимок экрана от 2024-11-07 15-15-26.png){#fig:010 width=70%}

Я также скопировал код вывода текста и заменил msg на buf1, после чего вывел текст с помощью команды sprint (рис. [-@fig:011]):

![Результат №3.2](image/Снимок экрана от 2024-11-07 16-25-37.png){#fig:011 width=70%}

# Выводы

Я приобрел практические навыки работы в Midnight Commander и освоил инструкции языка ассемблера mov и int.

