# Инструкция по работе с гит

## Что такое git?

Git — система управления версиями с распределенной архитектурой.В отличие от некогда популярных систем вроде CVS и Subversion (SVN), где полная история версий проекта доступна лишь в одном месте, в Git каждая рабочая копия кода сама по себе является репозиторием. Это позволяет всем разработчикам хранить историю изменений в полном объеме.
*Git* одна из реализаций распределенных систем контороля версий. *Git* на данный момент является самой популярной реализацией. Самой попоулярной реализацией *Git* является [GitHub](https://github.com)

## Подготовка репозитория
Для того, чтобы создать репозиторий используется команда "git init". Для этого необходимо написать в терминале в папке будующего репозитория "git init"

## Создание сохранений


### Добавление файла к коммиту

Для добавления файла к коммиту используе команда *git add*. Пишется она следующим образом *git add <имя файла>* в терминале в папке с созданным репозиторием 

### Создание коммита

Для создания нового "сохраниения" используется команда *git commit*. Используется она следующим образом: в терминале с папкой-репозиторием пишется *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать **ОБЯЗАТЕЛЬНО**!!!

## Журнал изменений

Для просмотра журнала изменений исползуется команда *git log*. Для этого в терминале в папке с репозиторием достаточно написать *git log*

## Перемещение между коммитами

Для перемещения между сохранениями используется команда *git checkout*. Для того, чтобы переместиться на указанный коммит в терминале в папке с репозиторием пишем *git checkout <номер коммита>*. **Номер коммита** берется из жкрнала изменений, о котором сказанно выше. После перемещения на указанный коммит мы попадаем в сосотояние *detached head*. Чтобы вернуться к обычной работе, необходимо написать *git checkout master*.

## Ветки в Gitt

Ветки нужны для того, чтобы программисты могли вести совместную работу над проектом и не мешать друг другу при этом. При создании проекта, Git создает базовую ветку. Она называется master веткой. Она считается центральной веткой, т.е. в ней содержится основной код приложения.
 Просто сделать ветку, не переключаясь на нее можно командой *git branch <имя ветки>*, для того чтобы переключиться на ветку используется команда *git checkout <имя ветки>*
 Команда *git branch* делает несколько больше, чем просто создаёт и удаляет ветки. При запуске без параметров, вы получите простой список имеющихся у вас веток. Обратите внимание на символ *, стоящий перед веткой master: он указывает на ветку, на которой вы находитесь в настоящий момент (т. е. ветку, на которую указывает HEAD). Это означает, что если вы сейчас сделаете коммит, ветка master переместится вперёд в соответствии с вашими последними изменениями.
 
## Слияние веток и разрешение конфликтов

Что бы смержить одну ветку в другую нужно вначале переключиться на ту ветку, в которую вы хотите смержить, делвется жто командой *git checkout <имя ветки>*, Затем выполнить команду *git merge <имя ветки>*, последняя команда как раз и реализует слияние
Конфликты возникают при мердже веток если в этих ветках одна и та же строка кода была изменена по-разному. Тогда получается, что Git не может сам решить какое из изменений нужно применить и он предлагает вручную решить эту ситуацию. Если мы делаем изменения в ручную, то обязательно после изменнения конфликтной строки, необходими выполнить коммит.

## Удаление веток

Чтобы удалить ветку в git, необходимо ввести команду *git branch -d <название ветки>*