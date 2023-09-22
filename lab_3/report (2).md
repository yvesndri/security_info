---
# Front matter
title: "Отчет по лабораторной работе №3"
subtitle: "лабораторной работы №3. Дискреционное
разграничение прав в Linux. Два пользователя"
author: "Ндри Ив Алла Ролан"
group: NFIbd-02-20
date: 2023 Sep 23th

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

#  Цель работы

Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей


## Результат выполнения лабораторной работы

### Создание учетной записи

В установленной операционной системе мы создали учетную запись гостевого пользователя (используя учетную запись администратора) :
useradd guest и Установили пароль для учетной записи гостевого пользователя (с использованием учетной записи администратора) :
passwd guest
![1](1_2.png)



## Результат выполнения лабораторной работы

### Аналогично создайте второго пользователя guest2.

![3](3.png)


## Результат выполнения лабораторной работы

### СДобавьте пользователя guest2 в группу guest:

Мы добавили пользователя guest2 в группу guest :
gpasswd -a guest2 guest

![4](4.png)



## Результат выполнения лабораторной работы

### Сравнение некоторых результатов работы командного интерпретатора 

Для обоих пользователей мы использовали команду pwd для определения каталога, в котором вы находитесь. Сравните ее с подсказками командной строки.
 Мы также определили имя пользователя, его группу, людей в ней и группы, к которым они принадлежат.
Мы также использовали команды groups guest и groups guest2, чтобы определить, к каким группам принадлежат пользователи guest и guest2. Наконец, мы сравнили вывод команды groups с выводом команд командной строки
id -Gn и id -G.

![6_7](6_7.png)


## Результат выполнения лабораторной работы

### рассмотрим содержимое group

мы сравнили полученную информацию с содержимым файла /etc/group.
Затем просмотрим этот файл с помощью команды
cat /etc/group

![8](8.png)

## Результат выполнения лабораторной работы

### использование команды newgrp guest

От имени пользователя guest2 мы зарегистрировали пользователя
guest2 в группе guest командой
newgrp guest

![9](9.png)


## Результат выполнения лабораторной работы

### использование командных chmod g+rwx , chmod 000 dir1

От имени пользователя guest мы изменили права доступа к каталогу /home/guest,
разрешив все действия пользователям из группы :
chmod g+rwx /home/guest
 как пользователь guest удаляем все атрибуты каталога /home/guest/dir1
из каталога /home/guest/dir1 с помощью команды
chmod 000 dir1. 
затем проверялась корректность удаления атрибутов.
Изменение атрибутов каталогов dir1 и file1 для учетной записи пользователя guest и проверка для учетной записи пользователя guest2

![10_11](10_11.png)



## Вывод 

В ходе работы мы получили практические навыки работы в консоли с атрибутами файлов для групп пользователей