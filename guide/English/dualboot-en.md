<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Windows on the Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Dualbooting Android and Windows seamlessly
> [!IMPORTANT]
> You have to be rooted to use this guide.

### Prerequisites
- [```Magisk```](https://github.com/topjohnwu/Magisk/releases/latest)

- [```UEFI```](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/Uefi) (You need Secureboot)

- [```StA installer```](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/dualboot)

- [```M3K WoA Helper app```](https://github.com/woa-vayu-archive/WoA-Helper-M3K/releases/latest)

### Setup - Android
- Download and install the M3K WoA Helper app, then open it and grant it root access.
- Download the **UEFI** image and place it inside the folder named `UEFI` in your internal storage.
- Press the `Mount Windows` button, then download and move StA_Installer_miatoll.exe to the newly created `Windows` folder in your internal storage.
> [!Important]
> If `/sdcard/Windows` is empty, your rom does not support mounting and you will have to make a boot.img backup inside the app, then copy it manually to Windows once you boot to it (for example by uploading it somewhere and then downloading it while booted into Windows). The same applies to the StA files, which are also generated in your internal storage.
>
> Do the same thing if the folder is read-only.
- Return to the M3K WoA Helper and press `QuickBoot to Windows`.

### Setup - Windows
- Navigate to `C:\StA_Installer_miatoll.exe` and run it.

#### Booting to Android
- Run the new shortcut on your desktop or start menu

#### Booting to Windows
- Press `Quickboot to Windows` inside the M3K WoA Helper
  
## Finished!

> [!TIP]
> Don't forget to check out [**```Useful apps and instructions```**](additional-materials-en.md
) page. You'll find a guide on how to activate your Windows, as well as other helpful information.