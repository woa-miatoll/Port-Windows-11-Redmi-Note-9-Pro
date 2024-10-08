<img align="right" src="https://github.com/woa-miatoll/Port-Windows-11-Redmi-Note-9-Pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Запуск Windows на Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Двойная загрузка Android и Windows
> [!IMPORTANT]
> Ваше устройство должно быть рутировано 

### Требования
- [```Magisk```](https://github.com/topjohnwu/Magisk/releases/latest)

- [```UEFI```](https://github.com/woa-miatoll/Miatoll-Releases/releases/latest) (Вам не нужен secureboot disabled)

- [```StA installer```](https://github.com/woa-miatoll/Port-Windows-11-Redmi-Note-9-Pro/releases/tag/dualboot)

- [```M3K Helper app```](https://github.com/woa-vayu-archive/WoA-Helper-M3K/releases/latest)

### Настройка - Android
- Скачайте и установите приложение M3K Helper, затем откройте его и предоставьте ему root-доступ.
- Загрузите образ **UEFI** и поместите его в папку с именем `UEFI` в внутреннем накопителе.
- Нажмите кнопку `Mount Windows`, затем скачайте и переместите файл StA_Installer_miatoll.exe в только что созданную папку `Windows` в внутреннем накопителе.
> [!Important]
> Если `/sdcard/Windows` пуста, значит, ваша система не поддерживает монтирование, и вам придется создать резервную копию boot.img внутри приложения, а затем вручную скопировать ее в Windows после загрузки (например, загрузив ее куда-нибудь, а затем скачать при загрузке в Windows). То же самое относится и к Файлам StA, Которые тоже сгенерировались в вашем внутренем хранилище.
- Вернитесь в M3K Helper и нажмите `QuickBoot to Windows`.

### Настройка - Windows
- Перейдите  к `C:\StA_Installer_miatoll.exe` и запустите его от имени администратора.

#### Загрузка в Android
- Запустите новый ярлык на рабочем столе или в меню Пуск.

#### Загрузка в Windows
- Нажмите `Quickboot to Windows` в M3K Helper
  
## Готово!

> [!TIP]
> Не забудьте проверить [**```Полезные приложения и инструкции```**](additional-materials.md
) Там вы найдете руководство по активации Windows, а также другую полезную информацию.