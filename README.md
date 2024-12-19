![example workflow](https://github.com/vvsmirnov19/kittygram_final/actions/workflows/main.yml/badge.svg)

## Описание проекта
Kittygram - проект социальной сети с возможностью публикации фотографий котиков и основной информации о них.

![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white) ![DjangoREST](https://img.shields.io/badge/DJANGO-REST-ff1709?style=for-the-badge&logo=django&logoColor=white&color=ff1709&labelColor=gray) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)

## Стек
- python 3.9
- Django 3.2.3
- DRF 3.12.4
- Nginx
- Docker

## Как развернуть проект
На машине, в которой будет развернут проект, необходимы установленные Git и Docker.

1. Копируем проект на машину
```bash 
git clone https://github.com/vvsmirnov19/kittygram_final.git
```
2. Переходим в директорию проекта
```bash
cd kittygram_final
```
3. Создаем файл с переменными окружения .env
Он должен содержать следующие переменные:
POSTGRES_USER
POSTGRES_PASSWORD
POSTGRES_DB
DB_HOST
DB_PORT
SECRET_KEY
ALLOWED_HOSTS
DEBUG
DB_POSTGRE
4. Для сборки из текущего репозитория выполняем:
```bash
docker compose up -d
```
Для сборки из Docker Hub выполняем:
```bash
docker compose -f docker-compose.production.yml up -d
```

Автор [Валерий Смирнов] (https://github.com/vvsmirnov19)

#  Как работать с репозиторием финального задания

## Что нужно сделать

Настроить запуск проекта Kittygram в контейнерах и CI/CD с помощью GitHub Actions

## Как проверить работу с помощью автотестов

В корне репозитория создайте файл tests.yml со следующим содержимым:
```yaml
repo_owner: ваш_логин_на_гитхабе
kittygram_domain: полная ссылка (https://доменное_имя) на ваш проект Kittygram
taski_domain: полная ссылка (https://доменное_имя) на ваш проект Taski
dockerhub_username: ваш_логин_на_докерхабе
```

Скопируйте содержимое файла `.github/workflows/main.yml` в файл `kittygram_workflow.yml` в корневой директории проекта.

Для локального запуска тестов создайте виртуальное окружение, установите в него зависимости из backend/requirements.txt и запустите в корневой директории проекта `pytest`.

## Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в `tests.yml`.
- Проект Kittygram доступен по доменному имени, указанному в `tests.yml`.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в телеграм.
- В корне проекта есть файл `kittygram_workflow.yml`.
