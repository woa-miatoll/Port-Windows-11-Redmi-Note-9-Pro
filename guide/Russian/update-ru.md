<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">


# Запуск Windows на Redmi Note 9 Pro

## Обновление драйверов

### Требования

- [UEFI](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/UefiV3)
- [Modded OFOX](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/modded-ofox)
- [Драйвера](https://github.com/N1kroks/7xx-Drivers/releases/latest)

#### Запустите OFOX recovery через компьютер с помощью команды

```cmd
fastboot boot <ofox.img>
```

#### Запустите скрипт msc

```cmd
adb shell msc
```

### Назначение букв дискам

#### Запустите диспетчер дисков Windows

> Когда Note 9 Pro определится как диск

```cmd
diskpart
```

### Назначьте `X` на том Windows

#### Выберите раздел для Windows
> Используйте  `list volume` чтобы найти его, это будет "WINMIATOLL"

```diskpart
select volume <number>
```

#### Назначьте букву X
```diskpart
assign letter=x
```

#### Выйдите из diskpart
```diskpart
exit
```


### Установка драйверов

> Распакуйте драйвера из архива и откройте 'OfflineUpdater.cmd' файл. Впишите букву диска WINMIATOLL (Должно быть X) и нажмите enter.

## Finished!
