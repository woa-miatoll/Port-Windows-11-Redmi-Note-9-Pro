<img align="right" src="https://github.com/woa-miatoll/Port-Windows-11-Redmi-Note-9-Pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Windows на Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Решение возможных проблем
> Ниже приведен список распространенных проблем и их решений

## Неполучается смонтировать Windows в Android
Если при монтировании Windows получается пустая папка, то у вас либо не установлена Windows, либо ваша прошивка не поддерживает монтирование

##### Готово!

## Невозможно записать данные в Windows в Android
> Это происходит из-за выключения Windows вместо ее перезапуска.
- Чтобы решить эту проблему, загрузитесь в Windows и нажмите "перезагрузить", затем, когда экран погаснет, загрузитесь в TWRP и оттуда загрузите Android.
- Или отключите спящий режим в Windows, используя [этот скрипт](https://github.com/n00b69/woa-beryllium/releases/tag/1.0) 
> Кроме того, если вы уже установили приложение Switch to Android, просто используйте его для перехода на Android.

##### Готово!

## DISM Error:87 The add-driver option is unkown
Обычно это означает, что у вас нечистый образ Windows с другими драйверами. Вам нужно получить чистый образ Windows (что означает, что вы не следовали инструкциям).

##### Готово!

## 0xc000021a BSOD
Обычно это означает, что winlogon.exe не сработал, и вам может потребоваться заново установить образ Windows

## Устройство может загрузиться в android, но не в загрузчик
Это происходит из-за разделов с именами которые загрузчик не может обработать:

- Загрузитесь в Рекавери

- Подключите телефон к компьютеру

- Откройте cmd на компьютере

- Запустите ```adb shell```

- Запустите ```parted```

- Запустите ```print``` чтобы вывести список всех разделов

- найдите разделы, в названиях которых есть пробелы, например "Basic Data Partition", и запишите номер их тома.

- Теперь запустите ```rm <vol number>``` например ```rm 36```

##### Готово!

## Сенсорный экран не работает
- Выключените и включите дисплея

##### Готово!