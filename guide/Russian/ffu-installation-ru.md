<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Запуск Windows на Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Установка Windows

### Требования
- [```FFU Образ Windows```](https://t.me/WoaMiatollFFU)

- [```UEFI```](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/Uefi) (Вам нужен SecureBoot)

- [```Android platform tools```](https://developer.android.com/studio/releases/platform-tools)

- [```FFU Tools```](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/download/FFUTools/FFU-Loader-Tools.zip)

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
> Замените `путь\до\platform-tools` на фактический путь к папке platform-tools, например **C:\platform-tools**.
```cmd
cd путь\до\platform-tools
```

### Запустите UEFI
> Загрузитесь в режим fastboot, затем выполните следующую команду, Заменив `путь\до\xiaomi-miatoll_SecureBoot.img` на фактический путь к образу UEFI
```cmd
fastboot boot путь\до\xiaomi-miatoll_SecureBoot.img
```
> Зажмите кнопку уменьшения громкости, пока не увидите qr код и значок с гаечным ключом

### Откройте CMD от имени администратора
> Скачайте **FFU Tools** и распакуйте папку куда-нибудь, затем откройте CMD от имени **администратора**.
> 
> Замените `путь\до\FFU-Loader-Tools` на фактический путь к папке FFU-Loader-Tools, например **C:\FFU-Loader-Tools**.
```cmd
cd путь\до\FFU-Loader-Tools
```

### Прошивка FFU
> Замените `путь\до\miatoll.ffu` на фактический путь к файлу FFU, например
**C:\miatoll_128GB_HalfSplit.ffu**
```cmd
ImageUtility.exe FlashDevice -Path путь\до\miatoll.ffu
```
> Подождите пока FFU прошьется и появится зеленая галка

### Перезагрузка в Android
```cmd
ImageUtility.exe RebootDevice
```
> Настройте свое устройство и двигайтесь к следующему шагу

## [Следующий шаг: Настройка Dualboot](dualboot-ru.md)
