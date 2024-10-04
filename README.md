## Backend приложения для социальной сети для обмена фотографиями

API для загрузки публикаций с фото с возможностью комментировать и ставить лайки. Прототип фронтенда приложения на скрине:

![Design](social_network/Design.png)

### Реализация

Посты состоят из текста и фотографии, также сохраняется время создания поста.

Публикации могут создаваться только авторизованными пользователями, редактировать же публикацию может только её автор.

Комментарии могут быть написаны к определённой публикации, оставлять их могут только авторизованные пользователи. 
Сам комментарий состоит из текста и даты его публикации.

Помимо комментариев, пользователи также могут оставлять реакцию на публикацию в виде лайка.

### Инструкция по запуску проекта

Для запуска проекта необходимо

* установить зависимости:
```python
pip install -r requirements.txt
```
* необходимо создать базу в postgres и прогнать миграции:
```python
manage.py migrate
```
* команда для запуска приложения:
```python
python manage.py runserver
```
* при создании моделей или их изменении необходимо выполнить следующие команды:
```python
python manage.py makemigrations
python manage.py migrate
```
*  при создании superuser необходимо выполнить следующую команду:
```python
python manage.py createsuperuser
```
* для создания пользователей и получения токенов авторизации можно воспользоваться административной панелью.