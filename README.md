## Cookiecutter for Django with Celery, Celery Beat, Postgres, Redis, Gunicorn, and Nginx

### O que este projeto faz?

Cria um projeto Django com banco de dados Postgres com ambientes de desenvolvimento e produção previamente configurados para Docker.

Este projeto usa como base o projeto do [tutorial](https://testdriven.io/dockerizing-django-with-postgres-gunicorn-and-nginx).

Além da stack padrão, o template já traz configurados um worker e um scheduler do Celery (celery beat) utilizando Redis como broker/result backend, e instala o pacote [django-widget-tweaks](https://github.com/jazzband/django-widget-tweaks) para facilitar ajustes em formulários.

### Como usar este projeto?

Para criar um novo projeto basta executar:

cookiecutter https://github.com/rogeriothe/django-caipora

### Development

Executar

```sh
$ make dev
```

ou

```sh
$ docker compose up --build
```

### Production

Uses gunicorn + nginx.

Executar

```sh
$ make prod
```

ou

```sh
$ docker compose -f docker-compose.prod.yml up -d --build
```
### Sugestões

- Comentar no docker-compose.prod.yml os containers redis, worker, beat e flower caso não vá usar o Celery.
