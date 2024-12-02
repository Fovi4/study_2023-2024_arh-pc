---
## Front matter
title: "Отчет по лабораторной работе №6"
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

Освоение арифметических инструкция языка ассемблера NASM.

# Задание

1. Листинг 1
1. Листинг 2
1. Листинг 3
1. Листинг 4
1. Задание для самостоятельной работы

# Выполнение лабораторной работы

## Листинг 1

Я создал файл lab6-1.asm в каталоге work/arch-pc/lab06, и в этот файл вставил код из Листинга 6.1 (рис. [-@fig:001]):

![Листинг 6.1](image/1.png){#fig:001 width=70%}

Запустил программу и получил такой результат (рис. [-@fig:002]):

![Результат Листинга 6.1](image/2.png){#fig:002 width=70%}

Затем изменяю текст программы и вместо символов записываю в регистры числа и у меня выводится пустые символы, тк по таблице ASCII код 10 - пустной символ, наша программа вывела именно 10 код (рис. [-@fig:003]):

![Измененный Листинг 6.1](image/3.png){#fig:003 width=70%}

## Листинг 2

Затем я создаю файл lab6-2.asm, ввожу текст из листинга и запускаю файл в работу: (рис. [-@fig:004]):

![Листинг 6.2](image/4.png){#fig:004 width=70%}

При исполнении этой программы я получил число 10, в этом мне помогла строчка iprintLF. Она выводит числа а не символы (рис. [-@fig:005]):

![Результат Листинга 6.2](image/5.png){#fig:005 width=70%}

Однако, если поменять текст программы и вместо iprintLF написать iprint, то у нас так же будет выведено число, но без переход на следующую строчку (рис. [-@fig:006]):

![Измененный Листинг 6.2](image/6.png){#fig:006 width=70%}

получится вот так: (рис. [-@fig:007]):

![Результат измененного Листинга 6.2](image/7.png){#fig:007 width=70%}

## Листинг 3

теперь я ввожу программу из листинга 6.3 и запускаю: (рис. [-@fig:009]):

![Результат Линстинга 6.3](image/9.png){#fig:009 width=70%}

А теперь изменяю текст программы для вычисления другого выражения следующим образом (рис. [-@fig:010]):

![Измененный Листинг 6.3](image/8.png){#fig:010 width=70%}

И программа выдала мне верный результат (рис. [-@fig:011]):

![Результат измененного Листинга 6.3](image/11.png){#fig:011 width=70%}

## Листинг 4

В качестве другого примера рассмотрим программу вычисления варианта задания по номеру студенческого билета (рис. [-@fig:012]):

![Вычисление варианта](image/12.png){#fig:012 width=70%}

Запустим программу и выясним мой вариант (рис. [-@fig:013]):

![Вариант](image/13.png){#fig:013 width=70%}

Ответим на несколько вопросов:

1. Какие строки листинга 6.4 отвечают за вывод на экран сообщения ‘Ваш вариант:’?

За это отвечают строки 10-11

2. Для чего используется следующие инструкции? *mov ecx, x mov edx, 80 call sread*

Они использются для ввода и считывания значения переменной х

3. Для чего используется инструкция “call atoi”?

Чтобы преобразовать символьное значение в числовое

4. Какие строки листинга 6.4 отвечают за вычисления варианта?

За это отвечают строки 15-20

5. В какой регистр записывается остаток от деления при выполнении инструкции “div
ebx”?

Он записывается в регистр edx

6. Для чего используется инструкция “inc edx”?

Увеличение значения регистра edx на 1

7. Какие строки листинга 6.4 отвечают за вывод на экран результата вычислений?

За это отвечают строки 23-24
 

##Задание для самостоятельной работы 

Написать программу вычисления выражения y = f(x). Программа должна выводить выражение для вычисления, выводить запрос на ввод значения x, вычислять заданное выражение в зависимости от введенного x, выводить результат вычислений. Вид функции f(x) выбрать из таблицы 6.3 вариантов заданий в соответствии с номером полученным при выполнении лабораторной работы. Создайте исполняемый файл и проверьте его работу для значений x2 и x2 из 6.3

Для выполнения этого задани я написал следующую программу (рис. [-@fig:014]):

![Задание для самостоятельной работы](image/14.png){#fig:014 width=70%}

У меня были вопросы в реализации умножения на 1/3, т.к. если записать это дробь в ассемблере, пользуясь знаниями из лекций, в лучшем случае получится 0, а в худшем - ошибка. Я мог умножить значение на 0, но думаю, что деление на 3 было более наглядным. Вот мой результат (рис. [-@fig:015]):

![Результат задания](image/15.png){#fig:015 width=70%}

# Выводы

Я освоил арифметические инструкции языка ассемблера NASM.
