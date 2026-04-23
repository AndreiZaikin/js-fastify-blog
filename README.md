![Push](https://github.com/AndreiZaikin/js-fastify-blog/actions/workflows/push.yml/badge.svg)

# js-fastify-blog

Учебный проект по упаковке приложения в Docker Compose.

## Описание

Приложение — блог на Fastify. Проект демонстрирует настройку Docker-окружения с разделением конфигураций для тестов и разработки, сборку production-образа и непрерывную интеграцию через GitHub Actions.

## Структура

- `app/` — исходный код приложения
- `Dockerfile` — образ для разработки
- `Dockerfile.production` — образ для продакшена
- `docker-compose.yml` — базовая конфигурация (тесты)
- `docker-compose.override.yml` — конфигурация для разработки
- `Makefile` — команды для управления

## Команды

- `make test` — запуск тестов
- `make dev` — запуск приложения в режиме разработки (порт 8080)
- `make down` — остановка контейнеров

## CI/CD

Автоматический прогон тестов и публикация образа на Docker Hub при пуше в main.
