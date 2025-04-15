# Основные команды `Docker`

`Docker` - это платформа для разработки, доставки и запуска приложений в контейнерах. Ниже представлены основные команды Docker:

## Управление контейнерами

### Создание контейнера:

```bash
docker create [OPTIONS] IMAGE [COMMAND] [ARG...]
```

### Запуск контейнера:

```bash
docker start [OPTIONS] CONTAINER
```

### Остановка контейнера:

```bash
docker stop [OPTIONS] CONTAINER
```

### Просмотр запущенных контейнеров:

```bash
docker ps
```

### Просмотреть все контейнеры (включая остановленные):

```bash
docker ps -a
```


### Получение доступа к командной оболочке контейнера:

```bash
docker exec [OPTIONS] CONTAINER COMMAND
```

### Проверка журналов контейнера:

```bash
docker logs container_id_or_name
```

### Перезапуск контейнера:

```bash
docker restart [OPTIONS] CONTAINER
```

### Коммит контейнера в образ:

```bash
docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]
```

### Просмотр информации о контейнере:

```bash
docker inspect [OPTIONS] CONTAINER
```

### Удаление контейнера:

```bash
docker rm [OPTIONS] CONTAINER
```

## Авторизация и аутентификация

### Вход в Docker Hub:

```bash
docker login [OPTIONS] [SERVER]
```

### Выход из Docker Hub

```bash
docker logout [SERVER]
```

## Управление образами

### Создание образа из Dockerfile:

```bash
docker build [OPTIONS] PATH | URL | -
```

### Список доступных образов:

```bash
docker images
```

### Загрузка образа из репозитория:

```bash
docker pull NAME[:TAG]
```

### Загрузка образа в репозиторий:

```bash
docker push NAME[:TAG]
```

### Добавление тега к образу:

```bash
docker tag IMAGE_NAME NEW_IMAGE_NAME:TAG
```

### Удаление образа:

```bash
docker rmi IMAGE_NAME
```

## Управление сетями

### Создание сети:

```bash
docker network create NETWORK_NAME
```

### Список сетей:

```bash
docker network ls
```

### Подключение контейнера к сети:

```bash
docker network connect NETWORK_NAME CONTAINER
```

## Управление томами

### Создание тома:

```bash
docker volume create VOLUME_NAME
```

### Список томов:

```bash
docker volume ls
```

### Удаление тома:

```bash
docker volume rm VOLUME_NAME
```

Для получения более подробной информации можно посмотреть официальную документацию `Docker`: https://docs.docker.com/
