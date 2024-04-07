<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">


# Running Windows on the Redmi Note 9 Pro

## Driver updating

### Prerequisites

- [UEFI](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/UefiV2)
- [Modded OFOX](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/modded-ofox)
- [DriverUpdater](https://github.com/WOA-Project/DriverUpdater/releases/latest)
- [Drivers](https://github.com/N1kroks/7xx-Drivers/releases/tag/latest)

#### Start TWRP recovery through the PC with the command

```cmd
fastboot boot <twrp.img>
```

> If you already have TWRP installed, just hold the power and vol+ buttons at startup


#### Execute script

```cmd
adb shell msc
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

#### Exit diskpart
```diskpart
exit
```


### Install Drivers

Open OfflineUpdater.bat file from the drivers folder and type X:


### Boot with Windows bootable UEFI image

```
fastboot flash boot <uefi.img>
```

## Finished!
