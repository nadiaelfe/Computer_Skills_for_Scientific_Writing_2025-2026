---
# Front matter
lang: ru-RU
title: "Лабораторная работа №5"
subtitle: "Дисциплина: Компьютерный практикум по научному письму"
author: "Надиа Эззакат"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # Список рисунков
lot: true # Список таблиц
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Познакомиться с созданием таблиц в LaTeX, изучить различные типы выравнивания колонок, исследовать поведение LaTeX при неправильном количестве элементов в строках таблицы, а также освоить использование команды `\multicolumn` для объединения ячеек.

# Задание

1. Изучить базовую структуру таблиц в LaTeX с использованием пакетов array и booktabs

2. Исследовать различные типы выравнивания колонок: l (влево), c (по центру), r (вправо)

3. Экспериментально проверить поведение LaTeX при:
   - Недостаточном количестве элементов в строке
   - Избыточном количестве элементов в строке

4. Освоить команду `\multicolumn` для объединения ячеек по горизонтали

# Выполнение лабораторной работы


## 1. База данных источников

Все источники можно представить как набор элементов:

$$
\[
B = \{b_1, b_2, ..., b_n\}
\]
$$

Каждый элемент — это отдельный источник информации.

## 2. Ссылки в тексте

Документ связан с источниками через ссылки:

$$
\[
D \rightarrow B
\]
$$

Это означает, что в тексте можно ссылаться на используемые материалы.

## 3. Цитирование

При использовании источников применяется цитирование:

$$
\[
C = f(b_i)
\]
$$

где выбирается нужный источник.

## 4. Упорядочивание

Источники могут быть отсортированы:

$$
\[
b_1 < b_2 < ... < b_n
\]
$$

# Выводы

В ходе выполнения лабораторной работы были получены практические навыки работы с таблицами в LaTeX:

1. **Освоены типы выравнивания колонок** (`l`, `c`, `r`), которые позволяют управлять позиционированием текста в таблицах.

2. **Исследована обработка ошибок** при неправильном количестве элементов в строках:
   - При недостаточном количестве элементов данные смещаются в неправильные колонки
   - При избыточном количестве элементы выводятся за пределами таблицы
   - LaTeX предоставляет информативные сообщения об ошибках для диагностики проблем

3. **Изучена команда `\multicolumn`**, которая необходима для создания объединенных ячеек и иерархических заголовков, улучшающих структурирование данных.

4. **Применены профессиональные пакеты** array и booktabs, которые предоставляют расширенные возможности для создания качественных таблиц в научных документах.

Полученные навыки являются фундаментальными для создания профессиональных научных документов с четкой и структурированной презентацией табличных данных.
