---
# Front matter
lang: ru-RU
title: "Лабораторная работа №7"
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

Изучить возможности создания презентаций в LaTeX с использованием документа class beamer. Освоить основные структуры и элементы презентаций, включая создание слайдов, использование блоков, списков и эффектов анимации.

# Задание

1. Изучить структуру презентации в beamer  
2. Создать титульный слайд  
3. Освоить различные типы слайдов  
4. Научиться управлять появлением элементов  
5. Изучить темы оформления  
6. Создать презентацию  

# Выполнение лабораторной работы

## 1. Структура презентации

Презентация состоит из набора слайдов:

$$
\[
S = \{s_1, s_2,\ldots, s_n\}}
\]
$$

Каждый слайд является отдельной частью презентации.

## 2. Титульный слайд

Титульный слайд содержит основную информацию о презентации: название, автора и дату.

Его можно представить как:

$$
\[
s_1 = (\text{title}, \text{author}, \text{date})
\]
$$

## 3. Типы слайдов

В презентации можно использовать разные типы слайдов:

- текстовые слайды  
- слайды с блоками  
- слайды с колонками  
- слайды со списками  

Это позволяет удобно структурировать информацию.

## 4. Пошаговое появление элементов

Для постепенного отображения информации используются специальные команды.

Это можно представить как последовательное добавление элементов:

$$
\[
E_1 \rightarrow E_2 \rightarrow E_3 \rightarrow \cdots
\]
$$

Таким образом информация появляется по шагам.

## 5. Типы слайдов

В презентации можно использовать разные типы слайдов:

- текстовые слайды
- слайды с блоками
- слайды с колонками
- слайды со списками

Пример слайда с блоком:

$$ 
\text{block} = 
\begin{cases}
\text{заголовок блока} \\
\text{содержимое блока}
\end{cases}
$$

## 6. Темы оформления

В beamer можно использовать разные темы оформления, которые меняют внешний вид презентации.

## 7. Создание презентации

В ходе работы была создана презентация, включающая различные типы слайдов и элементы оформления.

# Выводы

В ходе выполнения лабораторной работы были изучены основные возможности создания презентаций в LaTeX с использованием документа class beamer.

Были освоены следующие элементы:

- Создание титульного слайда с помощью команд `\title`, `\author`, `\date` и `\maketitle`

- Структурирование презентации с использованием окружения `frame` для создания отдельных слайдов

- Работа с блоками (`block`, `exampleblock`, `alertblock`) для выделения различного типа информации

- Организация материала в несколько колонок с помощью окружения `columns`

- Создание маркированных и нумерованных списков (`itemize`, `enumerate`)

- Применение эффектов анимации с помощью команд `\pause` и `\uncover` для пошагового появления элементов на слайде

- Использование различных тем оформления (`\usetheme`) для изменения визуального стиля презентации

Полученные навыки позволяют создавать профессионально оформленные презентации с четкой структурой, что особенно полезно для научных докладов и учебных выступлений. Преимущества использования LaTeX для презентаций включают:

$$ \text{Преимущества} = \{\text{единообразие оформления}, \text{легкость вставки формул}, \text{автоматическая нумерация}, \text{сосредоточение на содержании}\} $$
