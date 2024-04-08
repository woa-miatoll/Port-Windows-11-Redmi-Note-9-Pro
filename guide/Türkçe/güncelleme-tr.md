<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Redmi Note 9 Pro Üzerinde Windows 11 Çalıştırma">


# Redmi Note 9 Pro'da Windows Çalıştırma

## Sürücü Güncelleme

### Gereksinimler

- [UEFI](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/UefiV2)
- [Modded OFOX](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/modded-ofox)
- [Sürücü Güncelleyici](https://github.com/WOA-Project/DriverUpdater/releases/latest)
- [Sürücüler](https://github.com/N1kroks/7xx-Drivers/releases/tag/latest)

#### OFOX Kurtarmayı PC üzerinden şu komutla başlatın

```cmd
fastboot boot <ofox.img>
```

> OFOX zaten yüklüyse, başlangıçta güç ve ses+ düğmelerini basılı tutmanız yeterlidir


#### Komutu Çalıştırın

```cmd
adb shell msc.sh
```

### Disklere harf atama

#### Windows disk yönetimini açın

> Note 9 Pro bir disk olarak algılandığında 

```cmd
diskpart
```


### Windows birimine `X` harfini atama

#### Telefonun Windows birimini seçin
> Bulmak için `list volume` kullanın, "WINMIATOLL" adlı birimdir.

```diskpart
select volume <sayı>
```

#### X harfini atama
```diskpart
assign letter=x
```

#### Diskpart'tan çık
```diskpart
exit
```


### Sürücüleri Kurma

Sürücüler klasöründen OfflineUpdater.bat dosyasını açın ve X: yazın


### Windows önyüklenebilir UEFI İmajı ile önyükleme

```
fastboot flash boot <uefi.img>
```

## Bitti!
