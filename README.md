# Веб-приложение, написанное с помощью фреймворка Django.
Приложение создано выполнять функцию таск-менеджера. В данном случае - для персонала, работающего с физическим уровнем сети (монтажников).


# Запуск:
Для локального запуска необходимо поместить в директорию /task_manager_L1/tasks/tasks файл .env, либо добавить SECRET_KEY в settings.py в той же директориии.
Затем из папки /task_manager_L1/tasks/ произвести запуск:
python manage.py runserver --insecure (При выключенном DEBUG в режиме insecure будут корректно работать статические файлы)

После данных действий запустится локалхост, на котором можно протестировать приложение.
Если что-то пошло не так, можно добавить requirements вручую командой:  pip install -r requirements.txt    

## В приложении есть 2 группы пользователей:
- Support
- Installers

Различаются данные группы отображаемым на страницах контентом.
### Support имеют право:
- Просматривать, добавлять и редактировать (в т.ч. закрывать) задачи
- Оставлять комментарии
- Добавлять объявления на главной странице
Также данная группа в списке задач видит все элементы, относящиеся к задачам.

### Installers имеют право:
- Просматривать задачи
- Оставлять комментарии
Данная группа в списке задач видит только те задачи, которые назначены на конкретного авторизованного юзера.

https://drive.google.com/file/d/1TPidcUe4mRZd-bWAl8fC6zORuBsn8Lox/view?usp=sharing
