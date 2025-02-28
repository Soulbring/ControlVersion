![](https://github.githubassets.com/assets/git-commit-199ab3f3f652.png)
## Основные понятия
•   Репозиторий (Repository): Хранилище проекта, включающее все файлы и историю изменений.

•   Коммит (Commit): Зафиксированные изменения, которые сохраняются в истории репозитория.

•   Ветка (Branch): Независимая линия разработки. Основная ветка по умолчанию называется main или master.

•   Удалённый репозиторий (Remote repository): Репозиторий, размещенный на сервере, например, на GitHub или GitLab.

•   Слияние (Merge): Объединение изменений из одной ветки в другую.

## Установка Git
1.	Windows: Скачайте и установите Git для Windows.
2.	MacOS: Введите команду в терминале:

    brew install git

3.	Linux: Введите команду в терминале:

    sudo apt-get install git

## Настройка Git
После установки необходимо настроить Git:

    git config --global user.name "Ваше Имя"
    git config --global user.email "ваш_email@example.com"
# Создание репозитория
## Создание нового репозитория
1.	Перейдите в папку вашего проекта:
    cd путь/к/проекту
2.	Инициализируйте новый репозиторий:
    git init
3. Клонирование существующего репозитория

    git clone URL_репозитория
# Основные команды
## Статус
 Проверка состояния репозитория:

    git status
# Добавление изменений
## Добавление файлов в индекс (стадия для коммита):
    git add имя_файла
## Добавление всех изменений:
    git add .
# Коммит изменений
## Создание коммита:
    git commit -m "Описание изменений"
## Просмотр истории коммитов
    git log
# Ветки
## Создание новой ветки:
    git branch имя_ветки
## Переключение на другую ветку:
    git checkout имя_ветки
## Создание новой ветки и переключение на нее:
    git checkout -b имя_ветки
# Слияние веток
## Переключитесь на ветку, в которую хотите слить изменения, например main:
    git checkout main
## Слейте нужную ветку:
    git merge имя_ветки
# Удалённые репозитории
## Добавление удалённого репозитория:
    git remote add origin URL_репозитория
## Отправка изменений в удалённый репозиторий:
    git push origin имя_ветки
## Получение изменений из удалённого репозитория:
    git pull origin имя_ветки
# Удаление ветки
## Удаление локальной ветки:
    git branch -d имя_ветки
## Удаление удалённой ветки:
    git push origin --delete имя_ветки
# Создание запроса на вытягивание

Чтобы создать запрос на вытягивание, используйте подкоманду gh pr create

    gh pr create
Чтобы назначить запрос на вытягивание отдельному пользователю, используйте флаги --assignee или -a. Можно использовать @me для назначения запроса на вытягивание самому себе.

    gh pr create --assignee "@octocat"
Чтобы указать ветвь, в которую требуется объединить запрос на вытягивание, используйте флаги --base или -B. Чтобы указать ветвь, содержащую фиксации для запроса на вытягивание, используйте флаги   --head или -H.

    gh pr create --base my-base-branch --head my-changed-branch
Чтобы включить заголовок и текст нового запроса на вытягивание, используйте флаги --title и --body.

    gh pr create --title "The bug is fixed" --body "Everything works again"
Чтобы пометить запрос на вытягивание как черновик, используйте флаг --draft.

    gh pr create --draft
Чтобы добавить метки или вехи в новый запрос на вытягивание, используйте флаги --label и --milestone.

    gh pr create --label "bug,help wanted" --milestone octocat-milestone
Чтобы добавить новый запрос на вытягивание в конкретный проект, используйте флаг --project.

    gh pr create --project octocat-project
Чтобы назначить отдельного пользователя или команду в качестве рецензентов, используйте флаг --reviewer.

    gh pr create --reviewer monalisa,hubot  --reviewer myorg/team-name
Чтобы создать запрос на вытягивание в веб-браузере по умолчанию, используйте флаг --web.

    gh pr create --web
# Примеры использования
### Создание нового проекта
1.	Создаёт папку и переходит в нее:
    mkdir my_project
    cd my_project
2.	Инициализирует репозиторий:
    git init
3.	Создаё файл и добавляет его в индекс:
    echo "Hello, Git!" > README.md
    git add README.md
4.	Создаёт коммит:
    git commit -m "Initial commit"
### Работа с существующим проектом
1.	Клонирует удаленный репозиторий репозиторий:
    git clone URL_репозитория
    cd имя_проекта
2.	Создаёт новую ветку и переключается на нее:
    git checkout -b новая_ветка
3.	После внесения изменения в файлы и добавляет их в индекс:
    git add измененный_файл
4.	Создание коммита:
    git commit -m "Описание изменений"
5.	Отправляет изменения в удалённый репозиторий:
    git push origin новая_ветка
### Слияние изменений
1.	Переключение на основную ветку:
    git checkout main
2.	Сливает изменения из другой ветки:
    git merge новая_ветка
3.	Отправляет изменения в удалённый репозиторий:
    git push origin main
## Решение конфликтов
При слиянии веток могут возникнуть конфликты. Git сообщит вам о файлах с конфликтами, и вы должны будете вручную разрешить эти конфликты, отредактировав соответствующие файлы.

Дополнительные команды

•	Просмотр разницы между коммитами или состояниями: git diff

•	Отмена изменений в рабочем каталоге: git checkout -- <файл>

•	Удаление изменений из индекса: git reset <файл>

•	Просмотр удаленных репозиториев: git remote -v

•	Добавление удаленного репозитория: git remote add <имя> 
