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

Изучить возможности создания презентаций в LaTeX с использованием документа class beamer. Освоить основные структуры и элементы презентаций, включая создание слайдов, использование блоков, списков и эффектов анимации..

# Задание

1. Изучить структуру презентации в beamer  
2. Создать титульный слайд  
3. Освоить различные типы слайдов  
4. Научиться управлять появлением элементов  
5. Изучить темы оформления  
6. Создать презентацию  

# Выполнение лабораторной работы

# 1. Структура презентации

Презентация состоит из набора слайдов:

$$
\[
S = \{s_1, s_2, ..., s_n\}
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

##  4. Работа с блоками

В beamer используются блоки для выделения различных типов информации:

$$ \text{типы блоков} = \{\text{обычный блок}, \text{блок-пример}, \text{блок-предупреждение}\} $$

Каждый блок имеет заголовок и содержимое:

$$ \text{block} = \{\text{заголовок}, \text{содержимое}\} $$


## 5. Работа с колонками

Для разделения слайда на несколько колонок используется специальное окружение. Ширина каждой колонки задается относительно общей ширины текста:

$$ \text{ширина колонки}_i = w_i \times \text{ширина текста} $$

При этом сумма ширин всех колонок равна ширине текста:

$$ \sum_{i=1}^{n} w_i = 1 $$

### 6. Работа со списками

В презентациях используются два типа списков:

$$ \text{типы списков} = \{\text{маркированный}, \text{нумерованный}\} $$

**Маркированный список** представляет собой набор пунктов, каждый из которых отмечен символом:

$$ \text{список} = \{\text{пункт}_1, \text{пункт}_2, ..., \text{пункт}_n\} $$

**Нумерованный список** представляет собой последовательность пронумерованных пунктов:

$$ \text{список} = \{1. \text{пункт}_1, 2. \text{пункт}_2, ..., n. \text{пункт}_n\} $$

### 7. Пошаговое появление элементов

Для постепенного отображения информации используются специальные команды. Это позволяет управлять тем, какие элементы и в какой последовательности появляются на слайде.

Процесс пошагового появления можно представить как последовательное добавление элементов:

$$ \text{элемент}_1 \rightarrow \text{элемент}_2 \rightarrow \text{элемент}_3 \rightarrow ... $$

Для более точного управления можно указывать, на каких именно слайдах должен появляться тот или иной элемент:

$$ \text{элемент}\langle n \rangle = \text{появляется только на слайде } n $$

$$ \text{элемент}\langle n-m \rangle = \text{появляется на слайдах с } n \text{ по } m $$

$$ \text{элемент}\langle n- \rangle = \text{появляется на слайде } n \text{ и всех последующих} $$

### 8. Темы оформления

В beamer доступны различные темы оформления, которые изменяют внешний вид презентации:

$$ \text{темы} = \{\text{Madrid}, \text{Copenhagen}, \text{Warsaw}, \text{Berlin}, \text{Singapore}\} $$

Каждая тема имеет свое цветовое решение и стиль оформления элементов.

### 9. Созданная презентация

В ходе работы была создана презентация, которая включала следующие слайды:

- титульный слайд
- слайд с содержанием
- слайды с блоками различного типа
- слайд с колонками
- слайд со списками
- слайд с математическими формулами
- заключительный слайд

Структуру созданной презентации можно представить как:

$$ P = \{s_{\text{титульный}}, s_{\text{содержание}}, s_{\text{блоки}}, s_{\text{колонки}}, s_{\text{списки}}, s_{\text{формулы}}, s_{\text{заключение}}\} $$

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

Полученные навыки позволяют создавать профессионально оформленные презентации с четкой структурой, что особенно полезно для научных докладов и учебных выступлений. 

**Преимущества использования LaTeX для презентаций:**

$$ \text{преимущества} = 
\begin{cases}
\text{единообразие оформления всех слайдов} \\
\text{легкость вставки математических формул} \\
\text{автоматическая нумерация разделов} \\
\text{возможность сосредоточиться на содержании} \\
\text{широкий выбор тем оформления}
\end{cases} $$

Полученные навыки позволяют мне создавать профессионально оформленные презентации с четкой структурой, что особенно полезно для научных докладов и учебных выступлений.

---
