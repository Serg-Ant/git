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