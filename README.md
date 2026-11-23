# Лабораторная работа №6
## Система контроля версий
**Выполнил:** 4541в Шабуров И.А.

## Ход работы
### 1. Настройка Git
![Настройка git](screenshots/01_config.jpg)

### 2. Клонирование репозитория

### 3. Подтягивание изменений
![Подтягивание](screenshots/03_changes.jpg)

### 4. История веток
![Ветка master](screenshots/04_master.jpg)
![Ветка feature](screenshots/04_feature.jpg)
![Общий вид](screenshots/04_general.jpg)

### 5. Последние изменения
![Изменения](screenshots/05_recently.jpg)
![Различие ветвей](screenshots/05_diff.jpg)

### 6. Слияние с разрешением конфликта
![Слияние](screenshots/06_merge.jpg)
![Разрешение](screenshots/06_access.jpg)

### 7. Удаление побочной ветки
![Удаление](screenshots/07_delete.jpg)

### 8. Создание коммитов
![Создание первого](screenshots/08_commit1.jpg)
![Создание второго](screenshots/08_commit2.jpg)
![Создание третьего](screenshots/08_commit3.jpg)

### 9. Откат коммита
![откат](screenshots/09_backup.jpg)

### 10. Ветка для отчета
![создание](screenshots/10_branch.jpg)

## Лог команд
```bash
git config --global user.name "4541В Шабуров И.А."
git config --global user.email "shaburashka24@gmail.com"
git config --list
git clone https://github.com/SL1GHTLY52/LR6.git
cd LR6
git pull
git branch -a
git log master
git checkout -b feature
echo "строка для ветки feature" >> test.txt
git add test.txt
git commit -m "в ветке feature изменен test.txt"
git checkout master
echo "строка для ветки master" >> test.txt
git add test.txt
git commit -m "в ветке master изменен test.txt"
git log master
git log feature
git log --oneline --graph --all
git show
git diff master feature
git checkout master
git merge feature
git mergetool test.txt
notepad test.txt
git add test.txt
git commit -m "слияние feature в ветку master, разрешен конфликт в test.txt"
git log --oneline --graph --all
git branch -d feature
git branch -a
echo "файл с именами студентов" > names.txt
git add names.txt
git commit -m "добавлен файл для имен студентов names.txt"
echo "файл с датами рождения студентов" > birthday.txt
git add birthday.txt
git commit -m "добавлен файл для дат рождений студентов birthday.txt"
echo "Шабуров Иван Александрович" >> names.txt
git add names.txt
git commit -m "в файл names.txt добавлен новый студент"
git log --oneline
git revert HEAD
git checkout -b report
mkdir screenshots
cp "/e/фото лабы"/* screenshots/
git status
git add README.md screenshots/
git commit -m "Добавленые первые 5 пунктов отчета и соответствующие скриншоты"
пше ыефегы
git status
cp "/e/фото лабы"/* screenshots/
git add README.md screenshots/
git commit -m "Добавленые следующие 5 пунктов отчета и соответствующие скриншоты"
git status
git add README.md
git commit -m "Добавлен Лог команд"
```