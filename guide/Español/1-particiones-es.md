  <img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">


# Windows en el Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

Estos pasos son necesarios para crear las particiones donde pondremos Windows

### Requisitos Previos

- [OFOX Modificado](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/modded-ofox)

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)


## Notas:
> **Advertencia** si eliminas alguna partición via diskpart más adelante o ahora, Windows enviará un comando ufs que se malinterpretará y borrará toda la ufs
- Estos comandos han sido testeados.
- No ejecutes el mismo comando dos veces
- NO REINICIES TU DISPOSITIVO si crees que cometiste un error, preguntanos en el [Chat de Telegram](https://t.me/woamiatoll)

#### ⚠️ ¡No ejecutes todos los comandos a la vez, ejecútalos en orden!

##### ⚠️ ¡¡¡NO COMETAS NINGÚN ERROR!!! ¡¡¡PUEDES ROMPER TU DISPOSITIVO CON LOS COMANDOS A CONTINUACIÓN SI LOS HACES MAL!!!

#### Arranca en TWRP desde el PC con este comando
```cmd
fastboot boot <ofox.img>
```
> si tienes el OFOX modificado instalado, solo presiona el botón de encendido y vol+ para iniciarlo

### Iniciar parted
```sh
Adb shell parted /dev/block/sda
```

### Borrar la partición `userdata` 
>Para asegurarte de que la partición 18 es userdata puedes usar
>  `print all`
```sh
rm 18
```

### Crear particiones
> Si recibes cualquier advertencia que te diga ignorar o cancelar, solo escribe i y dale a enter enter

<details>
<summary><b><strong>Para modelos de 64Gb</strong></b></summary>
  
  - Crea la partición ESP (Aqui estará el bootloader de Windows y los archivos EFI)
```sh
mkpart esp fat32 11GB 11.4GB
```
  
- Creamos la partición principal donde instalaremos Windows
```sh
mkpart win ntfs 11.4GB 42.4GB
```  
  
  
- Creamos la partición de datos de Android
```sh
mkpart userdata ext4 42.4GB 59.4GB
```


  </summary>
</details>  
  
  
<details>
<summary><b><strong>Para modelos de 128Gb</strong></b></summary>
  

  - Crea la partición ESP (Aqui estará el bootloader de Windows y los archivos EFI)
```sh
mkpart esp fat32 11GB 11.4GB
```
  
- Creamos la partición principal donde instalaremos Windows
```sh
mkpart win ntfs 11.4GB 65.4GB
```  
  
  
- Creamos la partición de datos de Android
```sh
mkpart userdata ext4 65.4GB 123GB
```
  
  </summary>
</details> 

### Hace a ESP la partición de arranque para que la imagen EFI pueda detectarla
```sh
set 18 esp on
```

### Reiniciar a OFOX

### Iniciar shell otra vez en tu PC
```cmd
adb shell
```

### Formatear las particiones
-  Formatea la partición ESP en FAT32
```sh
mkfs.fat -F32 -s1 /dev/block/by-name/esp -n ESPMIATOLL
```

-  Formatea la partición de Windows en NTFS
```sh
mkfs.ntfs -f /dev/block/by-name/win -L WINMIATOLL
```

- Formatea data
Ve a Wipe en OFOX y presiona Format Data, 
después escribe `yes`.

### Comprueba si android inicia
Solo reinicia el teléfono y comprueba si Android inicia


## [Siguiente paso: Instalar Windows](2-instalacion-es.md)
