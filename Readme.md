# Инструкция по работе с Git и удалёнными репозиториями

## Что такое Git?
***Git*** - это одна из реализаций распределённой системы контроля версий, поддерживающие как локальные, так и удалённые репозитории. Самая популярная реализация Git - это [GitHub](https://github.com)

## Подготовка репозитория
Для создания репозитория используется команда *git init*. Для этого необходимо открыть в терминале папку с будущим репозиторием и там написать *git init*

## Создание коммитов

### Выполнение коммита
Для того, чтобы выполнить коммит используется команда *git commit*. Для этого в терминале с папкой-репозиторием необходимо написать *git commit -m "<сообщение к коммиту>"*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!!***

### Добавление файла к коммиту
Для добавления файла к коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.

## Журнал изменений
Для просмотра истории коммитов используется команда *git log*. Для этого в терминале с папкой-репозиторием пишем *git log*. В показанном журнале обязательно будут:
* Хеш(номер) коммита
* Дата и время коммита
* Автор коммита
* Текст сообщения к коммиту

## Перемещение между коммитами
Для перещения между коммитами используется команда *git checkout*. Для этого в терминале с папкогой-репозиторием необходимо написать *git checkout <хеш коммита>*. Хеш коммита можно взять из истории коммитов, про которую было рассказано в предыдущем пункте

## Ветки в Git

Веток может быть неограниченное количество.

### Создание веток
Для создания новой ветки используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch <название ветки>*. Название ветки должно быть ***УНИКАЛЬНО***!

### Просмотр списка веток
Для просмотра списка веток используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *giit branch* и Вы увидите список всех существующих веток. Зелёным цветом и символом **звёздочка** будет обозначена текущая актуальная ветка.

### Перемещение между ветками
Для перемещения между ветками используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <название веткки*. Ветка ***ОБЯЗАТЕЛЬНО ДОЛЖНА СУЩЕСТВОВАТЬ!!!***. 

## Слияние веток и разрешение конфликтов
Слияние веток выполняется командой *git merge*. Для этого необходимо перейти на ветку, на которую вы хотите выполнить слияние, и ввесте команду *git merge <название ветки, которую хотите слить>* После введения этой команды git будет сливать ветки по своим автоматическим алгоритмам. Бывают случаи, когда автоматическая стратегия слияния веток не срабатывают, и возникают **конфликты**. Разрешения конфликтов предусмотрены как *автоматические*, так и *вручную*, так, при автоматическом варианте будет предложено либо принять текущие изменения, либо принять входящие изменени, либо принять оба варианта, необходимо будет выбрать нужный вариант и нажать на него. При ручном способе разрешения конфликта необходимо выбрать нужный вариант и просто стереть ***НЕНУЖНЫЙ*** текст, также удаляя все спец. символы, такие как #####, <<<<< и т.д.

## Удаление веток
Для удаления веток используется команда *git branche -d*. Для этого необходимо в терминале ввести команду *git branche -d <название ветки>*. и произойдет удаление выбранной вами ветки.
___

### Небольшая общая информация по обозначению команд.
* git init – создает новый репозиторий
* git status – отображает список измененных, добавленных и удаленных файлов
* git add – добавляет указанные файлы в индекс
* git commit – фиксирует добавленные в индекс изменения
___

# Работа с удаленными репозиториями.

## Клонирование репозитория.
Для того, чтобы создать клон папки-репозитория необходимо открыть сайт *Github* или другой сайт, где есть папки-репозитории и скопирать с них ссылку. Далее необходимо дать команду *Git clone <ссылка>* и нажать enter. После этого Git начнет загрузку данной папки-репозитория.

## Переключение на папку-клона.
Переключение на папку-репозиторий (клон) необходимо дать команду *git cd <название папки>*, Git автоматически переключит вас на эту папку, после чего можно вносить изменения и делать коммиты.

## Загрузка изменений **ИЗ** сервера.
Для того, чтобы скачать изменения из удаленного репозитория необходимо ввести команда *git pull origin master*. После введения этой команды git "обновит" документ в удаленном репозитории автоматически, ***НО!*** если в удаленном репозитории имеется более актуальная версия документа git выдаст ошибку!. Для этого необходимо скачать версию с удаленного репозитория, ее подправить и отправить туда обратно.

## Выгрузка изменений **НА** сервер.
Для того, чтобы скачать изменения ***с сервера*** или принять самую актуальную версию документа необходимо написать команду *git push origin master*, после чего обновление (скачивание) документа произойдет автоматически. Возможно при слиянии будет состояние конфликта, поэтому их будет необходимо слить.

## Fork
fork это по сути полное копирование папки-репозитория другого автора для возможности внесения в нее изменений без риска испортить исходные данные. При форке доступен весь функционал системы git, после всех правок делается pull requests. Как правило такая система используется для более безопасного слияния для исходного документа (отдельных веток или всего документа целиком) 

## Pull requests.
Для того, чтобы после внесения изменений в форке поделиться новым документом с автором документа необходимо сделать pull requests. Для этого нужно на сайте github в выбранном форке нажать на кнопку pull Requests и там выбрать какой документ, кому и какую ветку отправим автору, после этого автору документа придет уведомление, где он сможет либо принять изменения в документе, либо отказаться от них.