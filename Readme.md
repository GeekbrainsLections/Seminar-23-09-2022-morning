# Инструкция по работе с Git

## Подготовка репозитория
Для создания репозитория используется команда *git init*. Чтобы созадать репозиторий напишите в терминале с открытой папкой для репозитория *git init*.

## Добавление файлов в репозиторий

Для добавления файла к коммиту используется комманда *git add*. Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.

## Создание коммита
Для создания коммита используется команда *git commit*. Чтобы создать новый коммит в терминале с открытой папкой-репозиторием пишем команду *git commit -m "<сообщение к коммиту>"*. Сообщения к коммитам писать ***ОБЯЗАТЕЛЬНО***.

## Создание копии (удаленного) репозитория

Для начала работы с центральным репозиторием, следует создать копию оригинального проекта со всей его историей локально.

Клонирует репозиторий, используя протокол http:

*git clone http://user@somehost:port/~user/repository/project.git*

Клонирует репозиторий с той же машины в директорию myrepo:

*git clone /home/username/project myrepo*

Клонирует репозиторий, используя безопасный протокол ssh:

*git clone ssh://user@somehost:port/~user/repository*

У git имеется и собственный протокол:

*git clone git://user@somehost:port/~user/repository/project.git/*

Импортирует svn репозиторий, используя протокол http:

*git svn clone -s http://repo/location*

где **-s** – понимать стандартные папки SVN (trunk, branches, tags)

## Забираем изменения из центрального репозитория

Для синхронизации текущей ветки с репозиторием используются команды **git fetch** и **git pull**.

**git fetch** — забирает изменения удаленной ветки из репозитория по умолчания, основной ветки; той, которая была использована при клонировании репозитория. Изменения обновят удаленную ветку (remote tracking branch), после чего надо будет провести слияние с локальной ветку командой **git merge**.

Получает изменения из определенного репозитория:

*git fetch /home/username/project*

Возможно также использовать синонимы для адресов, создаваемые командой *git remote*:

*git remote add username-project /home/username/project*

*git fetch username-project*

Естественно, что после оценки изменений, например, командой **git diff**, надо создать коммит слияния с основной:

*git merge username-project/master*

Команда **git pull** сразу забирает изменения и проводит слияние с активной веткой. Забирает из репозитория, для которого были созданы удаленные ветки по умолчанию:

**git pull** - Забирает изменения и метки из определенного репозитория:

*git pull username-project --tags*

Как правило, используется сразу команда **git pull**.