# Работа с репозиторием
<div align="center">
 <img src="https://spark.ru/upload/blogs_covers/n_6346f1fc73228.jpg" width="530px">
</div>

---

Сегодня мы узнаем о том, что "Как создать и работать с репозиторием?". 

Работа с репозиторием обычно включает несколько основных шагов: 

- создание репозитория 
- клонирование 
- добавление и коммит изменений 
- работа с удалёнными репозиториями 

Вот несколько базовых команд для работы с репозиторием Git: 

Для создания пустого репозитория на локальном компьютере, нам нужно прописать в Git эту команду:
```
git init
```
Создаётся пустой репозиторий. После того как вы изменили файлы в репозитории, их нужно добавить в индекс:
```
git add ваш_файл
```
Если вы хотите добавить все файлы в репозитории, пишем эту команду:
```
git add . 
```
# Создание коммита
После добавления файлов в индекс, нужно зафиксировать изменения (создать коммит):
```
git commit -m "Описание изменений"
```
# Отправка изменений на удалённый репозиторий
Чтобы отправить изменения в удалённый репозиторий:
```
git push origin main
```
Здесь origin — это имя удалённого репозитория (по умолчанию), а main — это ветка, в которую вы отправляете изменения.

# Получение изменений из удалённого репозитория
Если в удалённом репозитории были сделаны изменения, которые вы хотите получить, используйте команду:
```
git pull origin main
```
# Просмотр состояния репозитория
Чтобы увидеть, какие файлы были изменены и добавлены:
```
git status
```
# Просмотр истории коммитов
Чтобы увидеть историю коммитов:
```
git log
```
Если вы хотите работать в новой ветке:
```
git checkout -b new-branch
```
Чтобы переключиться на уже существующую ветку:
```
git checkout new-branch
```
# Что такое ветка?
<div align="center">
  <img src="https://i.ytimg.com/vi/pyJDBiRmFRw/maxresdefault.jpg" width="600px">
</div>

---

Ветка — это указатель на коммит.
Ветка main (или master) обычно является основной веткой, где хранится стабильная версия проекта.
Ветки позволяют изолировать изменения, а затем объединять их обратно в основную ветку.
Создание ветки
Чтобы создать новую ветку:
```
git branch имя-ветки
```
Пример:
```
git branch feature/login-form
```
# Просмотр веток
Чтобы увидеть список всех веток:
```
git branch
```
Ветки, которые существуют в репозитории, будут показаны списком.
Текущая ветка выделена звездочкой (*).
Пример вывода:
```
* main
  feature/login-form
```
# Переключение между ветками
Чтобы переключиться на существующую ветку:
```
git checkout имя-ветки
```
С версии Git 2.23 и выше можно использовать:
```
git switch имя-ветки
```
Пример:
```
git switch feature/login-form
```
# Создание и переход на новую ветку одновременно
Для создания ветки и одновременного перехода на неё:
```
git checkout -b имя-ветки
```
Или с новой командой:
```
git switch -c имя-ветки
```
# Слияние веток
Чтобы объединить изменения из одной ветки в другую:
```
git merge new-branch
```
# Удаление локальной ветки
Если вам больше не нужна ветка, можно её удалить:
```
git branch -d new-branch
```
# Удаление удалённой ветки
Чтобы удалить ветку на удалённом репозитории:
```
git push origin --delete new-branch
```
---

<div align="center">
  <img src="https://a.d-cd.net/fGkj61MC91njUbKjZUahzEm1-IA-960.jpg" width="600px" height="300px">
</div>
