  <img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">


# Запуск Windows на Redmi Note 9 Pro

## Установка

## Установка Windows

### Требования

- [Arm образ Windows (Windows 11 рекомендуется)](https://uupdump.net/)
- [UEFI](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/UefiV3)
- [Драйвера](https://github.com/N1kroks/7xx-Drivers/releases/latest)
- Мозги (Очень важно)

#### Выполните скрипт msc

```cmd
adb shell msc
```

### Назначение букв дискам

#### Запустите диспетчер дисков Windows
> [!Warning]
> Если вы удалите любой раздел с помощью diskpart сейчас или позже, Windows рано или поздно отправит команду памяти, которая будет неправильно распознана в следствие чего вся память будет стерта.

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

### Назначьте `Y` на том ESP

#### Выберите раздел для ESP
> Используйте  `list volume` чтобы найти его, это будет "ESPMIATOLL"

```diskpart
select volume <number>
```

#### Назначьте букву Y

```diskpart
assign letter=y
```

#### Выйдите из diskpart
```diskpart
exit
```

## Установка

### Установка Windows

> замените путь `<path/to/Install.wim>` на свой путь до install.wim

> Если вы используйте ISO файл, то файл образа находится в ISO. Монтируйте ISO через Windows Explorer, а затем скопируйте путь к нему

```cmd
dism /apply-image /ImageFile:<path/to/install.wim> /index:1 /ApplyDir:X:\
```

### Установка Драйверов

> Распакуйте драйвера из архива и откройте 'OfflineUpdater.cmd' файл. Впишите букву диска WINMIATOLL (Должно быть X) и нажмите enter.


### Создание загрузчика Windows

```cmd
bcdboot X:\Windows /s Y: /f UEFI
```

## Разрешить не подписанные драйверы

>  Если вы не сделаете этого, то получите BSOD

```cmd
bcdedit /store Y:\EFI\Microsoft\BOOT\BCD /set {default} testsigning on
```

## Загрузка в Windows

### Проверьте, какой тип панели у вас

> Open cmd
```cmd
adb shell panel
```

### Переместите файл `<uefi.img>` на устройство

```cmd
adb push <uefi.img> /sdcard
```

#### Если у вас есть карта microSD, воспользуйтесь этим

```cmd
adb push <uefi.img> /external_sd
```


### Создайте резервную копию существующего загрузочного образа
> Вам нужно сделать это всего один раз.

> Поместите его на карту microSD, если это возможно.


### Прошивка образа uefi из OFOX
Перейдите к файлу `uefi.img` и прошейте его в boot

## Загрузка в Android
> Используйте резервный загрузочный образ из OFOX

## [Следующий необязательный шаг: Настройте Dualboot](dualboot-ru.md)
