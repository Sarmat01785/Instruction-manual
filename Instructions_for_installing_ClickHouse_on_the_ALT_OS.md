# Инструкция по установке `ClickHouse` на ОС `ALT Workstation K 11.1 (Nemorosa)`

Данная пошаговая инструкция предназначена для установки и настройки ClickHouse на дистрибутив Alt Linux (Workstation K 11.1).

## 📌 Предварительные требования:

Перед началом убедитесь, что ваша система удовлетворяет следующим требованиям:

- Версия ОС: **ALT Workstation K 11.1 (x86_64)**.
- Доступ к интернету для загрузки необходимых пакетов.
- Пользовательские права администратора (root).

## 🛠️ Установка ClickHouse

### Шаг 1: Обновление списка пакетов

Первым делом обновите списки пакетов:

```bash
sudo apt-get update
```

### Шаг 2: Установка основного пакета `ClickHouse`

Установите базовую часть `ClickHouse`, включающую сервер и общие компоненты:

```bash
sudo apt-get install clickhouse-server
```

Процесс установки загрузит необходимые файлы и развернет сервер `ClickHouse`.

### Шаг 3: Проверка успешной установки

Проверьте успешность установки, проверив доступность программы-сервер:

```bash
which clickhouse-server
```

Результатом должна стать директория размещения бинарника, например:

```
/usr/bin/clickhouse-server
```

### Шаг 4: Настройка автозапуска

По умолчанию `ClickHouse` устанавливается без автоматического старта при загрузке системы. Чтобы включить автозагрузку, выполните:

```bash
sudo systemctl enable clickhouse-server
```

### Шаг 5: Запуск `ClickHouse`

Теперь запустите сервер вручную:

```bash
sudo systemctl start clickhouse-server
```

Проверяйте статус службы:

```bash
sudo systemctl status clickhouse-server
```

При правильном выполнении отобразится сообщение вида:

```
Active: active (running)
```

## 🚀 Тестирование ClickHouse

### Шаг 6: Использование клиента `ClickHouse`

Для взаимодействия с сервером используем встроенный клиент `ClickHouse`. Для начала установим клиент:

```bash
sudo apt-get install clickhouse-client
```

Теперь откройте клиент и соединитесь с сервером:

```bash
clickhouse-client
```

Появится приглашение для отправки запросов:

```
ClickHouse client version ...
Connecting to localhost:9000 as user default.
Connected to ClickHouse server version ...
```

Попробуйте простейший запрос для проверки версии:

```sql
SELECT version();
```

Ожидаемый результат:

```
┌─version()─┐
│ 25.x.y.z  │
└───────────┘
```

## 🧑‍💻 Примеры простых операций

### 1. Создание первой таблицы

Создаем таблицу для хранения численных значений:

```sql
CREATE TABLE example_numbers (
    number_id Int32,
    value Float64
) ENGINE = MergeTree()
ORDER BY number_id;
```

### 2. Вставка данных

Добавляем значения в таблицу:

```sql
INSERT INTO example_numbers VALUES (1, 3.14);
```

### 3. Чтение данных

Проверяем содержание таблицы:

```sql
SELECT * FROM example_numbers;
```

## ⚙️ Основные операции

- **Перезапуск ClickHouse:**  
  ```bash
  sudo systemctl restart clickhouse-server
  ```

- **Просмотр журнала ошибок:**  
  ```bash
  journalctl -u clickhouse-server
  ```

- **Проверка конфигурации:**  
  Файл конфигурации расположен по пути `/etc/clickhouse-server/config.xml`.



