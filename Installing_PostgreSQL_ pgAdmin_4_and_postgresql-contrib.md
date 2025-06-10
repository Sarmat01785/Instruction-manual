# Установка `PostgreSQL`, `pgAdmin4` и `postgresql-contrib` на Alt Linux

Данная инструкция предназначена для тех, кто хочет быстро и качественно настроить `PostgreSQL`-сервер с поддержкой расширенных функций и удобным веб-интерфейсом для администрирования `(pgAdmin4)` на дистрибутиве `Alt Linux`.

## Требования:

- Система на базе Alt Linux (используется в примере версия ALT Workstation K 11.1 Nemorosa).
- Доступ к терминалу с правами root.

## Основные этапы установки:

1. Установка PostgreSQL
2. Установка расширений (contrib)
3. Установка и настройка pgAdmin4
4. Настройка сервисов и проверка работоспособности

## 🛠️ Установка `PostgreSQL`

1. Обновите списки пакетов:

```bash
sudo apt-get update
```

2. Установите последнюю стабильную версию `PostgreSQL`:

```bash
sudo apt-get install postgresql17
```

3. После успешной установки проведите первичную инициализацию базы данных:

```bash
sudo su - postgres
initdb -D /var/lib/pgsql/data
exit
```

4. Запустите службу `PostgreSQL`:

```bash
sudo systemctl start postgresql.service
```

5. Добавьте `PostgreSQL` в автозагрузку:

```bash
sudo systemctl enable postgresql.service
```

## ⚙️ Установка расширений `(postgresql-contrib)`

Расширения включают дополнительные модули и библиотеки для улучшения функциональности `PostgreSQL`.

1. Установите пакет с дополнительными модулями:

```bash
sudo apt-get install postgresql17-contrib
```

## 🖥️ Установка и настройка `pgAdmin4`

`PgAdmin4` — популярный графический интерфейс для администрирования `PostgreSQL`.

1. Установите `pgAdmin4`:

```bash
sudo apt-get install pgadmin4
```

2. Запустите службу `pgAdmin4`:

```bash
sudo systemctl start pgadmin4.service
```

3. Добавьте `pgAdmin4` в автозагрузку:

```bash
sudo systemctl enable pgadmin4.service
```

## 👨‍💻 Настройка пользователей и баз данных

### Создание пользователя и базы данных

1. Подключитесь к `PostgreSQL` от имени пользователя `postgres`:

```bash
sudo su - postgres
psql
```

2. Создайте нового пользователя:

```bash
CREATE USER myuser WITH PASSWORD 'mypassword';
```

3. Создайте новую базу данных и назначьте владельца:

```bash
CREATE DATABASE mydatabase OWNER myuser;
```

4. Дайте пользователю полные права на базу данных:

```bash
GRANT ALL PRIVILEGES ON DATABASE mydatabase TO myuser;
```

5. Выход из консоли `PostgreSQL`:

```bash
\q
```

6. Вернитесь в обычную оболочку:

```bash
exit
```
