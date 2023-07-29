# Kittygram — социальная сеть для обмена фотографиями любимых питомцев. Это полностью рабочий проект, который состоит из бэкенд-приложения на Django и фронтенд-приложения на React.

[![.github/workflows/main.yml](https://github.com/Anastasia-Iziumskaya/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/Anastasia-Iziumskaya/kittygram_final/actions/workflows/main.yml)

![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white) ![DjangoREST](https://img.shields.io/badge/DJANGO-REST-ff1709?style=for-the-badge&logo=django&logoColor=white&color=ff1709&labelColor=gray) ![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)

## Описание проекта

Данный проект создан в процессе обучения на платформе Яндекс Практикум. Зарегистрированные пользователи могут делиться фотографиями своих (и не только) котиков, а также рассказать об их имени, окрасе и достижениях.

## Технологии

1) Django==3.2.3 
2) Python 3.9
3) Nginx
4) Gunicorn

## Запуск проекта
Клонируем репозиторий:
```bash
git clone git@github.com:anastasia-iziumskaya/kittygram_final.git
```
Переходим в директорию с проектом:
```bash
cd kittygram_final/
```
Выполняем запуск:
```bash
sudo docker compose -f docker-compose.yml up
```
Выполняем сбор статистики и применяем миграции бэкенда:
```bash
sudo docker compose -f [имя-файла-docker-compose.yml] exec backend python manage.py migrate
sudo docker compose -f [имя-файла-docker-compose.yml] exec backend python manage.py collectstatic
sudo docker compose -f [имя-файла-docker-compose.yml] exec backend cp -r /app/collected_static/. /static/static/
```
## Автор
Анастасия Изюмская

