# gitCourses

## https://ru.hexlet.io/courses/intro_to_git

 Первым делом установка гита на машину. с этим понятно.
 Затем настройка метаданных для аккаунта
``` 
git config --global user.name "<имя фамилия>"
git config --global user.email "<ваш емейл>" 
```
 Нужно создать ssh-ключи для подключения к аккаунту. 
```
ssh-keygen -t ed25519  -C "your_email@example.com"
# Дальше будет несколько вопросов. На все вопросы нужно нажимать Enter.

# Запуск агента ssh, который следит за ключами
eval "$(ssh-agent -s)"

# Добавления нового ssh-ключа в агент
ssh-add ~/.ssh/id_ed25519
```

Этот ключ нужно занести в гитхаб. Для этого копируем содержимое публичной части ключа из консоли и заносим в github. Ключ смотрим по расширению .pub
```
cat ~/.ssh/id_ed25519.pub
```
### Рабочая среда настроена.
Теперь мы создаём папку, в ней прописываем ``` git init ``` Инициализируя репозиторий.
Команда ``` git status ``` позволяет посмотреть состояние репозитория
Теперь для добавления файлов в репозиторий мы можем написать ``` git add {Путь до файла} ``` Статус такого добавленного файла изменится с *Untracked files* на *Changes to be committed*. Иными словами, файл попадает в *Индекс*

