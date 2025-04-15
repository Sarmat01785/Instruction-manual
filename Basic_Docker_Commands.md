{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Основные команды Docker"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "1. Создание контейнера:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "```bash\n",
    "docker create [OPTIONS] IMAGE [COMMAND] [ARG...]\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "2. Запуск контейнера:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "```bash\n",
    "docker start [OPTIONS] CONTAINER\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "3. Остановка контейнера:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "```bash\n",
    "docker stop [OPTIONS] CONTAINER\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "4. Просмотр запущенных контейнеров:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "```bash\n",
    "docker ps\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "5. Просмотр всех контейнеров (включая остановленные):"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "```bash\n",
    "docker ps -a\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "6. Удаление контейнера:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "```bash\n",
    "docker rm [OPTIONS] CONTAINER\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "7. Получение доступа к командной оболочке контейнера:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "```bash\n",
    "docker exec [OPTIONS] CONTAINER COMMAND\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "8. Создание образа из Dockerfile:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "```bash\n",
    "docker build [OPTIONS] PATH | URL\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "9. Загрузка образа из репозитория:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "```bash\n",
    "docker pull NAME[:TAG]\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "10. Загрузка образа в репозиторий:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "```bash\n",
    "docker push NAME[:TAG]\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "| Команда             | Описание                                                       |\n",
    "|---------------------|-----------------------------------------------------------------|\n",
    "| `docker run`        | Запуск контейнера из образа                                    |\n",
    "| `docker ps`         | Просмотр запущенных контейнеров                                |\n",
    "| `docker ps -a`      | Просмотр всех контейнеров (включая остановленные)              |\n",
    "| `docker images`     | Список всех образов на локальной машине                        |\n",
    "| `docker build`      | Сборка нового образа из Dockerfile                             |\n",
    "| `docker stop`       | Останавливает контейнер                                        |\n",
    "| `docker start`      | Запускает остановленный контейнер                              |\n",
    "| `docker rm`         | Удаляет контейнер                                              |\n",
    "| `docker rmi`        | Удаляет образ                                                  |\n",
    "| `docker exec`       | Выполнение команды внутри работающего контейнера                |\n",
    "| `docker commit`     | Сохранение изменений в контейнере как новый образ               |\n",
    "| `docker inspect`    | Просмотр подробной информации о контейнере или образе           |\n",
    "| `docker logs`       | Просмотр логов контейнера                                      |\n",
    "| `docker network`    | Управление сетями (создание, удаление, просмотр)                |\n",
    "| `docker volume`     | Управление томами (создание, удаление, просмотр)                |\n",
    "| `docker push`       | Загрузка образа в реестр (например, Docker Hub)                 |\n",
    "| `docker pull`       | Загрузка образа из реестра                                     |\n",
    "| `docker search`     | Поиск образов в реестре Docker Hub                             |\n",
    "| `docker tag`        | Присвоение тега образу (например, для версии)                   |\n",
    "| `docker login`      | Вход в Docker Hub или другой реестр                            |\n",
    "| `docker logout`     | Выход из Docker Hub или другого реестра                        |"
   ]
  }
 ],
 "metadata": {
  "language_info": {
   "name": "python"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
