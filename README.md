## Настройка репозитория

1. Перейти в корень проекта:
```bash
cd /путь/к/Reports
````

2. Инициализация git (если ещё не сделано):

```bash
git init
```

3. Игнорирование системных файлов macOS:

```bash
echo ".DS_Store" >> .gitignore
git add .gitignore
git commit -m "Ignore macOS system files"
```

4. Создание файла `.nojekyll` для папки `docs`:

```bash
touch docs/.nojekyll
```

5. Добавление папки `docs` с HTML-отчётами:

```bash
git add docs
git commit -m "Add docs folder with HTML reports and disable Jekyll"
```

6. Подключение удалённого репозитория (SSH):

```bash
git remote add origin <YOUR_GIT_SSH_URL>
git branch -M main
git push -u origin main
```

---

## Добавление новых файлов

1. Копируем новый HTML-отчёт в папку `docs`:

```bash
cp /путь/к/новому/отчету.html docs/
```

2. Добавляем файл в git:

```bash
git add docs/имя_нового_файла.html
```

3. Коммитим изменения:

```bash
git commit -m "Add new HTML report"
```

4. Пушим на GitHub:

```bash
git push
```

5. Ссылка на новый отчёт после обновления Pages:

```
https://<YOUR_GITHUB_USERNAME>.github.io/<REPO_NAME>/имя_нового_файла.html
```

---

## Полезные команды Git

* Проверка статуса:

```bash
git status
```

* Добавление всех изменений:

```bash
git add .
```

* Создание коммита:

```bash
git commit -m "Сообщение коммита"
```

* Пуш изменений на GitHub:

```bash
git push
```

## Работа с ветками

### Создание новой ветки и переключение на неё

```bash
# Создать новую ветку и сразу переключиться на неё
git checkout -b <название-ветки>
````

### Добавление изменений и коммит на новой ветке

```bash
# Добавить все изменения
git add .

# Создать коммит с описанием
git commit -m "Описание изменений на новой ветке"
```

### Отправка ветки на GitHub

```bash
# Отправить ветку на удалённый репозиторий и установить upstream
git push -u origin <название-ветки>
```

### Слияние ветки с main (после проверки изменений)

```bash
# Переключиться на main
git checkout main

# Слить изменения с вашей ветки
git merge <название-ветки>

# Отправить изменения на GitHub
git push
```