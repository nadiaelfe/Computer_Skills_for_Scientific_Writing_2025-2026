---
# Front matter
lang: ru-RU
title: "Лабораторная работа №8"
subtitle: "Работа с графикой в LaTeX"
author: "НАДИА ЭЗЗАКАТ"
institute: "РУДН, Москва, Россия"
date: "2026"

# Formatting
pdf-engine: lualatex
header-includes:
  - \usepackage{tikz}
  - \usetikzlibrary{math,calc,arrows.meta}
  - \usepackage{polyglossia}
  - \setmainlanguage{russian}
  - \setotherlanguage{english}
  - \newfontfamily\russianfont{DejaVu Serif}
  - \newfontfamily\russianfontsf{DejaVu Sans}
  - \newfontfamily\russianfonttt{DejaVu Sans Mono}
---

# Цель работы

Освоить работу с графикой в LaTeX с использованием пакета TikZ: создание диаграмм, графиков, кривых и фракталов.

# Задание

1. Набрать граф, подобный изображенному в упражнении 1.
2. Набрать график, подобный изображенному в упражнении 2.
3. Адаптировать код Sierpiński's triangle для создания Sierpiński's carpet.

# Теоретическое введение

TikZ — это мощный пакет для создания графики непосредственно в документах LaTeX. 

Основные элементы:
- `\node` для создания узлов
- `\draw` для рисования линий
- `\plot` для построения графиков функций

# Граф для упражнения 1

\begin{center}
\scalebox{0.6}{
\input{Task1.tex}
}
\end{center}

Граф с использованием полярных координат и различных стилей линий.

# График для упражнения 2

\begin{center}
\scalebox{0.6}{
\input{Task2.tex}
}
\end{center}

График функций $y = \ln(x)$ и $y = e^x$ с осями координат.

# Ковер Серпинского для упражнения 3

\begin{center}
\scalebox{0.5}{
\input{Task3.tex}
}
\end{center}
Фрактал "Ковер Серпинского", созданный с помощью рекурсивной функции.

# Выводы

В ходе лабораторной работы были освоены:

- Создание графов в TikZ
- Построение графиков функций
- Работа с рекурсией для создания фракталов
