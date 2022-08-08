# gitCourses

## https://ru.hexlet.io/courses/intro_to_git

- Первым делом установка гита на машину. с этим понятно.
- Затем настройка метаданных для аккаунта
``` 
git config --global user.name "<имя фамилия>"
git config --global user.email "<ваш емейл>" 
```
- Нужно создать ssh-ключи для подключения к аккаунту. 
```
ssh-keygen -t ed25519  -C "your_email@example.com"
# Дальше будет несколько вопросов. На все вопросы нужно нажимать Enter.

# Запуск агента ssh, который следит за ключами
eval "$(ssh-agent -s)"

# Добавления нового ssh-ключа в агент
ssh-add ~/.ssh/id_ed25519
```
