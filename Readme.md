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

## Игнорирование файлов

Зачастую, у вас имеется группа файлов, которые вы не только не хотите автоматически
добавлять в репозиторий, но и видеть в списках неотслеживаемых. К таким файлам обычно
относятся автоматически генерируемые файлы (различные логи, результаты сборки
программ и т. п.). В таком случае, вы можете создать файл .gitignore. с перечислением
шаблонов соответствующих таким файлам. Вот пример файла .gitignore. И уже внутри самого файла *.gitignore* вносить файлы, которые следует игнорировать.

## Просмотр индексированных и неиндексированных изменений

Если результат работы команды *git status* недостаточно информативен для вас — вам
хочется знать, что конкретно поменялось, а не только какие файлы были изменены — вы
можете использовать команду *git diff*. Позже мы рассмотрим команду git diff подробнее;
вы, скорее всего, будете использовать эту команду для получения ответов на два вопроса:
что вы изменили, но ещё не проиндексировали, и что вы проиндексировали и собираетесь
включить в коммит. Если git status отвечает на эти вопросы в самом общем виде,
перечисляя имена файлов, git diff показывает вам непосредственно добавленные и
удалённые строки — патч как он есть.

## Создание коммита
Для создания коммита используется команда *git commit*. Чтобы создать новый коммит в терминале с открытой папкой-репозиторием пишем команду *git commit -m "<сообщение к коммиту>"*. Сообщения к коммитам писать ***ОБЯЗАТЕЛЬНО***.

## Удаление файлов

Для того чтобы удалить файл из Git, вам необходимо удалить его из отслеживаемых файлов
(точнее, удалить его из вашего индекса) а затем выполнить коммит. Это позволяет сделать
команда *git rm*, которая также удаляет файл из вашего рабочего каталога, так что в
следующий раз вы не увидите его как «неотслеживаемый»

## Просмотр истории коммитов

После того, как вы создали несколько коммитов или же клонировали репозиторий с уже
существующей историей коммитов, вероятно вам понадобится возможность посмотреть
что было сделано — историю коммитов. Одним из основных и наиболее мощных
инструментов для этого является команда *git log*.

По умолчанию (без аргументов) git log перечисляет коммиты, сделанные в репозитории в
обратном к хронологическому порядке — последние коммиты находятся вверху. 

### Просмотр текущей ветки и историю слияния

С помощью команды git log --graph Отображает ASCII граф с ветвлениями и историей слияний.

## Создание новой ветки

Для создания новой ветки в файле потребуется команда *git branch* - вызов созданных ранее веток в файле (с помощью этой команды мы можем увидеть в какой ветке в данный момент находитесь)

А вот с помощью команды git branch _name branch_ создается новая ветка с указанием ее имени.

>### Альтернативный вариант создания ветки в файле и перейти сразу в нее
>Выполнить это можно с помощью команды *git branch -b *name branch*

## Переключение веток

Для переключения между существующими ветками в файле используется команда **git checkout** + *name branch*

>Чтобы  вернуться на основную ветку необходимо выполнить команду в VS Code - *git chechkout master*

## Удаление ветки
Для того, чтобы удалить ветку после того, как она выполнила свою функцию (после слияния) - необходимо выполнить команду git branch -d *name branch*. Используется также команда git branch -D *name branch* - (удаление ветки из под Основной ветки master).

## Слияние веток

Для того, чтобы слить ветку *name branch* с веткой master потребуется перейти в ветку master и выполнить команду git merge *name branch*. После выполнения этой команды вся информация из ветки *name branch* переместится в ветку master. 

Важно знать!!! Если в момент работы в ветки *name branch* проводились изменения в ветки master, то опреденно возникнет конфликт при слиянии двух веток, так как git определит рассходжения сохраненных версий. В этом случае git предложит:
* Accept Current Change (Принять текущее изменение);
* Accept Incoming Change (Принять входящие изменения);
* Accept Both Changes (Принять Оба изменения);
* Compare Changes (Сравните изменения).

Следует выбрать один из предложенных варинтов и после продолжить работу в файле.

