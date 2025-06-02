### Установка `Docker-Engine` и `Docker Compose` на операционной системе `ALT Linux` 

```bash
sudo apt-get update && sudo apt-get install docker-engine # проверяет наличие новых версий пакетов, а затем устанавливает Docker Engine.
```

#### Проверка версии `Docker`

```bash
docker --version # выводим информацию о текущей установленной версии Docker
```


### Установка `Docker Compose` на `ALT Linux` 

1. Убедитесь, что у вас установлен `Python` и `pip`. Вы можете проверить их наличие, выполнив следующие команды:

```bash
python3 --version # выводим информацию о текущей версии Python
```

```bash
pip --version # выводим информацию о текущей версии pip
```

2. Установите `Docker Compose`, выполнив следующие команды:

```bash
sudo curl -L "https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose # Загружаем последнюю версию Docker Compose (версия v2.33.1) из официального репозитория GitHub, сохранив файл в каталог `/usr/local/bin/`, предоставив доступ всем пользователям системы.
```

```bash
sudo chmod +x /usr/local/bin/docker-compose # Делаем файл исполняемым.
```

3. Проверьте, был ли `Docker Compose` успешно установлена, выполнив:

```bash
docker-compose --version # Выводим текущию версию docker-compose
```

4. Убедитесь, что сервис `Docker` запущен:

```bash
sudo service docker status # Просмотр текущего состояния службы Docker 
```

5. Если сервис `Docker` не запущен, запустите его:

```bash
sudo service docker start # используется для запуска службы Docker
```

6. Проверьте статус сервиса `Docker`:

```bash
sudo service docker status # просмотр статус службы Docker
```

7. Добавьте вашего пользователя в группу docker для выполнения Docker команд без `sudo`:

```bash
sudo usermod -aG docker $USER  # Замените $USER на ваше имя пользователя
```
8. Перезапустите вашу сессию для применения изменений.

9. Проверьте, что ваш пользователь добавлен в группу `docker`:

```bash
groups
```

10. Включите автозапуск службы `Docker` при загрузке системы:

```bash
sudo systemctl enable docker # добавляет службу Docker в автозагрузку системы.
```

11. Теперь `Docker` должен быть готов к использованию. Попробуйте выполнить команду `docker run hello-world`, чтобы убедиться, что `Docker` работает корректно.

### Удаление `Docker Compose` c `ALT Linux`

1. Если у вас установлен Docker Compose, вы можете удалить его, выполнив следующие команды:

```bash
sudo rm /usr/local/bin/docker-compose # выполняет удаление файла Docker Compose из каталога /usr/local/bin/.
```

2. Также рекомендуется удалить симлинк на версию `Docker Compose`, если он был создан:

```bash
sudo rm /usr/local/bin/docker-compose-2.33.1 # удаляет конкретный файл Docker Compose версии 2.33.1 из системного каталога /usr/local/bin/.
```

3. Убедитесь, что `Docker Compose` успешно удален, выполнив:

```bash
docker-compose --version # Выводим текущию версию docker-compose
```

   Если после удаления вы видите сообщение об ошибке, это означает, что `Docker Compose` был успешно удален.

4. Опционально, вы также можете удалить настройки и файлы `Docker Compose`, если они больше не нужны.

5. После удаления `Docker Compose`, рекомендуется перезапустить систему или завершить текущую сессию для полного завершения удаления.

6. Теперь `Docker Compose` должен быть удален с вашей системы.