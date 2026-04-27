![Push](https://github.com/AndreiZaikin/js-fastify-blog/actions/workflows/push.yml/badge.svg)

# js-fastify-blog

Учебный проект по упаковке приложения в Docker Compose

## Описание

Приложение — блог на Fastify. Проект демонстрирует настройку Docker-окружения с разделением конфигураций для тестов и разработки, сборку production-образа и непрерывную интеграцию через GitHub Actions.

## Требования

- Docker (с поддержкой Docker Compose)
- WSL 2 (для Windows)

## Запуск

```bash
# Клонирование репозитория
git clone git@github.com:AndreiZaikin/js-fastify-blog.git
cd js-fastify-blog

# Запуск в режиме разработки
make dev
```
Приложение будет доступно по адресу *https://localhost*

## Тесты

```bash
make test
```

## Остановка

```bash
make down
```

## Docker Hub

Образ приложения: [*andrei026/js-fastify-blog*](https://hub.docker.com/r/andrei026/js-fastify-blog)

## Структура

- `app/` — исходный код приложения
- `Dockerfile` — образ для разработки
- `Dockerfile.production` — образ для продакшена
- `docker-compose.yml` — базовая конфигурация (тесты)
- `docker-compose.override.yml` — конфигурация для разработки
- `services/caddy/Caddyfile` — конфигурация Caddy
- `Makefile` — команды для управления

## Команды

- `make dev` — запуск приложения в режиме разработки
- `make test` — запуск тестов
- `make down` — остановка контейнеров

## CI/CD

Автоматический прогон тестов и публикация образа на Docker Hub при пуше в main
