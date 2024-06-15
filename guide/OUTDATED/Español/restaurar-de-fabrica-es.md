<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">


# Windows en el Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Desinstalar

### ¿Por qué lo necesitamos?

Si quieres desinstalar Windows usa esto para evitar el error humano evitar escribir una guia dedicada solo a desinstalar.

Si quieres blooquear tu bootloader de nuevo necesitas la tabla de particiones stock

### Requisitos Previos

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)
- [gpt_both0.bin](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/Binaries)

### Notes

> Reemplaza ```<gpt_both0.bin>``` por el directorio de gpt_both0.bin 


## Restaurar GPT

```cmd
fastboot flash partition:0 <gpt_both0.bin>
```

## Formatea userdata para evitar el bootloop y resturar el peso de FS
```cmd
fastboot -w
```

