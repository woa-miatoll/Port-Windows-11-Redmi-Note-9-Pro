<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">


# Windows en el Redmi Note 9 Pro

## Actualizar Drivers

### Requisitos Previos

- [UEFI](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/Uefi)
- [OFOX Modificado](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/modded-ofox)
- [Drivers](https://github.com/N1kroks/7xx-Drivers/releases/latest)

#### Iniciar TWRP desde el pc con el comando

```cmd
fastboot boot <ofox.img>
```

> Si ya tienes el OFOX modificado instalado, solo presiona el botón de encendido y vol+ para iniciarlo


#### Ejecutar el script

```cmd
adb shell msc.sh
```

### Asignar Letras A Los Discos

#### Iniciar El Administrador De Discos De Windows

> Cuando el Note 9 Pro sea detectado como disco

```cmd
diskpart
```


### Asignar la letra `X` a la partición de Windows

#### Seleccione el volumen de Windows del teléfono
> Usa `list vol` para encontrarlo, es el que se llama "WINMIATOLL"

```diskpart
sel vol <number>
```

#### Asignar la letra X
```diskpart
assign letter=x
```

#### Salir de diskpart
```diskpart
exit
```


### Instalar Los Drivers

> Reemplaza `<miatolldriversfolder>` por la localización de la carpeta de los drivers

> Abre un cmd como administrador


```cmd
DriverUpdater.exe -d <miatolldriversfolder>\definitions\Desktop\ARM64\Internal\miatoll.txt -r <miatolldriversfolder> -p X:
```


### Arranca Windows con la UEFI

```
fastboot flash boot <uefi.img>
```

## ¡Terminado!
