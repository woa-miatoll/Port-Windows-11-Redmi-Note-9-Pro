<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Запуск Windows на Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Двойная загрузка Android и Windows
> [!IMPORTANT]
> Ваше устройство должно быть рутировано 

### Требования
- [```Magisk```](https://github.com/topjohnwu/Magisk/releases/latest)

- [```UEFI```](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/Uefi) (Вам нужен SecureBoot)

- [```WOA Helper app```](https://github.com/Marius586/WoA-Helper-update/releases/tag/WOA)

### Настройка - Android
- Скачайте и установите приложение WOA Helper, затем откройте его и предоставьте ему root-доступ.
- Загрузите образ **UEFI** для вашей панели и поместите его в папку с именем `UEFI` на внутреннем накопителе.
- Откройте приложение WOA Helper и нажмите STA CREATOR в WOA TOOLBOX
> [!Important]
> Если `/sdcard/Windows` пуста, значит, ваша система не поддерживает монтирование, и вам придется создать резервную копию boot.img внутри приложения, а затем вручную скопировать ее в Windows после загрузки (например, загрузив ее куда-нибудь, а затем скачать при загрузке в Windows). То же самое относится и к Файлам Sta, Которые тоже сгенерировались в вашем внутренем хранилище.
-  нажмите кнопку `Quickboot to Windows`.

### Настройка - Windows
- Перейдите  к `C:\sta` и создайте ярлык приложения sta.exe на ваш рабочий стол, Если он уже не создался там

#### Загрузка в Android
- Запустите новый ярлык на рабочем столе (вы также можете закрепить его в меню «Пуск» или на панели задач для удобства доступа).

#### Загрузка в Windows
- Нажмите `Quickboot to Windows` внутри приложения или воспользуйтесь вновь созданным переключателем на панели быстрых настроек.
  
## Готово!

> [!TIP]
> Не забудьте проверить [**```Полезные приложения и инструкции```**](additional-materials-ru.md
) Там вы найдете руководство по активации Windows, а также другую полезную информацию.