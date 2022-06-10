# Инструкция по работе с гит

## Что такое git?

## Подготовка репозитория
Для того, чтобы создать репозиторий используется команда "git init". Для этого необходимо написать в терминале в папке будующего репозитория "git init"

## Создание сохранений


### Добавление файла к коммиту

Для добавления файла к коммиту используе команда *git add*. Пишется она следующим образом *git add <имя файла>* в терминале в папке с созданным репозиторием 

### Создание коммита

Для создания нового "сохраниения" используется команда *git commit*. Используется она следующим образом: в терминале с папкой-репозиторием пишется *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать **ОБЯЗАТЕЛЬНО**!!!

## Перемещение между сохранениями

Для перемещения между сохранениями используется команда *git checkout*. Для того, чтобы переместиться на указанный коммит в терминале в папке с репозиторием пишем *git checkout <номер коммита>*. **Номер коммита** берется из жкрнала изменений, о котором сказанно выше. После перемещения на указанный коммит мы попадаем в сосотояние *detached head*. Чтобы вернуться к обычной работе, необходимо написать *git checkout master*.

## Журнал изменений

## Перемещение между коммитамиы

## Ветки в git

## Слияние веток и разрешение конфликтов

## Удаление веток