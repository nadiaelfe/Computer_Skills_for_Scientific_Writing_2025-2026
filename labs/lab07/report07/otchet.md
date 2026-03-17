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

Изучить основные принципы работы с библиографическими системами natbib и biblatex в LaTeX. Освоить полный цикл генерации библиографии с помощью BibTeX и Biber, научиться добавлять новые источники в базу данных, создавать корректные и некорректные ссылки, а также сравнить вывод различных стилей цитирования, включая числовой формат.

# Задание

1. Изучить структуру презентации в beamer  
2. Создать титульный слайд  
3. Освоить различные типы слайдов  
4. Научиться управлять появлением элементов  
5. Изучить темы оформления  
6. Создать презентацию  

# Выполнение лабораторной работы

## 1. Подготовка файлов

Множество файлов для работы:

$$
F = \{\text{beamer\_basic.tex}, \text{beamer\_blocks.tex}, \text{beamer\_pauses.tex}, \text{beamer\_uncover.tex}, \text{beamer\_layout.tex}\}
$$

---

## 2. Базовая структура презентации (`beamer_basic.tex`)

Структура слайда:

$$
\text{Frame}_i =
\begin{cases}
\text{TitlePage}, & i = 1 \\
\text{ContentSlide}(H_i), & i > 1
\end{cases}
$$

PDF:

$$
\text{beamer\_basic.pdf} : 3 \text{ страницы}
$$

---

## 3. Использование блоков (`beamer_blocks.tex`)

Блоки описываются как:

$$
\text{Block(title)} = \text{важное содержимое}
$$

Блок без заголовка:

$$
\text{Block(\{\})} = \text{контент без заголовка}
$$

PDF:

$$
\text{beamer\_blocks.pdf} : 1 \text{ страница}
$$

---

## 4. Пошаговое раскрытие элементов (`beamer_pauses.tex`)

Список элементов:

$$
\text{List} = \{a_1, a_2, a_3, \dots, a_n\}
$$

С шагами через `\pause`:

$$
S_k = \sum_{i=1}^{k} a_i, \quad k=1..n
$$

Пример:

$$
\begin{aligned}
S_1 &= a_1 \\
S_2 &= a_1 + a_2 \\
S_3 &= a_1 + a_2 + a_3 \\
&\vdots
\end{aligned}
$$

PDF:

$$
\text{beamer\_pauses.pdf} : 5 \text{ страниц}
$$

---

## 5. Точный контроль отображения (`beamer_uncover.tex`)

Элементы через `\uncover<n->`:

$$
x_i \uncover<n_i-> \text{ — появляется на шаге } n_i
$$

Формально:

$$
\text{Frame}_j = \{x_1\uncover<1->, x_2\uncover<2->, x_3\uncover<3->\}
$$

PDF:

$$
\text{beamer\_uncover.pdf} : 4 \text{ страницы}
$$

---

## 6. Смена темы оформления (`beamer_layout.tex`)

Тема и цвет:

$$
\text{Theme} = \text{Warsaw}, \quad \text{ColorTheme} = \text{beaver}
$$

Стиль слайдов:

$$
\text{SlideStyle} : \{\text{заголовки, блоки, панель навигации}\} \to \text{серо-красные оттенки}
$$

PDF:

$$
\text{beamer\_layout.pdf} : 2 \text{ страницы}
$$

---

## Математическое описание всех механизмов Beamer

1. **Структура слайдов**:

$$
\text{Presentation} = \{\text{Frame}_1, \text{Frame}_2, \dots, \text{Frame}_N\}
$$

2. **Блоки**:

$$
\text{Frame}_i = \{\text{Block}_1, \text{Block}_2, \dots, \text{Block}_m\}
$$

3. **Пошаговое раскрытие (`\pause`)**:

$$
S_k = \sum_{i=1}^{k} a_i
$$

4. **Точный контроль (`\uncover`)**:

$$
x_i \uncover<n_i->, \quad i = 1..n
$$

5. **Смена темы и цветовой схемы**:

$$
\text{Appearance} = (\text{Theme}, \text{ColorTheme})
$$
](https://github.com/Djintoba/Laboratories)
---

## Вывод

Класс **beamer** обеспечивает:

$$
\begin{aligned}
&\text{структура слайдов} &&\text{Frame}_i \\
&\text{блоки информации} &&\text{Block}_j \\
&\text{пошаговое раскрытие} &&S_k = \sum_{i=1}^{k} a_i \\
&\text{точное управление появлением} &&x_i \uncover<n_i-> \\
&\text{смена темы и цвета} &&(\text{Theme}, \text{ColorTheme})
\end{aligned}
$$

В ходе выполнения работы были изучены основные возможности создания презентаций в LaTeX с использованием класса **beamer**. Были рассмотрены примеры, демонстрирующие базовую структуру презентации, работу со слайдами, оформление содержимого и управление порядком появления элементов. Произведена компиляция нескольких файлов, что позволило на практике исследовать поведение различных механизмов beamer.

В результате работы были освоены следующие аспекты:

* создание презентации на основе класса `beamer` и использование стандартной структуры (`\title`, `\author`, `\begin{frame}...\end{frame}`);
* работа с блоками (`block`, `exampleblock`, `alertblock`) и оформление ключевых элементов информации;
* применение команды `\pause` для пошагового отображения списков и структур слайдов;
* использование команды `\uncover` для точного контроля момента появления текста, формул и объектов;
* рассмотрение различий между темами оформления и применение комбинации темы *Warsaw* с цветовой схемой *beaver*;
* анализ визуальных результатов компиляции и влияние настроек beamer на внешний вид презентации.

Полученные результаты подтверждают гибкость и выразительные возможности класса **beamer**, а также демонстрируют типичный рабочий процесс при создании презентаций в LaTeX и настройке их оформления.
