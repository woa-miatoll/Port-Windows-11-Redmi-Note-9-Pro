<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">

# Запуск Windows на Redmi Note 9 Pro

## Установка Windows

### Требования
- [Arm образ Windows](https://worproject.com/esd)

- [Драйвера](https://github.com/N1kroks/7xx-Drivers/releases/latest)

- [Мод рекавери](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/modded-ofox)

- Мозги (Очень важно)

### Запустите ofox с компьютера при помощи команды
```cmd
fastboot boot <ofox.img>
```

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
> замените путь `<path\to\install.esd>` на свой путь до install.esd (Может быть назван install.wim)
```cmd
dism /apply-image /ImageFile:<path\to\install.esd> /index:6 /ApplyDir:X:\
```

> Если вы получили `Error 87`, проверьте индекс образа с помощью команды `dism /get-imageinfo /ImageFile:<path\to\install.esd>`, затем замените `index:6` на фактический номер индекса Windows 11 Pro в вашем образе

### Установка Драйверов
> Распакуйте драйвера из архива и откройте 'OfflineUpdater.cmd' 

> Если он попросит вас ввести букву, введите букву диска **WINMIATOLL** (это должно быть X), затем нажмите enter.

> Если в разделе **Installing App Packages** появятся какие-либо ошибки, не обращайте на них внимания и продолжайте

### Создание загрузчика Windows
```cmd
bcdboot X:\Windows /s Y: /f UEFI
```

## Разрешить не подписанные драйверы
```cmd
bcdedit /store Y:\EFI\Microsoft\BOOT\BCD /set "{default}" testsigning on
```

#### Отключение восстановления
```cmd
bcdedit /store Y:\EFI\Microsoft\BOOT\BCD /set "{default}" recoveryenabled no
```

#### Отключение проверок целостности
```cmd
bcdedit /store Y:\EFI\Microsoft\BOOT\BCD /set "{default}" nointegritychecks on
```

### Перезагрузка в Android
> Для установки дуал бута

## [Последний шаг: Настройка Dualboot](dualboot-ru.md)
