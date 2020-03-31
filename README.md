# CCLS Reporting Backend

#### First time setup

```
cp .env.example .env
docker-compose build --no-cache
docker-compose up -d
docker-compose exec app bash
cd /application/server
python manage.py migrate
python manage.py createsuperuser
```

#### To bring up/down containers

```sh
docker-compose up -d   #(server starts here, at http://localhost:8000/)
docker-compose ps
docker-compose down
```

#### To get inside containers

```sh
docker-compose exec app bash
cd /application/server
```

#### To see logs

```sh
docker-compose logs -f --tail 1000
```

# Tools added

## [<u>sentry</u>](https://sentry.io/for/python/)

in settings.py file:

```
SENTRY_DSN=<% DSN from sentry server %>
```

## [<u>django-rest-framework</u>](https://www.django-rest-framework.org/)

To view browsable APIs:

http://localhost:8000/

## [<u>django-sql-explorer</u>](https://github.com/groveco/django-sql-explorer)

To explore:

http://localhost:8000/explorer/

## [<u>swagger</u>](https://swagger.io/)

To Swag:

http://localhost:8000/swagger/

http://localhost:8000/redoc/
