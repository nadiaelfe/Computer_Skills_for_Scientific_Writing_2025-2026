# Lab 06 Report: Bibliography in LaTeX
**Nadia Ezzakate** | March 13, 2026

## Цель работы

Изучить основы работы с библиографией в LaTeX, освоить создание BibTeX-файлов и использование различных команд цитирования.

## Задание

1. Создать BibTeX файл с библиографическими источниками
2. Использовать пакет natbib для цитирования
3. Изучить команды `\citet` и `\citep`
4. Освоить многоэтапный процесс компиляции документов с библиографией
5. Получить автоматически отформатированный список литературы

## Выполнение лабораторной работы

### 1. Подключение пакета natbib

Для работы с библиографией в LaTeX я подключила пакет natbib в преамбуле документа.

### 2. Создание BibTeX-файла

Я создала файл `references.bib` с тремя библиографическими записями:

- Книга Дональда Кнута "The TeXbook" (1984)
- Книга Лесли Лэмпорта "LaTeX: A Document Preparation System" (1994)
- Книга Гуссенса и др. "The LaTeX Companion" (1993)

Структура BibTeX записи может быть представлена как:

$$ \text{Запись} = \text{@тип}\{\text{ключ}, \text{поля}\} $$

### 3. Создание основного документа

Я создала файл `lab06.tex`, в котором использовала различные команды цитирования.

### 4. Процесс компиляции

Я освоила многоэтапный процесс компиляции документа с библиографией:

$$ \text{pdflatex} \rightarrow \text{bibtex} \rightarrow \text{pdflatex} \rightarrow \text{pdflatex} $$

На первом запуске `pdflatex` создается `.aux` файл с информацией о цитированиях. Затем `bibtex` обрабатывает этот файл и создает `.bbl` файл с отформатированной библиографией. Последующие два запуска `pdflatex` включают библиографию в документ и разрешают все ссылки.

### 5. Команды цитирования

Я изучила различные команды цитирования:

**Текстовое цитирование (`\citet`):**

$$ \text{\citet\{ключ\}} \rightarrow \text{Автор (год)} $$

**Цитирование в скобках (`\citep`):**

$$ \text{\citep\{ключ\}} \rightarrow \text{(Автор, год)} $$

**Цитирование с номером страницы:**

$$ \text{\citep[p.~42]\{ключ\}} \rightarrow \text{(Автор, год, стр. 42)} $$

**Множественное цитирование:**

$$ \text{\citep\{ключ1, ключ2\}} \rightarrow \text{(Автор1, год; Автор2, год)} $$

### 6. Стили библиографии

Я использовала стиль `plainnat`, который автоматически сортирует ссылки в алфавитном порядке:

$$ \text{Список литературы} = \text{сортировка}(\{\text{источник}_1, \text{источник}_2, \ldots, \text{источник}_n\}) $$

## Выводы

В ходе выполнения лабораторной работы я научилась:

1. **Создавать BibTeX-файлы** с библиографическими источниками:

$$ \text{references.bib} = \{\text{knuth1984}, \text{lamport1994}, \text{goossens1993}\} $$

2. **Использовать различные команды цитирования** в пакете natbib:

$$ \text{Команды} = \{\text{\citet}, \text{\citep}\} $$

3. **Понимать многоэтапный процесс компиляции** библиографии:

$$ \text{Документ} = \text{pdflatex} + \text{bibtex} + \text{pdflatex} + \text{pdflatex} $$

4. **Автоматически форматировать список литературы**:

$$ \forall i,j: \text{формат}(\text{ref}_i) = \text{формат}(\text{ref}_j) $$

Система библиографии в LaTeX значительно экономит время и обеспечивает единообразное форматирование ссылок, что особенно важно при написании научных статей и курсовых работ.
## Citation Commands

| Command | Result |
|---------|--------|
| `\citet{knuth1984}` | Textual citation: Knuth (1984) |
| `\citep{lamport1994}` | Parenthetical citation: (Lamport, 1994) |
| `\citep[p.~42]{knuth1984}` | Citation with page number: (Knuth, 1984, p. 42) |
| `\citep{knuth1984,lamport1994}` | Multiple citations: (Knuth, 1984; Lamport, 1994) |


## Conclusion
In this lab, I learned:
- How to create a .bib file with references
- Different citation commands in natbib
- The multi-step compilation process for bibliography
- How LaTeX automatically formats references

The bibliography system in LaTeX saves time and ensures consistent formatting of references.

