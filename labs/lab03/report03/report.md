---
# Front matter
lang: ru-RU
title: "Лабораторная работа №3"
subtitle: "Математический набор в LaTeX"
author: "Надиа Эззакат"

# Formatting
toc-title: "Содержание"
toc: true
toc_depth: 2
lof: true
lot: true
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
  - \linepenalty=10
  - \interlinepenalty=0
  - \hyphenpenalty=50
  - \exhyphenpenalty=50
  - \binoppenalty=700
  - \relpenalty=500
  - \clubpenalty=150
  - \widowpenalty=150
  - \displaywidowpenalty=50
  - \brokenpenalty=100
  - \predisplaypenalty=10000
  - \postdisplaypenalty=0
  - \floatingpenalty = 20000
  - \raggedbottom
  - \usepackage{float}
  - \floatplacement{figure}{H}
  - \usepackage{amsmath, amssymb, amsfonts}
  - \usepackage{bm}
---

# Цель работы

Освоить основные возможности LaTeX для набора математических формул, изучить различные режимы математического набора и научиться работать с пакетом amsmath.

# Задание

1. Изучить inline и display режимы математического набора
2. Освоить работу с индексами и степенями
3. Научиться набирать греческие буквы и математические функции
4. Изучить многострочные формулы с выравниванием
5. Освоить работу с матрицами
6. Изучить различные шрифты в математическом режиме
7. Научиться использовать жирный шрифт для математических символов

# Теоретическое введение

LaTeX предоставляет мощные возможности для набора математических формул. Основные понятия включают:

- **Математический режим** — специальное состояние LaTeX для набора формул
- **Inline математика** — формулы внутри текста (обозначается $...$)
- **Display математика** — выключные формулы (обозначается \[...\])

Пакет **amsmath** расширяет базовые возможности и предоставляет дополнительные окружения для многострочных формул, матриц и других математических конструкций.

# Выполнение лабораторной работы

## 1. Inline и Display математика
**Inline математика** (внутри текста) обрамляется одиночными знаками доллара:

Это пример inline математики: формула $E = mc^2$ находится прямо в тексте.
Еще пример: $x^2 + y^2 = z^2$ - теорема Пифагора.

**Display математика** (выключные формулы) создается с помощью двойных знаков доллара или квадратных скобок:

$$
E = mc^2
$$

Или с помощью \[ \]:

\[
x^2 + y^2 = z^2
\]

Сравнение:
- Inline: $\int_a^b f(x) \, dx$ - интеграл внутри текста
- Display: 
$$
\int_a^b f(x) \, dx
$$ - интеграл на отдельной строке

Многострочная display математика с выравниванием:

$$
\begin{aligned}
(x+y)^2 &= x^2 + 2xy + y^2 \\
(x-y)^2 &= x^2 - 2xy + y^2
\end{aligned}
$$


## 2. Индексы и степени
**Степени** создаются с помощью символа `^`:

- $x^2$ - икс в квадрате
- $x^{2y}$ - икс в степени 2y
- $e^{i\pi} + 1 = 0$ - формула Эйлера
- $(a+b)^2 = a^2 + 2ab + b^2$

**Индексы** создаются с помощью символа `_`:

- $x_1$ - икс с индексом 1
- $x_{ij}$ - икс с двойным индексом
- $a_1, a_2, \ldots, a_n$ - последовательность
- $x_{n+1} = x_n + d$ - рекуррентная формула

**Комбинация индексов и степеней**:

- $x_i^2$ - квадрат икса с индексом i
- $x^{2}_{i}$ - то же самое
- ${x_i}^2$ - икс с индексом i в квадрате (отличается расположением)
- $e^{x^2}$ - экспонента от икс в квадрате
- $\int_0^1 x^2 \, dx$ - интеграл с пределами



**Вложенные индексы и степени**:

- $x^{y^z}$ - степени башней
- $a_{b_c}$ - вложенные индексы
- $e^{x^2 + y^2}$ - сложная степень
- $R_{ij}^{kl}$ - тензорные обозначения

## 3. Греческие буквы


$$\Delta$$
$$\alpha$$ 
$$\beta$$ 
$$\gamma$$
$$\delta$$
$$\epsilon$$
$$\theta$$
$$\lambda$$
$$\pi$$
$$\rho$$
$$\sigma$$
$$\phi$$ 
$$\chi$$
$$\omega$$


## 4. Интегралы и суммы
$$
\int_{0}^{\infty} e^{-x^2} \, dx = \frac{\sqrt{\pi}}{2}
$$

$$
\sum_{k=1}^{\infty} \frac{1}{k^2} = \frac{\pi^2}{6}
$$

$$
\oint_C \vec{F} \cdot d\vec{r} = \iint_S (\nabla \times \vec{F}) \cdot d\vec{S}
$$

## 5. Многострочные формулы
Для многострочных формул используется окружение `align*` из пакета amsmath:

$$
\begin{align*}
(x+y)^2 &= x^2 + 2xy + y^2 \\
(x-y)^2 &= x^2 - 2xy + y^2 \\
(x+y)^3 &= x^3 + 3x^2y + 3xy^2 + y^3
\end{align*}
$$

Выравнивание по знаку равенства:

$$
\begin{align*}
f(x) &= x^2 + 2x + 1 \\
     &= (x+1)^2
\end{align*}
$$

Системы уравнений:

$$
\begin{cases}
x + y = 5 \\
2x - y = 4
\end{cases}
$$

## 6. Матрицы
Для создания матриц используются различные окружения:
**pmatrix** (круглые скобки):

⎛ 1  2  3 ⎞
⎜ 4  5  6 ⎟
⎝ 7  8  9 ⎠

**bmatrix** (квадратные скобки):

⎡ 1  2  3 ⎤
⎢ 4  5  6 ⎥
⎣ 7  8  9 ⎦

**vmatrix** (определитель):

| a  b |
| c  d | = ad - bc

**Матрица с многоточиями**:

⎛ a₁₁  a₁₂  ⋯  a₁ₙ ⎞
⎜ a₂₁  a₂₂  ⋯  a₂ₙ ⎟
⎜  ⋮    ⋮   ⋱   ⋮   ⎟
⎝ aₘ₁  aₘ₂  ⋯  aₘₙ ⎠

## 7. Различные шрифты в математике
В математическом режиме доступны различные шрифты:

- Прямой шрифт: $\mathrm{ABCabc123}$
- Полужирный: $\mathbf{ABCabc123}$
- Курсивный: $\mathit{ABCabc123}$
- Моноширинный: $\mathtt{ABCabc123}$
- Каллиграфический (только заглавные): $\mathcal{ABC}$
- Готический (только заглавные): $\mathfrak{ABCabc123}$
- Двойной (только заглавные): $\mathbb{ABC}$

Примеры использования:

$$
\mathrm{sin}^2 x + \mathrm{cos}^2 x = 1
$$

$$
\mathbf{A} = \begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

$$
\mathcal{L}\{f(t)\} = \int_0^\infty e^{-st} f(t) \, dt
$$

$$
\mathbb{R}, \mathbb{Z}, \mathbb{N}, \mathbb{Q}, \mathbb{C}
$$


# Выводы
В ходе выполнения лабораторной работы были изучены основные возможности LaTeX для математического набора:

- **Inline и display режимы** — для вставки формул внутри текста и в отдельные строки
- **Индексы и степени** — с помощью символов `_` и `^`
- **Греческие буквы** — команды вида `\alpha`, `\beta`, и т.д.
- **Математические функции** — `$\sin$`, `$\cos$`, `$\log$` и другие
- **Интегралы и суммы** — `$\int$`, `$\sum$`, `$\prod$`
- **Многострочные формулы** — окружение `align*` из пакета amsmath
- **Матрицы** — окружения `pmatrix`, `bmatrix`, `vmatrix`
- **Различные шрифты** — `$\mathrm$`, `$\mathbf$`, `$\mathit$`, `$\mathbb$`, `$\mathcal$`


Полученные навыки позволяют создавать профессионально оформленные математические документы любой сложности.
# Список литературы
Кулябов Д. С., Королькова А. В., Геворкян М. Н. Practical scientific writing. — 2024.

LaTeX documentation: https://www.latex-project.org/help/documentation/

AMS Math documentation: https://www.ams.org/publications/authors/tex/amslatex
