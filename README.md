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

EOF

# Создание файла .nojekyll в папке docs

touch docs/.nojekyll

# Добавляем README.md и docs в git

git add README.md docs

# Коммитим изменения

git commit -m "Add README and .nojekyll for GitHub Pages"

# Пушим в удалённый репозиторий

git push

```
