---
# Front matter
lang: ru-RU
title: "Дискреционное
разграничение прав в Linux. Расширенные атрибуты"
author: "Ндри Ив Алла Ролан"
group: NFIbd-02-20
date: 2023 Sep 29th

# Formatting
toc: false
slide_level: 2
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
theme: metropolis

---

# Результат выполнения лабораторной работы №4

# Цель работы

Получение практических навыков работы в консоли с расширенными
атрибутами файлов


## Результат выполнения лабораторной работы

### От имени пользователя guest определите расширенные атрибуты файла

От имени пользователя guest определите расширенные атрибуты файла
/home/guest/dir1/file1 командой
lsattr /home/guest/dir1/file1
/home/guest/dir1/file1 командой
lsattr /home/guest/dir1/file1 

![1](1.png)



## Результат выполнения лабораторной работы

### Установите командой 
chmod 600 file1
на файл file1 права, разрешающие чтение и запись для владельца файла.

![2](3.png)


## Результат выполнения лабораторной работы

### Попробуйте установить на файл /home/guest/dir1/file1 расширенный атрибут a от имени пользователя guest:

Попробуйте установить на файл /home/guest/dir1/file1 расширенный атрибут a от имени пользователя guest:
chattr +a /home/guest/dir1/file1

![3](4.png)



## Результат выполнения лабораторной работы

### 4 and 5 

Зайдите на третью консоль с правами администратора либо повысьте
свои права с помощью команды su. Попробуйте установить расширенный атрибут a на файл /home/guest/dir1/file1 от имени суперпользователя:
chattr +a /home/guest/dir1/file1
От пользователя guest проверьте правильность установления атрибута:
lsattr /home/guest/dir1/file1

![4](4.png)
![5](5.png)


## Результат выполнения лабораторной работы

###  6 , 7 ,8 

Выполните дозапись в файл file1 слова «test» командой
echo "test" /home/guest/dir1/file1
После этого выполните чтение файла file1 командой
cat /home/guest/dir1/file1
Убедитесь, что слово test было успешно записано в file1.
 Попробуйте удалить файл file1 либо стереть имеющуюся в нём информацию командой
echo "abcd" > /home/guest/dirl/file1
Попробуйте переименовать файл.
 Попробуйте с помощью команды chmod 000 file1
установить на файл file1 права, например, запрещающие чтение и запись для владельца файла. Удалось ли вам успешно выполнить указанные команды?

![6,7,8](6_7_8.png)

## Результат выполнения лабораторной работы

### 9, 10 

Снимите расширенный атрибут a с файла /home/guest/dirl/file1 от
имени суперпользователя командой
chattr -a /home/guest/dir1/file1
Повторите операции, которые вам ранее не удавалось выполнить. Ваши
наблюдения занесите в отчёт.
Повторите ваши действия по шагам, заменив атрибут «a» атрибутом «i».
Удалось ли вам дозаписать информацию в файл? Ваши наблюдения занесите в отчёт.

![9](9_10.png)
![10](10_2.png)


## Вывод 

В ходе работы мы получили практических навыков работы в консоли с расширенными атрибутами файлов