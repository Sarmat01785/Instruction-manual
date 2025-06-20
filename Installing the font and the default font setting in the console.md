## Инструкция по установке шрифта `Fira Code Medium Nerd Font Complete` на операционную систему `ALT Workstation K 11.1` и настройка шрифта в `Konsole` по умолчанию.

1. Скачайте шрифт:
   - Скачайте файл Fira Code Medium Nerd Font Complete.ttf с помощью этой ссылки [FiraCode](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/FiraCode.zip).

2. Разархивируйте файл:
   - Перейдите в директорию куда скачали `FiraCode`
   - Разархивируйте скачанный архив `FiraCode.zip` с помощью команды:

```bash
unzip FiraCode.zip
```

3. Копирование шрифта:
   - Откройте терминал и выполните команду для копирования файла шрифта в системную папку шрифтов:

```bash
sudo cp "/home/executor/Загрузки/Fira Code Medium Nerd Font Complete.ttf" /usr/share/fonts/
```

4. Обновление кэша шрифтов:
   - После копирования файла, обновите кэш шрифтов с помощью команды:

```bash
fc-cache -f -v
```
5. Настройка шрифта в `Konsole`:
   - Измените шрифт в конфигурации Konsole на Fira Code Medium Nerd Font Complete с помощью следующих команд:

```bash
kwriteconfig6 --file konsolerc --group 'General' --key 'font' 'Fira Code Medium Nerd Font Complete,12,-1,5,50,0,0,0,0,0'
```
6. Проверка установленного шрифта:
      
   - Для проверки установленного шрифта выполните команду:

```bash
kreadconfig6 --file konsolerc --group 'General' --key 'font'
```

7. Завершение:
   - После выполнения этих шагов, шрифт Fira Code Medium Nerd Font Complete успешно установлен в вашу операционную систему ALT Workstation K 11.1 и должен быть доступен для использования.

Эта инструкция поможет вам установить и настроить шрифт Fira Code Medium Nerd Font Complete в вашей операционной системе. 