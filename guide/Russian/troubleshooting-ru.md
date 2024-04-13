<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">


# Windows на Redmi Note 9 Pro

## Решение возможных проблем

## Устройство может загрузиться в android, но не в загрузчик

### Требования:

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

Это происходит из-за разделов с именами которые загрузчик не может обработать:

- Загрузитесь в Рекавери

- Подключите телефон к компьютеру

- Откройте cmd на компьютере

- Запустите ```adb shell```

- Запустите ```parted```

- Запустите ```print``` чтобы вывести список всех разделов

- найдите разделы, в названиях которых есть пробелы, например "Basic Data Partition", и запишите номер их тома.

- Теперь запустите ```rm <vol number>``` например ```rm 36```


## Сенсорный экран не работает

- Выключените и включите дисплея
