---
# Front matter
lang: ru-RU
title: "Лабораторная работа №2"
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

Познакомиться со структурой LaTeX-документа и созданием простых документов.

# Задание

1. Изучить структуру LaTeX-документа

2. Создать простой документ с базовыми элементами

3. Освоить основные команды и окружения LaTeX


# Выполнение лабораторной работы

В этой лабораторной работе мы изучаем основы работы с математическими формулами в LaTeX.

\subsection{Формулы в тексте}

Внутри текста математические формулы оформляются с использованием символов $. Например, формула $E = mc^2$ является одной из самых известных в физике.

\subsection{Выключные формулы}

Для более сложных формул используются выключные формулы:

$$E = mc^2$$

Или с использованием среды equation:

\begin{equation}
F = G\frac{m_1 m_2}{r^2}
\end{equation}

\subsection{Степени и индексы}

Степени и индексы оформляются с помощью символов ^ и _:

$$x^2 + y^2 = z^2$$

$$a_1 + a_2 + a_3 = S$$

$$e^{i\pi} + 1 = 0$$

\subsection{Дроби и корни}

Для создания дробей используется команда \frac:

$$\frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

Квадратный корень оформляется командой \sqrt:

$$\sqrt{2} \approx 1.414$$

\subsection{Греческие буквы}

В математических формулах часто используются греческие буквы:

$$\alpha + \beta = \gamma$$

$$\sin^2 \alpha + \cos^2 \alpha = 1$$


\subsection{Системы уравнений}

Для оформления систем уравнений используется среда cases:

$$
f(x) = 
\begin{cases}
x^2 & \text{при } x \geq 0 \\
-x & \text{при } x < 0
\end{cases}
$$

\subsection{Многострочные формулы}

Для многострочных формул используется среда align:

\begin{align}
(x+y)^2 &= x^2 + 2xy + y^2 \\
(x-y)^2 &= x^2 - 2xy + y^2
\end{align}


# Выводы

В ходе лабораторной работы была изучена структура LaTeX-документа и освоены основные принципы создания документов. Были получены практические навыки работы с разделами, подразделами и базовым форматированием текста. Созданный документ успешно скомпилирован в PDF-формат.
