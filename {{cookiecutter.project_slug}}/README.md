### Development

Executar

```sh
$ make dev
```
ou

```sh
$ docker-compose up --build
```

### Production

Uses gunicorn + nginx.

Executar

```sh
$ make prod
```
ou

```sh
$ docker-compose -f docker-compose.prod.yml up -d --build
```
