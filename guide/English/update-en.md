<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">


# Running Windows on the Redmi Note 9 Pro

## Driver updating

### Prerequisites

- [UEFI](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/UefiV2)
- [Modded OFOX](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/modded-ofox)
- [DriverUpdater](https://github.com/WOA-Project/DriverUpdater/releases/latest)
- [Drivers](https://github.com/Icesito68/7xx-Drivers/releases/tag/Miatoll-Drivers-V1.0.5)

#### Start TWRP recovery through the PC with the command

```cmd
fastboot boot <twrp.img>
```

> If you already have TWRP installed, just hold the power and vol+ buttons at startup


#### Execute script

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

#### Exit diskpart
```diskpart
exit
```


### Install Drivers

> Replace `<miatolldriversfolder>` with the location of the drivers folder

> Open cmd as administrator


```cmd
DriverUpdater.exe -d <miatolldriversfolder>\definitions\Desktop\ARM64\Internal\miatoll.txt -r <miatolldriversfolder> -p X:
```


### Boot with Windows bootable UEFI image

```
fastboot flash boot <uefi.img>
```

## Finished!
