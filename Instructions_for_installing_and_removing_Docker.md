### Установка `Docker-Engine` и `Docker Compose` на операционной системе `ALT Linux` 

```bash
sudo apt-get update && sudo apt-get install docker-engine
```

#### Проверка версии `Docker`

```bash
docker --version
```

### Установка `Docker Compose` Вариант 1

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


### Установка `Docker Compose` Вариант 2

#### Установка `Docker Compose` на `ALT Workstation K 10.4`

1. Убедитесь, что у вас установлен `Python` и `pip`. Вы можете проверить их наличие, выполнив следующие команды:

```bash
python --version
```

```bash
pip --version
```

2. Установите `Docker Compose`, выполнив следующие команды:

```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

```bash
sudo chmod +x /usr/local/bin/docker-compose
```

3. Проверьте, был ли `Docker Compose` успешно установлена, выполнив:

```bash
docker-compose --version
```

4. Убедитесь, что сервис `Docker` запущен:

```bash
sudo service docker status
```

5. Если сервис `Docker` не запущен, запустите его:

```bash
sudo service docker start
```

6. Проверьте статус сервиса `Docker`:

```bash
sudo service docker status
```

7. Добавьте вашего пользователя в группу docker для выполнения Docker команд без `sudo`:

```bash
sudo usermod -aG docker $USER
```
8. Перезапустите вашу сессию для применения изменений.

9. Проверьте, что ваш пользователь добавлен в группу `docker`:

```bash
groups
```

10. Включите автозапуск службы `Docker` при загрузке системы:

```bash
sudo systemctl enable docker
```

11. Теперь `Docker` должен быть готов к использованию. Попробуйте выполнить команду `docker run hello-world`, чтобы убедиться, что `Docker` работает корректно.

### Удаление `Docker Compose` на `ALT Workstation K 10.4` Вариант 2

1. Если у вас установлен Docker Compose, вы можете удалить его, выполнив следующие команды:

```bash
sudo rm /usr/local/bin/docker-compose
```

2. Также рекомендуется удалить симлинк на версию `Docker Compose`, если он был создан:

```bash
sudo rm /usr/local/bin/docker-compose-1.29.2
```

3. Убедитесь, что `Docker Compose` успешно удален, выполнив:

```bash
docker-compose --version
```

   Если после удаления вы видите сообщение об ошибке, это означает, что `Docker Compose` был успешно удален.

4. Опционально, вы также можете удалить настройки и файлы `Docker Compose`, если они больше не нужны.

5. После удаления `Docker Compose`, рекомендуется перезапустить систему или завершить текущую сессию для полного завершения удаления.

6. Теперь `Docker Compose` должен быть удален с вашей системы.