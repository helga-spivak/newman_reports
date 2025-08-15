# Newman Reports
## Language
- [English](#english)
- [Русский](#русский)

---

## English

### Repository Setup

1. Go to your project folder:
```bash
cd /path/to/Reports
````

2. Initialize git (if not already done):

```bash
git init
```

3. Ignore macOS system files:

```bash
echo ".DS_Store" >> .gitignore
git add .gitignore
git commit -m "Ignore macOS system files"
```

4. Create a `.nojekyll` file in `docs`:

```bash
touch docs/.nojekyll
```

5. Add the `docs` folder with HTML reports:

```bash
git add docs
git commit -m "Add docs folder with HTML reports and disable Jekyll"
```

6. Connect your SSH repository:

```bash
git remote add origin <YOUR_GIT_SSH_URL>
git branch -M main
git push -u origin main
```

7. Add new HTML reports:

```bash
cp /path/to/new/report.html docs/
git add docs/<report_filename>.html
git commit -m "Add new HTML report"
git push
```

**Link to the new report**:

```
https://<YOUR_GITHUB_USERNAME>.github.io/<REPO_NAME>/<report_filename>.html
```

---

## Русский

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

6. Подключение SSH репозитория:

```bash
git remote add origin <YOUR_GIT_SSH_URL>
git branch -M main
git push -u origin main
```

7. Добавление новых HTML-отчётов:

```bash
cp /путь/к/новому/отчету.html docs/
git add docs/<имя_нового_файла>.html
git commit -m "Add new HTML report"
git push
```

**Ссылка на новый отчёт**:

```
https://<YOUR_GITHUB_USERNAME>.github.io/<REPO_NAME>/<имя_нового_файла>.html
```
