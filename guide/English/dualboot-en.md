<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Windows on the Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Dualbooting Android and Windows seamlessly
> [!IMPORTANT]
> You have to be rooted to use this guide.

### Prerequisites
- [```Magisk```](https://github.com/topjohnwu/Magisk/releases/latest)

- [```UEFI```](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/Uefi)

- [```WOA Helper app```](https://github.com/Marius586/WoA-Helper-update/releases/tag/WOA)

### Setup - Android
- Download and install the WOA Helper app, then open it and grant it root access.
- Download the **UEFI** image for your panel and place it inside the folder named `UEFI` in your internal storage.
- Open the WOA Helper app and use the STA CREATOR in WOA TOOLBOX.
> [!Important]
> If `/sdcard/Windows` is empty, your rom does not support mounting and you will have to make a boot.img backup inside the app, then copy it manually to Windows once you boot to it (for example by uploading it somewhere and then downloading it while booted into Windows). The same applies to the StA files, which are also generated in your internal storage.
>
> Do the same thing if the folder is read-only.
- Press the QUICKBOOT TO WINDOWS button.

### Setup - Windows
- Navigate to `C:\sta` and create a shortcut of sta.exe to your desktop, if one isn't already present

#### Booting to Android
- Run the new shortcut on your desktop (you can also pin it to your start menu / taskbar for ease of access)

#### Booting to Windows
- Press `Quickboot to Windows` inside the app, or use the newly created toggle in your quick settings panel
  
## Finished!

> [!TIP]
> Don't forget to check out [**```Useful apps and instructions```**](additional-materials-en.md
) page. You'll find a guide on how to activate your Windows, as well as other helpful information.