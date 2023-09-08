---
# Front matter
title: "Отчет по лабораторной работе №1"
subtitle: "лабораторной работы №1. Установка и конфигурация
операционной системы на виртуальную машину"
author: "Ндри Ив Алла Ролан"
group: NFIbd-02-20
date: 2023 Sep 9th

# Generic otions
lang: ru-RU
toc-title: "Содержание"

# Pdf output format
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
### Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Misc options
indent: true
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

Целью данной работы является приобретение практических навыков
установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

## Результат выполнения лабораторной работы

![Окно «Свойства» VirtualBox](2.png)

## Результат выполнения лабораторной работы

### Окно «Носители» виртуальной машины: подключение образа оптического диска
![1](1.png)

## Запуск виртуальной машины

![Окно «Размер основной памяти»](4.png)

### Установка английского языка интерфейса ОС

![7](7.png)

### РОкно настройки установки образа ОС

![16](14.png)

### Окно настройки установки: место установки

![8.1](8.1.png)

### Установка пароля для root

![Окно настройки установки: отключение KDUMP](8.png)

### Первоначальная настройка ОС:переход к лицензии

![Окно настройки установки: место установки](17.png)

### centos теперь установлен

![Окно настройки установки: сеть и имя узла](15.png)

### Запуск образа диска дополнений гостевой ОС

![Установка пароля для root](13.png)

## Вывод 

В ходе работы были получены практические навыки
установки операционной системы на виртуальную машину, настройки минимально необходимых для выполнения работы сервисов.

# Список литературы

1. Методические материалы курса