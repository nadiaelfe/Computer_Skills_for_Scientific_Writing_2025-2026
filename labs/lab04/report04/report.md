
---
title: "Лабораторная работа 4"
author: "Надиа Эззакат"
date: "Включение графики в LaTeX"
lang: ru-RU
mainfont: Times New Roman
---

# Лабораторная работа 4: Включение графики в LaTeX
## Надиа Эззакат

---

# Цель работы
Научиться вставлять изображения в LaTeX-документы.

---

# 1. Подключение пакета graphicx

Для работы с графикой в LaTeX необходимо подключить пакет graphicx в преамбуле документа:

\usepackage{graphicx}

---

# 2. Вставка изображения

Для вставки изображения используется команда \includegraphics:

```latex
\includegraphics{example-image}
```
**Параметры вставки:**

$$ \text{Ширина} = \text{исходная ширина} $$
$$ \text{Высота} = \text{исходная высота} $$

---

# 3.Изменение размера изображения
Для изменения размера используются параметры width и height:

```latex
\includegraphics[width=5cm]{example-image}
\includegraphics[height=3cm]{example-image}
\includegraphics[width=0.5\textwidth]{example-image}
```
**Параметры изменения размеров:**

$$ w = 5\text{ cm} $$

$$ h = 3\text{ cm} $$

$$ w = 0.5 \times \text{\textwidth} $$

---

# 4.Поворот и масштабирование

Для поворота и масштабирования используются параметры angle и scale:

```latex
\includegraphics[angle=45, width=3cm]{example-image}
\includegraphics[scale=2, width=3cm]{example-image}
```
**Параметры преобразований:**

$$ \theta = 45^\circ $$

$$ k = 2 $$

$$ \text{Масштаб} = \frac{\text{новый размер}}{\text{исходный размер}} $$

---

# 5. Обрезка изображения

Для обрезки используются параметры trim и clip:

```latex
\includegraphics[trim=1cm 1cm 1cm 1cm, clip, width=3cm]{example-image}
```
**Обрезка задается отступами:**
$$ \text{trim} = (1\text{ cm},\ 1\text{ cm},\ 1\text{ cm},\ 1\text{ cm}) $$


---

# 6. Плавающие фигуры

Для создания плавающих фигур используется среда figure:

```latex
\begin{figure}[htbp]
    \centering
    \includegraphics[width=0.6\textwidth]{example-image}
    \caption{Пример плавающей фигуры}
    \label{fig:example}
\end{figure}
```

**Параметры позиционирования:**

$$ P \in \{h,\ t,\ b,\ p\} $$

---

# 7. Перекрестные ссылки

LaTeX поддерживает различные форматы:

| Формат | Расширение | Применение |
|--------|------------|------------|
| PDF | .pdf | Векторная графика |
| PNG | .png | Растровая графика |
| JPG | .jpg | Фотографии |
| EPS | .eps | Старая векторная графика |

---

# Выводы
В ходе лабораторной работы были изучены основные возможности пакета graphicx для работы с графикой в LaTeX. Освоены различные способы вставки изображений, изменения их размера, поворота и обрезки

---

# Спасибо за внимание!
