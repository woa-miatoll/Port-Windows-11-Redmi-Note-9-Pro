<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">

# Запуск Windows на Redmi Note 9 Pro

## Двойная загрузка Android и Windows
> [!IMPORTANT]
> Ваше устройство должно быть рутировано 

### Требования
- [Magisk](https://github.com/topjohnwu/Magisk/releases/latest)

- [UEFI](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/Uefi)

- [WOA Helper app](https://github.com/Marius586/WoA-Helper-update/releases/tag/WOA)

- [StA Установщик](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/download/dualboot/StA_Installer_miatoll.exe)

### Настройка - Android
- Скачайте и установите приложение WOA Helper, затем откройте его и предоставьте ему root-доступ.
- Загрузите образ **UEFI** для вашей панели и поместите его в папку с именем `UEFI` на внутреннем накопителе.
- Нажмите кнопку `Mount Windows`, чтобы смонтировать Windows на внутреннее хранилище по адресу `/sdcard/Windows`.
> [!Important]
> Если `/sdcard/Windows` пуста, значит, ваша система не поддерживает монтирование, и вам придется создать резервную копию boot.img внутри приложения, а затем вручную скопировать ее в Windows после загрузки (например, загрузив ее куда-нибудь, а затем скачать при загрузке в Windows). То же самое относится и к программе установки STA.
>
> Сделайте то же самое, если папка доступна только для чтения.
- Скачайте и переместите **StA_Installer_miatoll.exe** в `/sdcard/Windows`.
- Вернитесь в приложение WOA Helper и нажмите кнопку `Quickboot`.

### Настройка - Windows
- Перейдите  к `C:\StA_Installer_miatoll.exe` и запустите его. Если это не сработает, убедитесь, что все антивирусные программы отключены, поскольку они, вероятно, не позволят приложению запуститься.

#### Загрузка в Android
- Запустите новый ярлык на рабочем столе (вы также можете закрепить его в меню «Пуск» или на панели задач для удобства доступа).

#### Загрузка в Windows
- Нажмите `Quickboot to Windows` внутри приложения или воспользуйтесь вновь созданным переключателем на панели быстрых настроек.
  
## Готово!