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

## Удаление веток
Ветки можно удалять используя 2 флага

## Создание репозитория 
### Создане своего репозитория на ГитХаб
Чтоб создать свой репозиторий на ГитХабе нажимаем на + возле своего аватара или находим кнопку репозиторий --> новый репозиторий --> Придумываем название --> Great Repository. Копируем url ссылку
На ПК в VSC терминале пишем команды:
* git branch -M master
* git remote add origin https://github.com/Algo102/123.git
* git push -u origin master или git push origin master - указывая флаг -u в дальнейшем можно коротко указыват git push, но при этом push пойдет на все сервера, где есть эта репозитория

### Клонирование репозитория с ГитХаб на ПК
Клонировать на ПК можно любой репозиторий как свой, так и чужой.
Для этого в ГБ находим нужный репозиторий --> Code --> копируем УРЛ ссылку, а в терминале набираем git clone https://github.com/Algo102/Seminar-19-01-2023.git
Не забываем в терминале зайти в этот каталог через cd или проводник "Открыть интегрированный терминал"

### Копирование чужого репозитория с ГитХаб на свой Гитхаб
Для совместной работы, когда вы не админ, можно скопировать проект себе, а потом уже отправлять создателю проекта свои предложения в виде кода. 
Для этого на ГХ находим проект, нажимае fork --> greate fork 
Таким образом этот проект скопиравали себе на ГХ, далее вносим изменения или в ГХ или в терминале, а после
отправляем его обратно создателю проекта на рассмотрение 
pull request --> new pull request --> great pull request --> комментарии --> great pull request

## Pull and Push
