# API для проекта YaTube
## Описание проекта API Yatube:
API для проекта Yatube. Зарегестрированные пользователи могут создавать, 
редактировать и удалять записи, просматривать 
и комментировать записи других пользователей и подписываться на других авторов. 


## Технологии:
    Django 2.2.16
    Python 3.7
    djoser 2.1
    django rest framework
    Django ORM
    Simple JWT

## Как запустить проект с Windows
#### Запустить проект можно следующим образом:

- Клонировать репозиторий и перейдите в него в командной строке:

```
git clone https://github.com/Valerii22/api_final_yatube.git
```

```
cd api_final_yatube
```

- Установить виртуальное окружение:

```
python -m venv env
```

- Запустить виртуальное окружение
```
env\Scripts\activate
```

- Обновить pip:

```
python -m pip install --upgrade pip
```

- Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

- Выполнить миграции:

```
python manage.py migrate
```

- Запустите проект:

```
python manage.py runserver
```



## Примеры запросов

- GET: /api/v1/posts/ 

        Request:
        [ 
           {
                "id": 1, 
                "author": "author", 
                "image":"" 
                "text": "text", 
                "pub_date": "pub_date", 
                "group": null
            },
        ]

- POST: /api/v1/posts/ :

        {
           "text": "string",
           "image": "string",
           "group": 0
        }

        Request:

        {
        "id": 0,
        "author": "string",
        "text": "string",
        "pub_date": "2022-12-17T18:15:22Z",
        "image": "string",
        "group": 0
        }


- Остальные возможные запросы можно посмотреть 
    http://127.0.0.1:8000/redoc/