<img align="right" src="https://github.com/woa-miatoll/Port-Windows-11-Redmi-Note-9-Pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Запуск Windows на Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Установка Windows

### Требования
- [```ARM Windows ESD```](https://worproject.com/esd) (Выберите - Version:  ```11``` Build:  ```22631.2861``` Architecture:  ```ARM64``` Edition:  ```CLIENT``` Language:  ```Выберите ваш язык```)

- [```Драйвера```](https://github.com/woa-miatoll/Miatoll-Releases/releases/latest)

- ```Мозги (Очень важно)```

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

#### Выберите раздел для ESP
> Используйте `list volume`, чтобы найти его, замените **$** на номер тома  **ESPMIATOLL**.
```diskpart
select volume $
```

#### Назначьте букву Y
```diskpart
assign letter y
```

#### Выйдите из diskpart
```diskpart
exit
```

### Установка Windows
> [!Warning]
> НЕ ИСПОЛЬЗУЙТЕ 24H2!!!

> замените путь `путь\до\install.esd` на свой путь до install.esd (Может быть назван install.wim)
```cmd
dism /apply-image /ImageFile:путь\до\install.esd /index:6 /ApplyDir:X:\
```

> Если вы получили `Error 87`, проверьте индекс образа с помощью команды `dism /get-imageinfo /ImageFile:путь\до\install.esd`, затем замените `index:6` на фактический номер индекса Windows 11 Pro в вашем образе

### Установка Драйверов
> Распакуйте драйвера из архива и откройте 'OfflineUpdater.cmd' 

> Если он попросит вас ввести букву, введите букву диска **WINMIATOLL** (это должно быть X), затем нажмите enter.

### Создание загрузчика Windows
```cmd
bcdboot X:\Windows /s Y: /f UEFI
```

### Перезагрузка в Android
```cmd
adb reboot
```

## [Последний шаг: Настройка Dualboot](dualboot-ru.md)
