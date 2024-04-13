<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">


# Запуск Windows на Redmi Note 9 Pro

## Двойная загрузка Android и Windows
> [!IMPORTANT]
> Ваше устройство должно быть рутировано 

### Требования
- [Magisk](https://github.com/topjohnwu/Magisk/releases/latest)
- [UEFI](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/UefiV3)
- [WOA Helper app](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/download/dualboot/woahelper.apk)
- [StA Установщик](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/download/dualboot/StA_Installer_miatoll.exe)

## Настройка приложений для двойной загрузки

### Настройка - Android
> [!NOTE]
> Чтобы смонтировать Windows во время загрузки Android, вам необходимо правильно «выключить» Windows. Для этого перезагрузите Windows, а затем загрузитесь в TWRP, когда экран станет черным. Отсюда вы можете вернуться на Android, используя резервную копию, сделанную ранее.

- Скачайте и установите [WOA Helper app](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/download/dualboot/woahelper.apk)
- Скачайте [UEFI image](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/UefiV3) и перенесите в папку с названием UEFI которая находится в внутреннем хранилище, если папки нету создайте её.
- Вернитесь в WOA Helper и нажмите `Back up Android boot`. Выберите Windows и Android.
- Нажмите `Mount Windows`, после чего скачайте [StA_Installer_miatoll.exe](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/download/dualboot/StA_Installer_miatoll.exe) и перенесите в новую папку `Windows` в вашем внутреннем хранилище.
- Вернитесь в WOA Helper и нажмите `Quickboot to Windows`.

### Настройка - Windows
- Перейдите  к `C:\StA_Installer_miatoll.exe` и запустите его. Если это не сработает, убедитесь, что все антивирусные программы отключены, поскольку они, вероятно, не позволят приложению запуститься.

##### Загрузка в Android
  - Запустите новый ярлык на рабочем столе (вы также можете закрепить его в меню «Пуск» или на панели задач для удобства доступа).

##### Загрузка в Windows
  - Нажмите `Quickboot to Windows` внутри приложения или воспользуйтесь вновь созданным переключателем на панели быстрых настроек.
  
## Готово!