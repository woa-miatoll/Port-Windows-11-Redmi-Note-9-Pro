<img align="right" src="https://github.com/woa-miatoll/Port-Windows-11-Redmi-Note-9-Pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Запуск Windows на Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Установка

### Требования
- [```Образ рекавери```](https://github.com/woa-miatoll/Port-Windows-11-Redmi-Note-9-Pro/releases/tag/Recoveries)

- [```Android platform tools```](https://developer.android.com/studio/releases/platform-tools)

- ```Мозги (Очень важно)```

### Примечание:
> [!Warning]
> Все пользовательские файлы будут стерты! Создайте резервную копию, если это необходимо.
>
> НЕ ПЕРЕЗАГРУЖАЙТЕ ТЕЛЕФОН! Если вы считаете, что совершили ошибку, обратитесь за помощью в [чат в телеграмме](https://t.me/woamiatoll)
>
> Не запускайте все команды сразу, выполняйте их по очереди!
>
> **ПОЖАЛУЙСТА, НЕ ИСПОЛЬЗУЙТЕ УСТАРЕВШИЕ ВИДЕОГАЙДЫ НА YOUTUBE ИЛИ ЛЮБОЙ ДРУГОЙ ПЛАТФОРМЕ! ЭТИ ВИДЕО УСТАРЕЛИ, И ВЫ МОЖЕТЕ СЛОМАТЬ СВОЕ УСТРОЙСТВО, ИСПОЛЬЗУЯ ИХ!**

### Откройте CMD от имени администратора
> Скачайте **platform-tools** и распакуйте папку куда-нибудь, затем откройте CMD от имени **администратора**.
>
> Рекомендуется держать CMD открытым и использовать его на протяжении всего руководства.
> 
> Замените `путь\до\platform-tools` на фактический путь к папке platform-tools, например **C:\platform-tools**.
```cmd
cd путь\до\platform-tools
```

##### Прошейте ofox с компьютера при помощи команды
> Загрузитесь в режим fastboot, затем выполните следующую команду, заменив `путь\до\ofox.img` на фактический путь к образу ofox
```cmd
fastboot flash recovery путь\до\ofox.img reboot recovery
```

#### Запустите скрипт разметки
> Замените **$** на объем памяти, который вы хотите предоставить Windows (не добавляйте ГБ, просто напишите число).
> 
> Если скрипт попросит запустить его ещё раз, то так и сделайте
```sh
adb shell partition $
```

#### Проверьте, запускается ли Android
```cmd
adb reboot
```
> Настройте свое устройство и двигайтесь к следующему шагу

## [Следующий шаг: установка Windows](2-install.md)
