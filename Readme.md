# Инструкция по работе с Git

## Подготовка репозитория
Для создания репозитория используется команда *git init*. Чтобы созадать репозиторий напишите в терминале с открытой папкой для репозитория *git init*.

## Добавление файлов в репозиторий

Для добавления файла к коммиту используется комманда *git add*. Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.

## Создание коммита
Для создания коммита используется команда *git commit*. Чтобы создать новый коммит в терминале с открытой папкой-репозиторием пишем команду *git commit -m "<сообщение к коммиту>"*. Сообщения к коммитам писать ***ОБЯЗАТЕЛЬНО***.

# Работа с удаленными репозиториями в Git

- Копирование удаленного репозитория. Для этого необходимо взять с Github адрес репозитория, который мы хотим скопировать и в терминале вставить команду git clone адрес_репозитория.

- Добавление своего репозитория в общий доступ. Для этого необходимо сначала создать профиль на Github. Затем необходимо соединить локальный и удаленный репозиторий(git remote). Потом отправляем (push) наш локальный репозиторий в удаленный (Github).

- Получение корректировок из удаленного репозитория. Для того, чтобы внесенные изменения отобразились созданные на Github неообходима команда git pull адрес_репозитория

- Отключить удаленны репозиторий от локального. Для этого необходимо вызвать команду git remote remove название_удаленного_ репозитория
