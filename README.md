# REST API для проекта YAMDB

## Описание проекта.

- YamDB - это проект, позволяющий оставлять отзывы, комментарии и оценки к различным произведениям, будь то фильмы, книги, музыка или что бы то ни было.

## Как скачать, установить и запустить проект:

Склонируйте репозиторий в рабочее пространство командой:

```
git clone https://github.com/Nizzerato/infra_sp2.git
```

Запустите проект командой:

```
docker-compose up -d --build`
```

Глобальные настройки проекта находятся в файле `api_yamdb/settings.py`

# Создание суперпользователя

- Выполните команду:

```
docker-compose exec -ti container_name python manage.py createsuperuser
```

# Наполнение базы данных тестовыми данными

- Выполните команду:

```
docker-compose exec -ti container_name python manage.py loaddata fixtures.json
```

## Пример наполнения .env-файла:

```
SECRET_KEY=(Этот ключ находится в настройках проекта)
DB_ENGINE=django.db.backends.postgresql
DB_NAME=postgres
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
DB_HOST=db
DB_PORT=5432
```

# Tech
**Python**, **Django**, **Rest Framework**, **Simple-JWT**, **NGINX**, **Docker**, **Gunicorn**
