<img align="right" src="https://github.com/woa-miatoll/Port-Windows-11-Redmi-Note-9-Pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Запуск Windows на Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Установка Windows

### Требования
- [```ARM Windows ESD```](https://arkt-7.github.io/woawin/)

- [```Драйвера```](https://github.com/woa-miatoll/Miatoll-Releases/releases/latest)

### Перезагрузитесь в рекавери
> Перезагрузите телефон в рекавери

#### Выполните скрипт msc
```cmd
adb shell msc
```

### Diskpart
> [!Warning]
> НЕ СТИРАЙТЕ, НЕ СОЗДАВАЙТЕ И НЕ ИЗМЕНЯЙТЕ РАЗДЕЛЫ В DISKPART!!!!. ЭТО МОЖЕТ СТЕРЕТЬ UFS ВАШЕГО ТЕЛЕФОНА ИЛИ ПОМЕШАТЬ ЗАГРУЗКЕ В FASTBOOT!!!!. ЭТО ОЗНАЧАЕТ, ЧТО ВАШЕ УСТРОЙСТВО БУДЕТ НАВСЕГДА ОКИРПИЧЕНО И НЕ БУДЕТ ИМЕТЬ НИКАКОГО РЕШЕНИЯ! (кроме как отнести устройство в Xiaomi или прошить его с помощью EDL, но оба варианта, скорее всего, будут стоить денег)
```cmd
diskpart
```

#### Выберите раздел для Windows
> Используйте `list volume`, чтобы найти его, замените **$** на номер тома  **WINMIATOLL**.
```diskpart
select volume $
```

#### Назначьте букву X
```diskpart
assign letter x
```

#### Выйдите из diskpart
```diskpart
exit
```

#### Форматирование Windows
> Перейдите в Проводник Windows > Этот компьютер и выберите **WINMIATOLL**. Щелкните правой кнопкой мыши и отформатируйте диск как NTFS

### Установка Windows
> замените путь `путь\до\install.esd` на свой путь до install.esd (Может быть назван install.wim)
```cmd
dism /apply-image /ImageFile:путь\до\install.esd /index:6 /ApplyDir:X:\
```

> Если вы получили `Error 87`, проверьте индекс образа с помощью команды `dism /get-imageinfo /ImageFile:путь\до\install.esd`, затем замените `index:6` на фактический номер индекса Windows 11 Pro в вашем образе

### Установка Драйверов
> Распакуйте драйвера из архива и откройте 'OfflineUpdater.cmd' 

> Если он попросит вас ввести букву, введите букву диска **WINMIATOLL** (это должно быть X), затем нажмите enter.

> Если в разделе **Installing App Packages** появятся какие-либо ошибки, не обращайте на них внимания и продолжайте

### Загрузка в Windows
Перезагрузите телефон. Если вы попали в Android вместо Windows, прошейте UEFI еще раз с помощью WOA Helper

#### Настройка Windows
>  Теперь на вашем устройстве будет установлена Windows. Это займет некоторое время. В конце концов устройство перезагрузится, после чего запустится начальная установка (oobe)

> [!Note]
> Чтобы не входить в учетную запись Microsoft, используйте "g" для ввода электронной почты и пароля. После этого Windows позволит вам создать локальную учетную запись

## Готово!
