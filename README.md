# Newman Reports

[🇬🇧 English](#english) | [🇷🇺 Русский](#russian)

---

## English {#english}

### Repository setup

1. Go to project root:
```bash
cd /path/to/Reports
````

2. Initialize git (if not done yet):

```bash
git init
```

3. Ignore macOS system files:

```bash
echo ".DS_Store" >> .gitignore
git add .gitignore
git commit -m "Ignore macOS system files"
```

4. Create `.nojekyll` for the docs folder:

```bash
touch docs/.nojekyll
```

5. Add docs folder with HTML reports:

```bash
git add docs
git commit -m "Add docs folder with HTML reports and disable Jekyll"
```

6. Connect remote repository (SSH):

```bash
git remote add origin <YOUR_GIT_SSH_URL>
git branch -M main
git push -u origin main
```

---

### Adding new files

1. Copy new HTML report to docs folder:

```bash
cp /path/to/new/report.html docs/
```

2. Add file to git:

```bash
git add docs/<new-file-name>.html
```

3. Commit changes:

```bash
git commit -m "Add new HTML report"
```

4. Push to GitHub:

```bash
git push
```

5. Link to the report after Pages update:

```
https://<YOUR_GITHUB_USERNAME>.github.io/<REPO_NAME>/<new-file-name>.html
```

---

### Useful Git commands

* Check status:

```bash
git status
```

* Add all changes:

```bash
git add .
```

* Commit changes:

```bash
git commit -m "Commit message"
```

* Push changes:

```bash
git push
```

---

### Branching

#### Create new branch and switch to it

```bash
git checkout -b <branch-name>
```

#### Add changes and commit on new branch

```bash
git add .
git commit -m "Description of changes on new branch"
```

#### Push branch to GitHub

```bash
git push -u origin <branch-name>
```

#### Merge branch into main (after review)

```bash
git checkout main
git merge <branch-name>
git push
```

---

## Russian {#russian}

### Настройка репозитория

1. Перейти в корень проекта:

```bash
cd /путь/к/Reports
```

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

### Добавление новых файлов

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

### Полезные команды Git

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

---

### Работа с ветками

#### Создание новой ветки и переключение на неё

```bash
git checkout -b <название-ветки>
```

#### Добавление изменений и коммит на новой ветке

```bash
git add .
git commit -m "Описание изменений на новой ветке"
```

#### Отправка ветки на GitHub

```bash
git push -u origin <название-ветки>
```

#### Слияние ветки с main (после проверки изменений)

```bash
git checkout main
git merge <название-ветки>
git push
```