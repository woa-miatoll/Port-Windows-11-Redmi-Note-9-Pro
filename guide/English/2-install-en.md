  <img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">


# Running Windows on the Redmi Note 9 Pro

## Installation

## Installing Windows
> You will need to have MTP disabled in Mount

### Prerequisites

- [Windows on ARM image (Windows 11 is recommended)](https://uup.ee/)
- [UEFI image](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/UefiV2)
- [DriverUpdater](https://github.com/WOA-Project/DriverUpdater/releases/latest)
- [Drivers](https://github.com/Icesito68/7xx-Drivers/releases/tag/Miatoll-Drivers-V1.0.5)

#### Execute the msc script

```cmd
adb shell msc.sh
```

### Assign letters to disks
  

#### Start the Windows disk manager

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

> Replace `<miatollriversfolder>` with the location of the drivers folder

```cmd
driverupdater.exe -d <miatolldriversfolder>\definitions\Desktop\ARM64\Internal\miatoll.txt -r <miatolldriversfolder> -p X:
```

  

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
