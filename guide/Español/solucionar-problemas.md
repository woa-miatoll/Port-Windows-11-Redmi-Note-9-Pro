<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">


# Windows en el Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Solucionar problemas


## El dispositivo puede arrancar el bootloader pero no en android

### Requisitos previos:

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

Esto es causado por particiones con nombres de volumen que el bootloader no puede manejar, para arreglar esto:

- Arranca el recovery

- Conecta el teléfono al PC

- Abre el cmd en el PC

- Pon ```adb shell```

- Pon ```parted```

- Pon ```print``` to list all partitions

- Busca particiones que tengan espacios en los nombres, por ejemplo, "Partición de datos básicos" y anota su número de volumen

- Ahora pon ```rm <vol number>``` por ejemplo ```rm 36```


## La pantalla táctil no funciona

- Apaga y enciende la pantalla o tu panel es Huaxing y todavia no se soporta.

