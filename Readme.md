cd# Инструкция по работе с Git

## Подготовка репозитория
Для создания репозитория используется команда *git init*. Чтобы созадать репозиторий напишите в терминале с открытой папкой для репозитория *git init*.

## Добавление файлов в репозиторий

Для добавления файла к коммиту используется комманда *git add*. Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.

## Создание коммита
Для создания коммита используется команда *git commit*. Чтобы создать новый коммит в терминале с открытой папкой-репозиторием пишем команду *git commit -m "<сообщение к коммиту>"*. Сообщения к коммитам писать ***ОБЯЗАТЕЛЬНО***.

## Создание новой ветки 

Для создания новой ветки используется команда *git branch <название новой ветки>* 
Кроме того, можно использовать команду *git checkout -b <название ветки>* для создания и перехода сразу на эту ветку 


## Просмотр всей информации и комитов 

Для вывода всех коммитов используется команда *git log* 


## Просмотр всех сузествующих веток 

Для вывода всех существующих веток используется команда *git branch* символом * будет указана ветка на которой вы сейчас находитесь, также она будет выделена другим цветом текста 


## Переход на другую ветку 

Для перехода на другую ветку, используется команда *git checkout <название ветки>* 

## Загрузка репозитория

Для того чтобы загрузить/скопировать репозиторий, используется команда *git clone*

## Отправка информации из локального, в удалённый репозиторий 

Для того, чтобы отправить информацию в удалённый репозиторий, используется команда *git push*

## Добавление информации из удалённого репозитория в локальный

Чтобы стянуть информацию из удалённого репозитория в локальный, используется команда *git pull*
