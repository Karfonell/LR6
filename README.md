# LR6
## Лабораторная работа №6

**Цель работы:** изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.
<br>**Ход работы:**
<br>На Гитхаб уже был создан аккаунт, поэтому был сделан форк [репозитория](https://github.com/Kurtyanik/LR6/).

Затем текущая директория изменяется на специальную папку для лабораторной работы
```
cd '/c/Users/Anna/Desktop/уник/лабы и тесты и другая теоретическая/Информатика/для лаб6'
```
Затем клонируется удаленный репозиторий на локальный компьютер
```
git clone https://github.com/Karfonell/LR6
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/1.jpg)
<br>На гитхаб создается новый файл<br>
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/2.jpg)
<br>В консоли происходит переход в репозиторий и подгрузка всех изменений<br>
```
cd LR6
git pull
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/3.jpg)
<br>Получается история операций по каждой из веток в графическом виде<br>
```
git log --oneline --graph --all
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/4.jpg)
<br>Просматриваются последние 8 коммитов<br>
```
git log -n 8
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/5.jpg)
<br>Переключение на ветку master и слияние с ней ветки branch1
```
git checkout master
git merge origin/branch1
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/6.jpg)
<br> Случается конфликт. Он решается при помощи удаления из файла ветки branch1 информации, противоречащей основной ветке. После этого файлы сливаются.<br>
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/7.jpg)<br>
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/8.jpg)
<br>Создается коммит с информацией о том, что конфликт разрешен
```
git add mergefile.txt
git commit -m "Разрешение конфликта"
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/9.jpg)
<br>Удаляется ветка branch1, создается коммит с информацией об этом
```
git branch
git branch -d branch1
```
```
git add .
git commit "Слияние в одну ветку и удаление ненужной"
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/10.jpg)
<br>В папке создается файл *changes.txt*, создается коммит об этом
```
git add changes.txt
git commit -m "Создание файла"
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/11.jpg)
<br>Производится первое изменение в файле, после него происходит коммит. Затем аналогичные действия повторяются после второго изменения
```
git add changes.txt
git commit -m "Первое изменение в changes.txt"
git add changes.txt
git commit -m "Второе изменение в changes.txt"
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/13.jpg)<br>
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/12.jpg)
<br>Происходит удаление последнего коммита со вторым изменением в файле
```
git reset --hard HEAD^
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/14.jpg)
<br>Создается новая ветка для отчета - report
```
git switch -s report
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/15.jpg)
<br>Создается файл readme.md
```
touch readme.md
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/16.jpg)
<br>В файл вносится информация по заданию, периодически делаются коммиты
```
git add .
git commit -m "Сделан лог команд до удаления ветки включительно"
git add .
git commit -m "Сделан лог команд до создания ветки для отчета включительно"
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/17.jpg)
<br>Получается история операций в форматированном виде
```
git log --pretty=format:"%h - %ad | %an | %s" --date=short
```
![](https://github.com/Karfonell/LR6/blob/report/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D1%8B/18.jpg)

**Вывод:** Я изученла базовые возможности системы управления версиями и получила опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.
