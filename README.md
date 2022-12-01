### Описание проекта:


Проект «API для Yatube»

Позволяет создавать, просматривать и комментировать посты.
Просматривать группы и подписываться на авторов.

### Как запустить проект:


Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

### Примеры запросов:

Создание публикации
Добавление новой публикации в коллекцию публикаций. Анонимные запросы запрещены.

REQUEST application/json


[POST].../api/v1/posts/

{
  "text": "string",
  "image": "string",
  "group": 0
}

RESPONSES:

{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2019-08-24T14:15:22Z",
"image": "string",
"group": 0
}

Подробная документация в формате ReDoc доступна по адресу .../redoc/