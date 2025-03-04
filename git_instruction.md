# Инструкция по работе с системой контроля версий GIT

## Работа с локальным репозиторием

### Создание локального репозитория

Репозиторий создается в конкретном каталоге с помощью команды ***git init***  
В результате выполнения команды *git init* появится подкаталог .git, в котором и будут храниться служебные настройки git'а и сам репозиторий.

### Добавление измененных файлов в список отслеживания

GIT будет следить только за теми файлами, которые вы добавили в список отслеживаемых.  
Сделать это можно с помощью команды ***git add name_file***, где add_file - имя добавляемого файла

### Фиксация изменений в файлах

Чтобы зафиксировать (закоммитить) изменения файла после сохранения, необходимо использовать команду ***git commit***  
Если необходимо добавить к коммиту сообщение, в котором указано, какие именно изменения мы внесли, необходимо использовать команду ***git commit -m "Сообщение коммита"***

### Проверка текущего статуса репозитория

Для отслеживания текущего статуса репозитория необходимо ввести команду ***git status***

### Просмотр истории коммитов

Для просмотра истории создания всех коммитов текущей ветки необходимо использовать команду ***git log***

### Просмотр имеющихся веток, создание и удаление новых

Для просмотра имеющихся веток необходимо использовать команду ***git branch***  
Для создания новой ветки необходимо использовать команду ***git branch name***, где name - имя новой ветки  
Для удаления созданной ветки необходимо использовать команду ***git branch -d name***, где name - имя удаляемой ветки

### Переключение между ветками / коммитами

Для переключения на другую ветку нужно использовать команду ***git checkout name***, где name - имя ветки, на которую хотим переключиться.  
Для переключения на другой коммит нужно использовать команду ***git checkout id_commit***, где id_commit - это идентификатор нужного нам коммита.

### Слияние веток

Для слияния двух уже существующих веток необходимо выполнить следующие действия:  
1. Переключиться на ту ветку, на которую будем производить слияние.  
2. Для слияния использовать команду ***git merge name***, где name - название ветки, с которой происходит слияние.

## Работа с удаленным репозиторием

### Отправка изменений с локального в удаленный репозиторий

Для первичной отправки изменений на удаленный репозиторий необходимо использовать команду ***git push link_repository***, где link_repository - это ссылка удаленного репозитория.  
Для всех последующих отправок изменений необходимо использовать команду ***git push***, поскольку привязка к удаленному репозиторию уже сделана.

### Получение изменений с удаленного в локальный репозиторий

Для получения изменений с удаленного репозитория необходимо использовать команду ***git pull***  
**Заметка:** прежде чем отправлять изменения на удаленный репозиторий, необходимо сначала получить оттуда все изменения. В противном случае при слиянии произойдет конфликт.

### Копирование удаленного репозитория к себе на компьютер

Для копирования удаленного репозитория себе на компьютер необходимо использовать команду ***git clone link_repository***, где link_repository - URL-адрес расположения удаленного репозитория в интернете.

## Игнорирование файлов в работе с GIT

Чтобы часть файлов можно было игнорировать, нужно создать в репозитории файл с названием ***.gitignore***, в который внести, сохранить, добавить (git add name_file) и закоммитить (git commit) название с расширением каждого игнорируемого файла на отдельной строке.
