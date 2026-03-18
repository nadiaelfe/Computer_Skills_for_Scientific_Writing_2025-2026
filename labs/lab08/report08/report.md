---
# Front matter
lang: ru-RU
title: "Лабораторная работа №8"
subtitle: "Компьютерный практикум по научному письму"
author: "Надиа Эззакат"
institute: "РУДН"

# Formatting
toc: true
toc-depth: 2
numbersections: true
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: article
geometry: "left=2cm,right=2cm,top=2cm,bottom=2cm"
mainfont: "DejaVu Serif"
sansfont: "DejaVu Sans"
monofont: "DejaVu Sans Mono"
header-includes:
  - \usepackage{tikz}
  - \usetikzlibrary{math}
  - \usepackage{booktabs}
  - \usepackage{siunitx}
  - \usepackage{float}
  - \usepackage{fontspec}
  - \usepackage{polyglossia}
  - \setmainlanguage{russian}
  - \setotherlanguage{english}

# Bibliography settings
bibliography: references.bib
citeproc: true
reference-section-title: Библиография
nocite: |
  @*
---
\newpage

# Лабораторная работа №8
**Тема: Работа с графикой в LaTeX** 

\newpage

# Цель работы
Освоить работу с графикой в LaTeX: использование TikZ для создания графов, графиков функций и фракталов.

\newpage

# Задание

Выполнить упражнения из раздела 8.2:

1. Набрать граф, подобный изображенному в упражнении 1.
2. Набрать график, подобный изображенному в упражнении 2.
3. Адаптировать код Sierpiński's triangle для создания Sierpiński's carpet.

\newpage

# Выполнение работы

## 1. Построение графа
Был реализован направленный граф.

\begin{figure}[H]
    \centering
    \input{Task1.tex}
    \caption{Граф для упражнения 1}
    \label{fig-015}
\end{figure}

```
\begin{tikzpicture}
  \node[circle, draw, fill=green] (A) at (90:0) {A};
  \node[circle, draw, fill=yellow] (B) at (150:3) {B};
  \node[circle, draw, fill=yellow] (C) at (210:3.5) {C};
  \node[circle, draw, fill=yellow] (D) at (270:4) {D};
  \node[circle, draw, fill=green] (E) at (330:3.5) {E};
  \node[circle, draw, fill=green] (F) at (30:3) {F};
  \draw[->, red] (A) to[bend left=40] node[midway, above, sloped] {6} (B);
  \draw[->, dotted, blue] (A) to[bend right=50] node[midway, below, sloped] {2} (C);
  \draw[->, red] (A) to[bend left=50] node[midway, below, sloped] {4} (E);  
  \draw[->, red] (A) to[bend right=40] node[midway, above, sloped] {$\sqrt{2}$} (F);
  \draw[->, dotted, blue] (B) -- (C) node[midway, left, sloped] {$\sqrt{5}$};  
  \draw[->, red] (C) -- (D) node[midway, left] {11};
  \draw[->, dotted, blue] (D) -- (E) node[midway, below] {3};
  \draw[->, red] (E) -- (F) node[midway, right] {12};
\end{tikzpicture}
```
\newpage

## 2. Математический график
Построен график функций $y = \ln(x)$ и $y = e^x$.

\begin{figure}[H]
    \centering
    \input{Task2.tex}
    \caption{График функций для упражнения 2}
    \label{fig-016}
\end{figure}

```
\begin{tikzpicture}
  \draw[->] (-2,0) -- (3.2,0) node[right] {$x$};
  \draw[->] (0,-3) -- (0,3.1) node[above] {$y$};
  \node[below right] at (0,0) {O};
  \draw[blue, domain=0.1:3, smooth] plot (\x,{ln(\x)}) node[below right] {$y = \ln(x)$};
  \draw[blue, domain=-1:1.5, smooth] plot (\x,{exp(\x)}) node[above left] {$y = e^{x}$};
  \draw[black] (0,1) -- (0.1,1) node[left] {$y=1$};
  \draw[black] (1,0) -- (1,0.1) node[below] {$x=1$};
  \fill[black] (0,1) circle (1.5pt);  
  \fill[black] (1,0) circle (1.5pt);  
\end{tikzpicture}
```
\newpage

## 3. Фрактал (Ковер Серпинского)
Реализована генерация фрактала "Ковер Серпинского" с использованием рекурсии.

\begin{figure}[H]
    \centering
    \resizebox{\textwidth}{!}{%
    \input{Task3.tex}
    }
    \caption{Этапы построения ковра Серпинского}
    \label{fig-017}
\end{figure}

```
\begin{tikzpicture}
  \tikzmath{
    function carpet(\x, \y, \side, \depth) {
      if (\depth == 0) then {
        { \fill (\x,\y) rectangle ++(\side,\side); };
      } else {
        let \u = \side / 3;
        for \i in {0,1,2}{
          for \j in {0,1,2}{
            if !(\i==1 && \j==1) then {
              carpet(\x + \i*\u, \y + \j*\u, \u, \depth-1);
            };
          };
        };
      };
    };
    \S = 4;
    for \d in {0,1,2,3}{
      \px = (\S + 1) * \d;
      carpet(\px, 0, \S, \d);
    };
  }
\end{tikzpicture}
```
\newpage

# Выводы

В ходе лабораторной работы №8 были освоены следующие навыки:

1. **Создание графики в TikZ**: Линии, узлы, кривые и циклы.
2. **Построение графов**: С использованием полярных координат и меток.
3. **Построение графиков**: Функций с осями и пересечениями.
4. **Рекурсивные фигуры**: Адаптация кода для фракталов, как ковер Sierpiński.
5. **Эксперименты со стилями**: Цвета, стили линий, формы узлов.

Освоение TikZ в LaTeX важно для создания профессиональной графики в научных документах, позволяя генерировать сложные изображения программно.

\newpage

