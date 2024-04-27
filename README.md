# Check project

## Описание проекта

Сервисы, связанные посредством Apache Kafka, для обработки и анализа чеков покупок. Первый сервис отвечает за прием, валидацию и запись чеков в журнал, а также их передачу второму сервису. Второй сервис разбивает содержимое чеков на привязку к местам покупок, считает аналитику и предоставляет данные по API.

## Технологии

- Linux
- Python
- pip+env
- Django
- DRF
- PostgreSQL
- Redis
- Celery
- Docker
- Docker Compose

## Зависимости

Зависимости, необходимые для работы проекта, указаны в файлах requirements.txt каждого сервиса.
Чтобы установить зависимости, используйте команду `pip install -r requirements.txt`

## Документация

Документация находится по ссылкам:
1. Swagger `api/schema/swagger-ui/`

## Как запустить проект

Для запуска проекта необходимо выполнить следующие шаги:
1. При необходимости установите Docker и Docker Compose с помощью инструкции https://docs.docker.com/engine/install/
2. Cклонируйте репозиторий `git clone git@github.com:UlianaSem/check_project.git`
3. Перейдите в созданный каталог `cd check_project`
4. Склонируйте репозитории `git clone git@github.com:UlianaSem/check_producer.git` и `git clone git@github.com:UlianaSem/check_consumer.git`
5. Создайте файлы .env `nano check_producer/.env` и `nano check_consumer/.env` и заполните их, используя образец из файла .env.example 
6. Соберите образ с помощью команды `docker-compose build`
7. Запустите контейнеры с помощью команды `docker-compose up`

## Авторы

UlianaSem

## Связь с авторами

https://github.com/UlianaSem/
