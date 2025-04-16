# Установка и обновление `Visual Studio Code` на ALT Workstation K 10.4 (Sorbaronia Mitschurinii)

## Установка

1. Скачайте `.rpm` файл для `Visual Studio Code` со страницы [Visual Studio Code Downloads](https://code.visualstudio.com/download). Выберите версию для Red Hat, Fedora, CentOS.

2. Перейдите в папку, где вы сохранили `.rpm` файл. Вы можете использовать команду `cd` в терминале для этого. Например, если файл был скачан в папку `Загрузки`, вы можете ввести `cd Загрузки`.

3. Установите `Visual Studio Code`, используя следующую команду:

```bash
sudo apt-get install ./file-name.rpm
```

(Замените `file-name.rpm` на имя скачанного файла.)

## Обновление

Процесс обновления Visual Studio Code похож на установку:

1. Скачайте новый `.rpm` файл с официального сайта [Visual Studio Code](https://code.visualstudio.com/download) (выберите версию для Red Hat, Fedora, CentOS).

2. Откройте терминал и перейдите в папку, где вы сохранили новый `.rpm` файл.

3. Запустите команду установки с новым файлом:

```bash
sudo apt-get install ./new-file-name.rpm
```

(Замените `new-file-name.rpm` на имя скачанного файла.)

Это обновит `Visual Studio Code` до новой версии.