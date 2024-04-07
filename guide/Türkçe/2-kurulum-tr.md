  <img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Redmi Note 9 Pro Üzerinde Windows 11 Çalıştırma">


# Redmi Note 9 Pro'da Windows Çalıştırma

## Kurulum

## Windows'u Yükleme
> Mount'ta MTP'yi devre dışı bırakmanız gerekecek

### Ön Koşullar

- [ARM üzerinde Windows ISO'su (Windows 11 önerilir)](https://uup.ee/)
- [UEFI İmajı](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/UefiV3)
- [Sürücü Güncelleyici](https://github.com/WOA-Project/DriverUpdater/releases/latest)
- [Sürücüler](https://github.com/N1kroks/7xx-Drivers/releases/tag/Miatoll-Drivers-V1.0.9)

#### Msc Komut Dosyasını Çalıştırın

```cmd
adb shell msc.sh
```

### Disklere Harf Atama
  

#### Windows disk yöneticisini başlatın
> [!Warning]
> if you delete any partitions via diskpart later on or now windows will send a ufs command that gets misinterpreted which erase all your ufs

> Once the Note 9 Pro is detected as a disk

```cmd
diskpart
```


### Assign `X` to Windows volume

#### Select the Windows volume of the phone
> Use `list volume` to find it, it's the one named "WINMIATOLL"

```diskpart
select volume <number>
```

#### Assign the letter X
```diskpart
assign letter=x
```

### Assign `Y` to esp volume

#### Select the ESP volume of the phone
> Use `list volume` to find it, it's the one named "ESPMIATOLL"

```diskpart
select volume <number>
```

#### Assign the letter Y

```diskpart
assign letter=y
```

#### Exit diskpart
```diskpart
exit
```

## Install

> replace `<path/to/Install.wim>` with the path of the install.wim file

> `install.wim` is in the ISO sources folder
> you can get it after mounting or extracting the ISO

```cmd
dism /apply-image /ImageFile:<path/to/install.wim> /index:1 /ApplyDir:X:\
```

### Install Drivers

Open OfflineUpdater.bat file from the drivers folder and type X:

### Create Windows bootloader files for the EFI

```cmd
bcdboot X:\Windows /s Y: /f UEFI
```

## Allow unsigned drivers

> If you don't do this you'll get a BSOD

```cmd
bcdedit /store Y:\EFI\Microsoft\BOOT\BCD /set {default} testsigning on
```

## Boot into Windows

### Move the `<uefi.img>` file to the device

```cmd
adb push <uefi.img> /sdcard
```

#### if you have a microSD card use this

```cmd
adb push <uefi.img> /external_sd
```


### Make a backup of your existing boot image
> You need to do it just once

> Put it to the microSD card if possible


### Flash the uefi image from TWRP
Navigate to the `uefi.img` file and flash it into boot

## Boot back into Android
> Use your backup boot image from TWRP

## Finished!
