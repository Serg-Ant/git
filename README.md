# Полезные команды Git

**Задача:** создать новую ветку и переключиться на нее.

**Команда:** `git checkout -b имя новой ветки`.
- `-b` - указывает, что необходимо создать новую ветку.

**Ссылка на документацию:** https://git-scm.com/docs/git-checkout#Documentation/git-checkout.txt--bltnewbranchgt

***

**Задача:** загрузить локальную ветвь на удаленный репозиторий.

**Команда:** `git push -u origin имя ветки`.
- `-u` - указывает, что необходимо связать локальную и удаленную ветвь;
- `origin` - имя удаленного репозитория по умолчанию.

`-u` является сокращением опции `--set-upstream`.

**Ссылка на документацию:** https://git-scm.com/docs/git-push#Documentation/git-push.txt--u

***

**Задача:** показать различия между файлами рабочей области и файлами последнего коммита.

**Команда:** `git diff`

**Ссылка на документацию:** https://git-scm.com/docs/git-diff#Documentation/git-diff.txt-emgitdiffemltoptionsgt--ltpathgt82308203

***

**Задача:** откатить коммиты на github'е.

**Команда 1:** `git reset --hard HEAD хэш коммита`.
- `--hard` - указывает, что необходимо удалить все изменения после указанного хэша коммита;
- `HEAD` - указатель на последний коммит.

**Команда 2:** `git push -f origin имя ветки`.
- `-f` - указывает, что необходимо сделать принудительный коммит в репозиторий на github;
- `origin` - имя удаленного репозитория по умолчанию.

**Ссылка на документацию по команде 1:** https://git-scm.com/docs/git-reset#Documentation/git-reset.txt---hard

**Ссылка на документацию по команде 2:** https://git-scm.com/docs/git-push#Documentation/git-push.txt--f

***

**Задача:** Переключиться на другую ветку, не делая коммит промежуточных изменений.

**Команда:** `git stash`.

**Ссылка на документацию:** https://git-scm.com/docs/git-stash#_name

***

**Задача:** Посмотреть список спрятанного в stash'е.

**Команда:** `git stash list`.

**Ссылка на документацию:** https://git-scm.com/docs/git-stash#_description

***

**Задача:** Извлечь определнные изменения из stash'а.

**Команда:** `git stash apply stash@{номер_изменения}`.

**Ссылка на документацию:** https://git-scm.com/docs/git-stash#Documentation/git-stash.txt-apply--index-q--quietltstashgt

***

**Задача:** Удалить спрятанные изменения из stash'а.

**Команда:** `git stash drop stash@{номер_изменения}`.

**Ссылка на документацию:** https://git-scm.com/docs/git-stash#Documentation/git-stash.txt-drop-q--quietltstashgt

***

**Задача:** Посмотреть список удаленнх репозиториев, где можно
делать fetch/push.

**Команда:** `git remote -v`.

**Ссылка на документацию:** https://git-scm.com/docs/git-remote#Documentation/git-remote.txt--v

***

**Задача:** Добавить дополнительный удаленный репозиторий для push/pull.

**Команда:** `git remote add [произвольное имя репозитория] [ссылка на репозиторий]`.

**Ссылка на документацию:** https://git-scm.com/docs/git-remote#Documentation/git-remote.txt-emaddem

***

**Задача:** Настроить push в дополнительный репозиторий.

**Команда:** `git remote set-url --add --push [произвольное имя репозитория] [ссылка на репозиторий]`.

**Ссылка на документацию:** https://git-scm.com/docs/git-remote#Documentation/git-remote.txt-emaddem

***

**Задача:** Удалить локальную ветку.

**Команда:** `git branch -d имя_ветки`.

**Ссылка на документацию:** https://git-scm.com/docs/git-branch#Documentation/git-branch.txt--d

***

**Задача:** Создание локальной ветки из удаленной.

**Команда:** `git checkout -b [название локальной ветки] [название репозитория]/[название удаленной ветки]`.

***

**Задача:** Создание патча из незакоммитченных изменений.

**Команда:** `git diff > [путь, до места сохранения патча\имя патча.patch]`. 

**Ссылка на документацию:** https://git-scm.com/docs/git-diff

***

**Задача:** Получить статистику по патчу.

**Команда:** `git apply --stat [путь до патча\имя патча.patch]`. 

**Ссылка на документацию:** https://git-scm.com/docs/git-apply#Documentation/git-apply.txt---stat

***

**Задача:** Проверка патча.

**Команда:** `git apply --check [путь до патча\имя патча.patch]`. 

**Ссылка на документацию:** https://git-scm.com/docs/git-apply#Documentation/git-apply.txt---check

***

**Задача:** Применить патч.

**Команда:** `git apply [путь до патча\имя патча.patch]`. 

**Ссылка на документацию:** https://git-scm.com/docs/git-apply

***

**Задача:** Откатить последний коммит, сохранив изменения в рабочей директории.

**Команда:** `git reset --mixed`. 

**Ссылка на документацию:** https://git-scm.com/docs/git-reset#Documentation/git-reset.txt---mixed

***