<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">

# Windows on the Redmi Note 9 Pro

## Dualbooting Android and Windows seamlessly
> [!IMPORTANT]
> You have to be rooted to use this guide.

### Prerequisites
- [Magisk](https://github.com/topjohnwu/Magisk/releases/latest)

- [UEFI](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/Uefi)

- [WOA Helper app](https://github.com/Marius586/WoA-Helper-update/releases/tag/WOA)

- [StA Installer](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/download/dualboot/StA_Installer_miatoll.exe)

### Setup - Android
- Download and install the WOA Helper app, then open it and grant it root access.
- Download the **UEFI** image for your panel and place it inside the folder named `UEFI` in your internal storage.
- Press the `Mount Windows` button to mount Windows to your internal storage at `/sdcard/Windows`
> [!Important]
> If `/sdcard/Windows` is empty, your rom does not support mounting and you will have to make a boot.img backup inside the app, then copy it manually to Windows once you boot to it (for example by uploading it somewhere and then downloading it while booted into Windows). The same applies to the STA installer.
>
> Do the same thing if the folder is read-only.
- Download and move the **StA_Installer_miatoll.exe** to `/sdcard/Windows`.
- Return to the WOA Helper app and press the `Quickboot` button.

### Setup - Windows
- Navigate to `C:\StA_Installer_miatoll.exe` and run it. If it doesn't work, make sure that any antivirus software is off, as it will probably not let the app run.

#### Booting to Android
- Run the new shortcut on your desktop (you can also pin it to your start menu / taskbar for ease of access)

#### Booting to Windows
- Press `Quickboot to Windows` inside the app, or use the newly created toggle in your quick settings panel
  
## Finished!
