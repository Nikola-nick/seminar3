# **Инструкция по работе с Git**

Git- это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контрол версий в мире.

## Инициализация репозитория

Для создание репозитория необходимо выполнить команду git init в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

## Проверка состояния репозитория

Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.

## Фиксация изменений

### Git add
Для добавления измений в коммит используется команда *git add*. Чтобы исползовать команду *git add*,напишите *git add <имя файла>*, где вместо имя файла пишется полное имя файла в котором были произведены изменения.
### Git commit
Для того, чтобы зафиксировать ваши изменения необходимо вызвать команду *git commit*.Эта команда откроет выбранный вами текстовый редактор.В редакторе будет отображён текст. В этом тексте вы можете удалить коментарии инабрать своё сообщение или же оставить их для напоминания о том, что вы фиксируете.
### Git commit -m 
Для того чтобы ускорить и упростить работу, можно выбрать другой вариант фиксации измнений. Для этого необходимо вызвать команду "git commit -m". вы набираете свой комментарий к коммиту в командной строке вместе с командой commit указав его после параметра -m. Для примера - *git command -m "new commit"*.
### Git commit -a
Для сокращения действий, есть команда для совмещения последовательно выполненных действий команд "dit add" и "gi commit". Чтобы воспользоваться этим сокращеним необходимо вызвать команду "git commit -am"

## Просмотр истории комитов

git log
    Чтобы посмотреть историю коммитов используется команда *git log*
git log --all
    Для отображения всех комитов (не зависимо от того на который мы сейчас переключены) используется команда *git log --all*
git log --oneline
    Для отображения лога в кратком виде (один комит - одна строка) используется команда *git log --oneline*

## Переключение между версиями

Команда *git checkout* используется для переключения веток и выгрузки их содержимого в рабочий каталог.

## Просмотр различий между комитами

Команда *git diff* показывает различия по внесённым изменениям в ещё не проиндексированных файлах.

## Ветвление

git branch Список именованных веток коммитов с указанием выбранной ветки
git branch txt Создаёт новую ветку
git branch -d [имя ветки] Удаляет выбранную ветку
git merge Вносит изменения указанной ветки в текущую ветку.Находясь в Master(главной) ветви, Вы можете использовать эту команду, чтобы взять коммиты из любой из ветвей и соединить их вместе.

## Игнорировнаие некоторых файлов

Git будет игнорировать файлы и директории, перечисленные в файле ** .gitignore ** с помощью синтаксиса.

## Удаленные репозитории

УДАЛЕННЫЕ РЕПОЗИТОРИИ НУЖНЫ ДЛЯ ОБЕСПЕЧЕНИЯ СОВМЕСТНОЙ РАБОТ И РЕЗЕРВИРОВАНИИ НАШЕГО ПРОЕКТА В ОБЛАЧНОМ РЕПОЗИТОРИИИ

## Удаленный репозиторий

Удалённые репозитории — это модификации проекта, которые хранятся в интернете или ещё где-то в сети. Их может быть несколько, каждый из которых, как правило, доступен для вас либо только на чтение, либо на чтение и запись.

### Управление удаленным репозиторием

Совместная работа включает в себя управление удалёнными репозиториями и помещение (push) и получение (pull) данных в и из них тогда, когда нужно обменяться результатами работы. Управление удалёнными репозиториями включает умение добавлять удалённые репозитории, удалять те из них, которые больше не действуют, умение управлять различными удалёнными ветками и определять их как отслеживаемые (tracked) или нет и прочее.

    ** git remote **
Чтобы просмотреть, какие удалённые серверы у вас уже настроены, следует выполнить команду *git remote*.  Чтобы добавить новый удалённый Git-репозиторий под именем-сокращением, к которому будет проще обращаться, выполните *git remote add [сокращение] [url]*.

    ** git fetch **
Для получения данных из удалённых проектов, следует выполнить: *git fetch [имя удал. сервера]*.
*git fetch origin* извлекает все наработки, отправленные (push) на этот сервер после того, как вы склонировали его (или получили изменения с помощью fetch.

    ** git clone **
Когда вы клонируете репозиторий, команда clone автоматически добавляет этот удалённый репозиторий под именем origin. Команда *git clone* автоматически настраивает вашу локальную ветку master на отслеживание удалённой ветки master на сервере, с которого вы клонировали.

### Отображение удаленных репозиториев

Если у вас есть ветка, настроенная на отслеживание удалённой ветки, то вы можете использовать команду *git pull*.Выполнение *git pull*, как правило, извлекает данные с сервера, с которого вы изначально склонировали, и автоматически пытается слить (merge) их с кодом, над которым вы в данный момент работаете. Если вы, находясь на ветке master, выполните *git pull*, ветка master с удалённого сервера будет автоматически влита в вашу сразу после получения всех необходимых данных.

## Github

GitHub — это облачная платформа для хостинга IT-проектов и совместной разработки, под капотом которой находится популярная система контроля версий Git, а также полноценная социальная сеть для разработчиков.
А ещё не стоит путать GitHub и Git. GitHub — лишь одна из реализаций системы контроля версий Git, в которую добавлено много удобных инструментов и возможностей (те же комментарии, issues, гиперссылки, форматированный текст и тому подобное).
Почти вся терминология наследуется у Git. Основные термины — репозиторий, ветка, коммит, форк.
