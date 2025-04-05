## Инструкция по установке шрифта `Fira Code Medium Nerd Font Complete` на операционную систему `ALT Workstation K 10.4`

1. Скачивание шрифта:
   - Скачайте файл шрифта Fira Code Medium Nerd Font Complete.ttf на ваш компьютер.

2. Копирование шрифта в каталог шрифтов:
   - Откройте терминал.
   - Выполните команду для копирования файла шрифта в каталог шрифтов:

```bash
sudo cp "/путь_к_файлу/Fira Code Medium Nerd Font Complete.ttf" /usr/share/fonts/
```

3. Обновление кэша шрифтов:
   - Выполните команду для обновления кэша шрифтов:

```bash
fc-cache -f -v
```

## Настройка шрифта в `консоли` по умолчанию

1. Установка шрифта в консоли:
   - Откройте терминал `konsole`.
   - Выполните команду для установки шрифта `Fira Code Medium Nerd Font Complete` по умолчанию:

```bash
kwriteconfig5 --file konsolerc --group 'General' --key 'font' 'Fira Code Medium Nerd Font Complete,12,-1,5,50,0,0,0,0,0'
```
2. Проверка установленного шрифта:
   - Для проверки установленного шрифта выполните команду:

```bash
kreadconfig5 --file konsolerc --group 'General' --key 'font'
```

P.S После выполнения этих шагов шрифт Fira Code Medium Nerd Font Complete будет установлен на вашей системе ALT Workstation K 10.4 и использоваться по умолчанию в терминале `konsole`. 