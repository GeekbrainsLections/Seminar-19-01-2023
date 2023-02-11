# Инструкция по работе с Git и удаленными репозиториями

## Что такое Git?
***Git*** - это одна из реализаций распределенной системы контроля версий, поддерживающие как локальные, так и удаленные репозитории.Самая популярная реализация Git - это [GitHub](https://github.com)

## Подготовка репозитория
Для создания репозитория используется команда *git init*. Для этого необходимо открыть в терминале папку с будущим репозиторием и там написать *git init*

## Создание коммитов

### Выполнение коммита
Для того, чтобы выполнить коммит используется команда *git commit*. Для этого в терминале с папкой-репозиторием необходимо написать *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!!***

### Добавление файла к коммиту
Для добавления файла к коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.

## Журнал изменений
Для просмотра истории коммитов используется команда *git log*. Для этого в терминале с папкой-репозиторием пишем *git Log*. В показанном журанале обязательно будут:
* Хеш (номер) коммита
* Дата и время коммита
* Автор коммита
* Текст сообщения к коммиту

## Перемещение между коммитами
Для перемещения между коммитами используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <[хеш коммита]>*. Хеш коммита можно взять из истории коммитов, про которую было рассказано в предыдущем пункте.

## Ветки в Git
Используя ветвление, Вы отклоняетесь от основной линии разработки и продолжаете работу независимо от неё, не вмешиваясь в основную линию.

### Создание веток
Для создания новой ветки используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch <название ветки>*. Название ветки должно быть ***УНИКАЛЬНО***!

### Просмотр списка веток
Для просмотра списка веток используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch* и Вы увидите список всех существующих веток. Зеленым цветом и символом **звездочка** будет обозначена текущая актуальная ветка

### Перемещение между ветками
Для перемещения между ветками используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <название ветки>*. Ветка ***обязательно должна существовать!!!***.

## Слияние веток и разрешение конфликтов

Команда git merge используется для слияния одной или нескольких веток в текущую. Затем она устанавливает указатель текущей ветки на результирующий коммит.
В некоторых случаях Git не может автоматически определить, какое изменение является правильным, После этого возникают конфликты затрагивают только того разработчика, который выполняет слияние, остальная часть команды о конфликте не знает. Git помечает файл как конфликтующий и останавливает процесс слияния. В этом случае ответственность за разрешение конфликта несут разработчики.

## Удаление веток

Чтобы удалить локальную ветку GIT, мы можем выполнить одну из следующих команд:

git branch -d branch_name

## Команда git clean
Команда git clean используется для удаления мусора из рабочего каталога. Это могут быть результаты сборки проекта или файлы конфликтов слияний.

## Удаленный репозиторий
Версии вашего проекта, сохраненные на удаленном сервере. Доступ к репозиторию на таком сервере может осуществляться по интернету или по локальной сети.
Если мы подключим удаленный репозиторий к своему локальному, то у нас появятся копии всех ссылочных объектов удаленного репозитория.

## Добавление удаленного репозитория
Чтобы добавить новый удаленный репозиторий, выполните команду git remote add в терминале в каталоге, в котором хранится репозиторий.

Команда git remote add принимает два аргумента:

имя удаленного репозитория, например, origin;
URL-адрес удаленного репозитория, например, https://github.com/user/repo.git.

## Команда git pull
Автоматичеси извлекает и затем сливает данные из удалённой ветки в вашу текущую ветку. Этот способ может для вас оказаться более простым или более удобным. 

## Команда git push
Используется для выгрузки содержимого локального репозитория в удаленный репозиторий. Она позволяет передать коммиты из локального репозитория в удаленный.

## git remote
Команда git remote служит для управления списком удалённых репозиториев. Она позволяет сохранять длинные URL репозиториев в виде понятных коротких строк, например «origin», так что вам не придётся забивать голову всякой ерундой и набирать её каждый раз для связи с сервером. Вы можете использовать несколько удалённых репозиториев для работы и git remote поможет добавлять, изменять и удалять их.
