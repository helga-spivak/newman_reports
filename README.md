````markdown
# Newman Reports

<style>
.tab { overflow: hidden; border-bottom: 1px solid #ccc; margin-bottom: 10px; }
.tab button { background-color: #f1f1f1; float: left; border: none; outline: none; cursor: pointer; padding: 8px 16px; transition: 0.3s; font-size: 14px; }
.tab button.active { background-color: #ddd; font-weight: bold; }
.tabcontent { display: none; padding: 10px 0px; border-top: none; }
</style>

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'English')">🇬🇧 English</button>
  <button class="tablinks" onclick="openTab(event, 'Russian')">🇷🇺 Русский</button>
</div>

<div id="English" class="tabcontent" style="display:block;">
## Repository setup

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

### Adding new files

```bash
cp /path/to/new/report.html docs/
git add docs/<new-file-name>.html
git commit -m "Add new HTML report"
git push
```

### Useful Git commands

```bash
git status
git add .
git commit -m "Commit message"
git push
```

### Branching

```bash
git checkout -b <branch-name>
git add .
git commit -m "Description of changes on new branch"
git push -u origin <branch-name>
git checkout main
git merge <branch-name>
git push
```

</div>

<div id="Russian" class="tabcontent">
## Настройка репозитория

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

### Добавление новых файлов

```bash
cp /путь/к/новому/отчету.html docs/
git add docs/имя_нового_файла.html
git commit -m "Add new HTML report"
git push
```

### Полезные команды Git

```bash
git status
git add .
git commit -m "Сообщение коммита"
git push
```

### Работа с ветками

```bash
git checkout -b <название-ветки>
git add .
git commit -m "Описание изменений на новой ветке"
git push -u origin <название-ветки>
git checkout main
git merge <название-ветки>
git push
```

</div>

<script>
function openTab(evt, tabName) {
  var i, tabcontent, tablinks;
  tabcontent = document.getElementsByClassName("tabcontent");
  for (i = 0; i < tabcontent.length; i++) { tabcontent[i].style.display = "none"; }
  tablinks = document.getElementsByClassName("tablinks");
  for (i = 0; i < tablinks.length; i++) { tablinks[i].className = tablinks[i].className.replace(" active", ""); }
  document.getElementById(tabName).style.display = "block";
  evt.currentTarget.className += " active";
}
</script>
