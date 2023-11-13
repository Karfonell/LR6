# LR6
Лабораторная работа №6

Лог команд:
cd '/c/Users/Anna/Desktop/уник/лабы и тесты и другая теоретическая/Информатика/для лаб6'
git clone https://github.com/Karfonell/LR6
cd LR6
git pull
git log --oneline --graph --all
git log -n 8
git checkout master
git merge origin/branch1
git branch -d origin/branch1
git add mergefile.txt
git commit -m "Разрешение конфликта"
git branch
git branch -d branch1
git add .
git commit "Слияние в одну ветку и удаление ненужной"
git add changes.txt
git commit -m "Создание файла"
git add changes.txt
git commit -m "Первое изменение в changes.txt"
git add changes.txt
git commit -m "Второе изменение в changes.txt"
git reset --hard HEAD^
git switch -s report