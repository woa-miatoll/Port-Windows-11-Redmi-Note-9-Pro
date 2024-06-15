<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Запуск Windows на Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Дополнительные материалы
> Ниже вы найдете список твиков и материалов для Windows для вашего ARM-устройства

## Список поддерживаемых приложений/игр
Этот список ни в коем случае не является полным, в нем просто перечислены приложения/игры, которые были протестированы сообществом
[Ссылку можно найти здесь](https://docs.google.com/spreadsheets/d/1XYuoySgYQE0HL573sA-0RGMX7I4lt5rWJuQ8Z8yRJNY/edit?usp=drivesdk)

Вы также можете найти список нативных программ для ARM [по этой ссылке](https://armrepo.ver.lt/)

##### Готово!

## Спрячьте диск D (раздел модема)
> [!NOTE]
> Это рекомендуется, поскольку этот диск не должен быть изменен, а некоторые приложения могут попытаться записать на него данные.

- Откройте окно командной строки и запустите ```diskpart```
- Запустите ```list volume``` чтобы увидеть все доступные тома
- Выберите диск с буквой D ```select volume $```, заменяя "$" на номер тома
- Удалите букву с помощью ```remove letter d```
- Выйдите из diskpart с помощью ```exit```

##### Готово!

## Переключение режима USB-хоста
> [!Warning]
> Отключите режим USB-хоста, если вы используете USB хаб с питанием, так как это может необратимо повредить устройство. Если вы не используете концентратор USB с питанием, включите режим хоста USB, иначе вы не сможете использовать устройства USB

Запустите [USB Host Control](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/usbhost) чтобы включить/выключить режим хоста USB, и подтвердите, что вы хотите отключить/включить режим хоста USB

##### Готово!

## Отключение secureboot
> [!Warning]
> Делайте это только в случае необходимости!

> [Руководство по отключению secureboot](disable-secureboot-ru.md)

## Установите Microsoft Office / Microsoft 365
- Скачайте этот [файл](https://drive.google.com/file/d/10FTyC0XBccj0BkxdIa_W_haixQz-d3to/view?usp=drivesdk) на телефон
- Нажмите пкм на файле iso и выберите "Смонтировать", чтобы открыть его в проводнике
- Дважды нажмите на ```Office Tool Plus.exe``` чтобы запустить мастер установки
- В появившемся окне нажмите `Да`
- Дождитесь завершения установки

##### Готово!

## Активировать Windows / Office
Следуйте инструкциям Massgravel [здесь](https://github.com/massgravel/Microsoft-Activation-Scripts)

##### Готово!