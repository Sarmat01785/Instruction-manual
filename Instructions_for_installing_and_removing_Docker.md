### Установка `Docker-Engine` и `Docker Compose` на операционной системе `ALT Linux` 

```bash
sudo apt-get update && sudo apt-get install docker-engine
```

#### Проверка версии `Docker`

```bash
docker --version
```

### Установка `Docker Compose`

```bash
sudo pip3 install docker-compose
```

#### Проверка версии `Docker Compose`

```bash
docker-compose --version
```

### Описание шагов:

1. Обновление списка пакетов:

```bash
sudo apt-get update
```

2. Установка `Docker Engine`:

```bash
sudo apt-get install docker-engine
```

3. Проверка установленной версии `Docker`:

```bash
docker --version
```

4. Установка `Docker Compose` через `pip`:

```bash
sudo pip3 install docker-compose
```
5. Проверка версии установленного `Docker Compose`:

```bash
docker-compose --version
```
### Удаление `Docker-Engine` и `Docker Compose` на операционной системе `ALT Linux` 

Для удаления `Docker` с операционной системы следуйте указанным ниже шагам:

1. Остановите и удалите все запущенные контейнеры `Docker`:

```bash
sudo docker stop $(docker ps -a -q)
```

```bash
sudo docker rm $(docker ps -a -q)
```

2. Удалите все образы `Docker`:

```bash
sudo docker rmi $(docker images -q)
````

3. Удалите установленный `Docker Engine`:

```bash
sudo apt-get remove docker-ce
```

4. Удалите остаточные пакеты `Docker`:

```bash
sudo apt-get autoremove
```

5. Удалите Docker `Compose`:

```bash
sudo pip3 uninstall docker-compose
```

6. Удалите ссылку на `Docker Compose` (если существует):

```bash
sudo rm /usr/local/bin/docker-compose
```

7. Удалите ссылку на `Docker` (если существует):

```bash
sudo rm /usr/bin/docker
```
P.S. После выполнения всех указанных выше шагов Docker должен быть успешно удален с вашей операционной системы.