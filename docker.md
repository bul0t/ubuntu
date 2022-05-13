# Docker
Руководство Docker

## Установка
Установка Docker на Linux Ubuntu 20
- https://unixhost.pro/clientarea/knowledgebase/95/kak-ustanovit-docker-ubuntu-2004.html
- Образы контейнеров https://hub.docker.com/

## Команды
- `sudo systemctl status docker` - проверяем запущен ли докер **жмём Ctrl+Z**
- `sudo docker run hello-world` - загружаем и запускаем тестовый контейнер (проверка работы докера)
- `sudo docker search web` - поиск образов по словосочетанию, например `web`
- `sudo docker pull wordpress` - загружаем контейнер wordpress
- `sudo docker images` - показывает список загруженных контейнеров (образов)
- `sudo docker ps` - показать список активных контейнеров
- `sudo docker ps -a` - показать список контейнеров системы
- `docker ps -l` - показать список последних созданных контейнеров
- `docker start ID or NAME` - запуск контейнера по его ID или имени
- `docker stop ID or NAME` - остановка контейнера по его ID или имени
- `docker rm ID or NAME` - удаление контейнера по его ID или имени
- `exit` - выход из контейнера

## Workflow
Начнем работать с PHP:
- `sudo docker pull php` - загружаем контейнер PHP
- `sudo docker run php` - запускаем загруженный контейнер
