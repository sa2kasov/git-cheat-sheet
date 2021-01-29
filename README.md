# Git Cheat Sheet
The most important and commonly used Git commands

---

Настройка конфигурации репозитория

```bash
git config
```

Статус текущего состояния Git

```bash
git status
```

Добавить `<file>` в индексированную stage область. Точка (.) в значении аргумента подставляет все файлы

```bash
git add <file>
```

Удалить файл `<file>` из staged-области

```bash
git rm --cached <file>
```

Сбросить `<file>` из stage области

```bash
git reset HEAD <file>
```

Коммит с последующим вводом комментария в файле

```bash
git commit
```

Коммит с одновременным ввод комментария

```bash
git commit -m "comment"
```

Обновляет последний коммит

```bash
git commit --amend
```

Обновление последнего коммита с сохранением предыдущего комментария

```bash
git commit --amend --no-edit
```

Отмена изменений в файле находящемся в не отслеживаемой области (untracked files)

```bash
git checkout -- <file>
```

Смена ветки на [branch_name]

```bash
git checkout [branch_name]
```

Лог коммитов

```bash
git log
```

Список веток

```bash
git branch
```

Создание копии текущей ветки с именем `<branch>` при этом текущая ветка остаётся активной

```bash
git branch <branch>
```

Подробный список веток с описаниями коммитов

```bash
git branch -v
```

Удалить ветку `<branch>`

```bash
git branch -D <branch>
```

Слияние веток [source_branch] с текущей

```bash
git merge [source_name]
```

Отмена слияния веток

```bash
git merge --abort
```

Сохранить изменения в хранилище stash

```bash
git stash
```

Извлечь изменения из временного хранилища (черновика, буфера обмена) для текущей ветки. Причем не важно в какой ветке ранее были помещены помещены данные в stash

```bash
git stash pop
```

Клонировать удалённый репозиторий

```bash
git clone [URL]
```

Добавить копию удалённого репозитория с именем [repo_name], находящийся по ссылке [URL]

```bash
git remote add [repo_name] [URL]
```

Информация об удалённых репозиториях

```bash
git remote -v
```

Удалить удалённый репозиторий [repo_name]

```bash
git remote remove [repo_name]
```

Получить данные с удалённого репозитория [repo_name]

```bash
git fetch [repo_name]
```

Выгрузка данных из локальной ветки [branch_name] на ветку [branch_name] удалённого репозитория [repo_name]

```bash
git push [repo_name] [branch_name]
```

Выгрузить данные локальной ветки [branch_name] на удалённый репозиторий [repo_name] в ветку под именем [remote_branch_name]

```bash
git push [repo_name] [branch_name]:[remote_branch_name]
```

Получить данные из локальной копии удалённого репозитория [repo_name] ветки [branch_name] в текущую активную ветку

```bash
git pull [repo_name] [branch_name]
```
