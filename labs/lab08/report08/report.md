---
## Front matter
title: "Отчёт по лабораторной работе №8"
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

Изучение возможностей пакета **TikZ** для создания графических объектов в LaTeX, включая построение графов, графиков функций и фрактальных структур, а также освоение принципов описания изображений с использованием математических моделей, координат и функций.

# Ход выполнения

## Компиляция и проверка задания *Exercise 8.2.1 (Graph)*

На первом этапе был открыт исходный файл `exercise8_1.tex` и выполнена его компиляция командой `pdflatex`.

В процессе компиляции использовался дистрибутив **TeX Live 2025**. В логе компилятора зафиксировано подключение пакета `tikz` и успешная обработка графических команд.

Компиляция завершилась успешно, что подтверждается созданием PDF-файла и отсутствием критических ошибок. Сообщение `No file .aux` является стандартным для первого прохода.

## Анализ сгенерированного документа *Exercise 8.2.1 (Graph)*

Полученный граф можно описать математически как:

$$
\[
G = (V, E)
\]
$$

где множество вершин:

$$
\[
V = \{A, B, C, D, E, F, Z\}
\]
$$

а множество рёбер:

$$
\[
E = \{(A,B), (B,C), (C,D), (D,E), (E,A), (F,Z), ...\}
\]
$$

Каждая вершина задаётся координатами:

$$
\[
V_i = (x_i, y_i)
\]
$$

Рёбра могут иметь веса:

$$
\[
w_{ij}
\]
$$

Таким образом, граф представляет собой систему связанных элементов с числовыми параметрами.

## Компиляция и проверка задания *Exercise 8.2.2 (Plot)*

Далее был открыт файл `exercise8_2.tex` и выполнена его компиляция.

Использовался тот же дистрибутив **TeX Live 2025** и пакет `tikz`. Компиляция прошла успешно, результатом стал PDF-файл с построенными графиками функций.

## Анализ сгенерированного документа *Exercise 8.2.2 (Plot)*

Графики функций можно описать с помощью математических выражений.

Экспоненциальная функция:

$$
\[
y = e^x
\]
$$

Логарифмическая функция:

$$
\[
y = \ln(x), \quad x > 0
\]
$$

Дополнительно используются вспомогательные линии:

$$
\[
x = 1, \quad y = 1
\]
$$

График функции представляет собой множество точек:

$$
\[
f = \{(x, y) \mid y = f(x)\}
\]
$$

## Компиляция и проверка задания *Exercise 8.2.3 (Sierpinski Carpet)*

На заключительном этапе был открыт файл `exercise8_3.tex` и выполнена его компиляция.

Компиляция прошла успешно, что подтверждает корректность построения сложных графических структур.

## Анализ сгенерированного документа *Exercise 8.2.3 (Sierpinski Carpet)*

Фрактал «ковёр Серпинского» можно описать с помощью итерационного процесса:

$$
\[
S_{n+1} = S_n - C_n
\]
$$

где удаляется центральная часть на каждом шаге.

Площадь фигуры уменьшается по формуле:

$$
\[
A_n = \left(\frac{8}{9}\right)^n A_0
\]
$$

Фракталa обладает свойством самоподобия:

$$
\[
S_n \sim S_{n+1}
\]
$$

Таким образом, сложная структура строится на основе повторения простых операций.

# Вывод

В ходе выполнения работы были изучены основные возможности TikZ, включая:

- описание графов через множества вершин и рёбер  
- построение графиков функций с использованием аналитических выражений  
- использование координатных систем и математических зависимостей  
- моделирование сложных структур с помощью итерационных процессов  

Все задания были успешно выполнены, а графические объекты могут быть полностью описаны с помощью математических формул без использования изображений.
