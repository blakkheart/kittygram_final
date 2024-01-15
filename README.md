Kittygram Final - это веб-приложение для публикации и просмотра фотографий котиков. Пользователи могут создавать и просматривать котиков, загружать их фотографии и ставить им достижения.


## Описание проекта

Сайт с возможностью публикации фотографий котов и их достижений.

## Технологии

- Фронтенд: React
- Бэкенд: Django Rest Framework
- База данных: PostgreSQL
- Nginx
- Docker
- Gunicorn
- Github actions


## Запуск проекта

Выполняем запуск:

```bash
sudo docker compose -f docker-compose.yml up
```

## После запуска: миграции, сбор статики



```bash
sudo docker compose -f [имя-файла-docker-compose.yml] exec backend python manage.py migrate

sudo docker compose -f [имя-файла-docker-compose.yml] exec backend python manage.py collectstatic

sudo docker compose -f [имя-файла-docker-compose.yml] exec backend cp -r /app/collected_static/. /backend_static/static/
```

Веб-приложение будет доступно по адресу:

```
http://localhost:9000/
```
