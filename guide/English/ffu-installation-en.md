<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Running Windows on the Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Windows Installation 

### Prerequisites
- [```FFU Windows Image```](https://t.me/WoaMiatollFFU)

- [```UEFI```](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/Uefi) (You need Secureboot)

- [```Android platform tools```](https://developer.android.com/studio/releases/platform-tools)

- [```FFU Tools```](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/download/FFUTools/FFU-Loader-Tools.zip)

### Notes:
> [!Warning]
> All your data will be erased! Back up now if needed.
>
> DO NOT REBOOT YOUR PHONE if you think you made a mistake, ask for help in the [Telegram chat](https://t.me/woamiatoll)
>
> Do not run all commands at once, execute them in order!
>
> **PLEASE DON'T USE OUTDATED VIDEO GUIDES ON YOUTUBE OR ANY OTHER PLATFORM! THESE VIDEOS ARE OUTDATED AND YOU CAN BRICK YOUR DEVICE USING THEM!**

### Opening CMD as an admin
> Download **platform-tools** and extract the folder somewhere, then open CMD as an **administrator**.
> 
> Replace `path\to\platform-tools` with the actual path to the platform-tools folder, for example **C:\platform-tools**.
```cmd
cd path\to\platform-tools
```

### Boot UEFI
> Boot into fastboot mode, then run the following command, replacing `path\to\xiaomi-miatoll_SecureBoot.img` with the actual path of UEFI
```cmd
fastboot boot path\to\xiaomi-miatoll_SecureBoot.img
```
> Press volume down button until you see the qr code and the wrench icon

### Opening CMD as an admin
> Download **FFU Tools** and extract the folder somewhere, then open CMD as an **administrator**.
> 
> Replace `path\to\FFU-Loader-Tools` with the actual path to the FFU-Loader-Tools folder, for example **C:\FFU-Loader-Tools**.
```cmd
cd path\to\FFU-Loader-Tools
```

### Flash FFU
> Replace `path\to\miatoll.ffu` with the actual path to FFU file, for example **C:\miatoll_128GB_HalfSplit.ffu**
```cmd
ImageUtility.exe FlashDevice -Path path\to\miatoll.ffu
```
> Wait until FFU is flashed and green check mark appears

### Reboot to Android
```cmd
ImageUtility.exe RebootDevice
```
> Set up your device, then go to the next step

## [Next step: Setting up dualboot](dualboot-en.md)