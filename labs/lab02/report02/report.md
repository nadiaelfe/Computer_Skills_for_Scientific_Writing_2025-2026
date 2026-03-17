---
## Front matter
title: "Отчёт по лабораторной работе №2"
subtitle: "Computer Skills for Scientific Writing"
author: "Надиа Эззакат"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true
toc-depth: 2
lof: true
lot: true
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
  - \usepackage{float}
  - \floatplacement{figure}{H}

---

# Цель работы

Познакомиться со структурой LaTeX-документа и созданием простых документов.

# Задание

1. Изучить структуру LaTeX-документа

2. Создать простой документ с базовыми элементами

3. Освоить основные команды и окружения LaTeX


# Выполнение лабораторной работы

В этой лабораторной работе мы изучаем основы работы с математическими формулами в LaTeX.

## Формулы в тексте

Внутри текста математические формулы оформляются с использованием символов $. Например, формула $E = mc^2$ является одной из самых известных в физике.

## Выключные формулы

Для более сложных формул используются выключные формулы:

$$E = mc^2$$



## Степени и индексы

Степени и индексы оформляются с помощью символов ^ и _:

$$x^2 + y^2 = z^2$$

$$a_1 + a_2 + a_3 = S$$

$$e^{i\pi} + 1 = 0$$

## Дроби и корни

Для создания дробей используется команда \frac:

$$\frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

Квадратный корень оформляется командой \sqrt:

$$\sqrt{2} \approx 1.414$$

\subsection{Греческие буквы}

В математических формулах часто используются греческие буквы:

$$\alpha + \beta = \gamma$$

$$\sin^2 \alpha + \cos^2 \alpha = 1$$

## Системы уравнений

Для оформления систем уравнений используется среда cases:

$$
f(x) = 
\begin{cases}
x^2 & \text{при } x \geq 0 \\
-x & \text{при } x < 0
\end{cases}
$$


# Выводы

В ходе лабораторной работы была изучена базовая информация о дистрибутиве TeXlive и освоены основные способы его установки . Были получены знания о процессе обновления дистрибутива, что является важным для поддержания актуальной версии LaTeX.

