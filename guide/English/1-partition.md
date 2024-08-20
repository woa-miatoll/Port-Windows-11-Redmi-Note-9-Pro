<img align="right" src="https://github.com/woa-miatoll/Port-Windows-11-Redmi-Note-9-Pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Running Windows on the Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Installation

### Prerequisites
- [```Recovery Image```](https://github.com/woa-miatoll/Port-Windows-11-Redmi-Note-9-Pro/releases/tag/Recoveries)

- [```Android platform tools```](https://developer.android.com/studio/releases/platform-tools)

- ```Brain (Very important)```

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
> It is recommended to keep this window open and use it throughout the entire guide.
> 
> Replace `path\to\platform-tools` with the actual path to the platform-tools folder, for example **C:\platform-tools**.
```cmd
cd path\to\platform-tools
```

#### Flash OFOX recovery
> Boot into fastboot mode, then run the following command, replacing `path\to\ofox.img` with the actual path of the image
```cmd
fastboot flash recovery path\to\ofox.img reboot recovery
```

#### Run the partitioning script
> Replace **$** with the amount of storage you want Windows to have (do not add GB, just write the number)
> 
> If it asks you to run it once again, do so
```sh
adb shell partition $
```

#### Check if Android still starts
```cmd
adb reboot
```
> Set up your device, then go to the next step

## [Next step: Installing Windows](2-install.md)
