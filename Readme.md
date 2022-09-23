# Инструкция по работе с Git

Что такое **«система контроля версий»** и почему это важно? Система контроля версий — это
система, записывающая изменения в файл или набор файлов в течение времени и
позволяющая вернуться позже к определённой версии. Для контроля версий файлов в этой
книге в качестве примера будет использоваться исходный код программного обеспечения,
хотя на самом деле вы можете использовать контроль версий практически для любых
типов файлов.

## Имя пользователя

Первое, что вам следует сделать после установки Git — указать ваше имя и адрес
электронной почты. Это важно, потому что каждый коммит в Git содержит эту
информацию, и она включена в коммиты, передаваемые вами, и не может быть далее
изменена: 

git config --global user.name "John Doe"
git config --global user.email johndoe@example.com

## Подготовка репозитория
Для создания репозитория используется команда *git init*. Чтобы созадать репозиторий напишите в терминале с открытой папкой для репозитория *git init*.

## Создание коммита
Для создания коммита используется команда *git commit*. Чтобы создать новый коммит в терминале с открытой папкой-репозиторием пишем команду *git commit -m "<сообщение к коммиту>"*. Сообщения к коммитам писать ***ОБЯЗАТЕЛЬНО***.

## Определение состояния файлов

Основной инструмент, используемый для определения, какие файлы в каком состоянии
находятся — это команда git status. Если вы выполните эту команду сразу после
клонирования, вы увидите что-то вроде этого:

*git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean*

Это означает, что у вас чистый рабочий каталог, другими словами — в нем нет
отслеживаемых измененных файлов. Git также не обнаружил неотслеживаемых файлов, в
противном случае они бы были перечислены здесь. Наконец, команда сообщает вам на
какой ветке вы находитесь и сообщает вам, что она не расходится с веткой на сервере.

## Отслеживание новых файлов (Добавление файлов в репозиторий)

Для добавления файла к коммиту используется комманда *git add*. Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.