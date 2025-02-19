# Репозиторий для **pull request**
* В своём аккаунте на GitHub создать копию репозитория **"AndreyBulgakov19/SCV_GitPR"** с помощью кнопки **"Fork"**.
---
* Клонировать копию репозитория на локальный компьютер.
---
* Создать новую ветку.
---
* Добавить файл с инструкцией в новую ветку.
---
* Дополнить инструкцию разделами по работе с удалёнными репозиториями, pull request.
---
* Зафиксировать изменения (коммиты).
---
* Отправить изменения на GitHub.
---
* На сайте GitHub выполнить **Pull request**.
---
![Logo Git](/image\dfafafaf.png)
# Работа с Git и GitHub
## 1. Проверка наличия установленного Git
В терминале выполнить команду **git —version**.
Если Git установлен появится сообщение с информацией о версии программы. Иначе будет сообщение об ошибке.
## 2. Установка Git
Загружаем последнюю версию Git с [сайта](https://git-scm.com/download/win)
Устанавливаем с настройками по умолчанию.
## 3. Настройка Git
При первом использовании Git необходимо представиться.
Для этого нужно ввести в терминале 2 команды:

**git config —global user.name "Ваше имя английскими буквами"**

**git config —global user.email ваша почта@example.com**
## 4. Инициализация репозитория
Для создания нового репозитория используется команда *git init*. Команду *git init* выполняют только один раз для первоначальной настройки нового репозитория. Выполнение команды приведет к созданию нового подкаталога **git** в вашем рабочем каталоге. Кроме того, будет создана новая главная ветка.
## 5. Запись изменений в репозитории
Основной инструмент, используемый для определения, какие файлы в каком состоянии находятся - это команда
```
git status
```
## 6. Просмотр истории коммитов
После того, как вы создали несколько коммитов или же клонировали репозиторий с уже существующей историей коммитов, вероятно вам понадобится возможность посмотреть что было сделано - *историю коммитов*. Одним из основных способов и наиболее мощных инструментов для этого является команда ``git log``
## 7. Перемещение между сохранениями
Чтобы перемещаться между сохранениями, нужно использовать команду **git checkout**.
## 8. Игнорирование файлов
Для того чтобы исключить из отслеживания в репозитории определенные файл или папки необходимо создать файл ***.gitignore*** и записать в него их названия или шаблоны, соответсвующие таким файлам или папкам.
## 9. Создание веток в Git
Создать новую ветку можно командой
```
git branch <branch_name>
```
Список веток в репозитории можно посмотреть с помощью команды :
```
git branch
```
Текущая вечка будет отмечена звёздочкой
**\* master**

## 10. Слияние веток и разрешение конфликтов
Для слияния выбранной ветки с текущей нужно выполнить команду:
```
git merge <название выбранной ветки>
```
Если была изменена одна и та же часть файла в обеих ветках, то может возникнуть конфликт, который потребует участия пользователя.
VSCode предлагает варианты разрешения.

## 11. Удаление веток
Для удаления ветки, мы должны использовать уже знакомую команду **git branch** c ключами **-d** и **-D**. Выглядит это так:
```
git branch -d <название выбранной ветки>
```
или
```
git branch -D <название выбранной ветки>
```
**Ключи:**

``-d``

С этим ключом команда удалит вашу ветку. Ветка будет удалена только в том случае, если она полностью слита с одной из других веток. В противном случае, Git выдаст предупреждение, о том, что в ветке есть неслитые изменения, и не даст ее удалить.

``-D``

Этот ключ нужен, если вы хотите удалить ветку, игнорируя предупреждения Git. В отличие от **-d**, этот ключ удалит ветку в любом случае, даже если в ней есть изменения, которые вы можете потерять.

Так же нельзя удалить ветку, находясь в самой ветке, нужно перейти в другую ветку.

## 12. Работа с удаленными репозиториями
**Клонирование удаленного репозитория**

Давайте узнаем, как можно склонировать удаленный репозиторий к себе на компьютер. Операция клонирования создаёт на вашем компьютере точную копию удаленного репозитория.

Необходимость клонировать существующий удаленный репозиторий возникает в ситуациях, когда вы решаете поработать над уже существующим кодом. Для выполнения этой операции в Git предусмотрена команда
```
git clone
```
Нужно нажать на зеленую кнопку *Code* на главной странице репозитория на GitHub, чтобы получить ссылку на удаленный репозиторий.

``Давайте на примере разберем, как происходит клонирование. Клонируем нужный нам репозиторий. При выполнении команды git сlone <ссылка нужного репозитория> произойдет следующее:``

**1.** В директории, откуда вы запустили команду git clone,

Git - Downloading Package
git-scm.com
создается директория с именем репозитория.

**2.** В созданную директорию копируется репозиторий, все его ветки и коммиты.

**3.** В новосозданный локальный репозиторий добавляется удаленный репозиторий с именем origin и ссылкой, которую мы передавали в git clone. Это избавляет нас от необходимости вручную писать git remote add origin. На этом процесс клонирования заканчивается.

**Отправка изменений в удаленный репозиторий**

Когда вы хотите поделиться своими наработками, вам необходимо отправить их в удалённый репозиторий. Команда для этого действия простая: *git push*. Чтобы отправить вашу ветку *master* на сервер *origin* (повторимся, что клонирование обычно настраивает оба этих имени автоматически), вы можете выполнить следующую команду для отправки ваших коммитов:

```
git push origin master
```

Эта команда срабатывает только в случае, если вы клонировали с сервера, на котором у вас есть права на запись, и если никто другой с тех пор не выполнял команду *push*. Если вы и кто-то ещё одновременно клонируете, затем он выполняет команду *push*, а после него выполнить команду push попытаетесь вы, то ваш *push* точно будет отклонён. Вам придётся сначала получить изменения и объединить их с вашими и только после этого вам будет позволено выполнить *push*.

**Получение изменений из удалённого репозитория**

 Как вы только что узнали, для получения данных из удалённых проектов, следует выполнить:
```
git fetch
```
Данная команда связывается с указанным удалённым проектом и забирает все те данные проекта, которых у вас ещё нет. После того как вы выполнили команду, у вас должны появиться ссылки на все ветки из этого удалённого проекта, которые вы можете просмотреть или слить в любой момент.

Когда вы клонируете репозиторий, команда clone автоматически добавляет этот удалённый репозиторий под именем *«origin»*. Таким образом, *git fetch origin* извлекает все наработки, отправленные на этот сервер после того, как вы его клонировали (или получили изменения с помощью fetch). Важно отметить, что команда *git fetch* забирает данные в ваш локальный репозиторий, но не сливает их с какими-либо вашими наработками и не модифицирует то, над чем вы работаете в данный момент. Вам необходимо вручную слить эти данные с вашими, когда вы будете готовы.

Если ветка настроена на отслеживание удалённой ветки, то вы можете использовать команду **git pull** чтобы автоматически получить изменения из удалённой ветки и слить их со своей текущей. Этот способ может для вас оказаться более простым или более удобным. К тому же, по умолчанию команда *git clone* автоматически настраивает вашу локальную ветку *master* на отслеживание удалённой ветки *master* на сервере, с которого вы клонировали репозиторий. Название веток может быть другим и зависит от ветки по умолчанию на сервере. Выполнение **git pull**, как правило, извлекает (fetch) данные с сервера, с которого вы изначально клонировали, и автоматически пытается слить (merge) их с кодом, над которым вы в данный момент работаете.

**Просмотр удалённого репозитория**

Если хотите получить побольше инфффформации об одном из удалённых репозиториев, вы можете использовать команду:
```
git remote
```
