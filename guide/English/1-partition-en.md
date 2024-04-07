  <img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">


# Running Windows on the Redmi Note 9 Pro

## Installation

## Partitioning your device

### Prerequisites

- [Modded OFOX](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/modded-ofox)

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

### Notes:
> [!Warning]
> All your data will be erased! Backup now if needed.
>
> These commands have been tested.
>
> Ignore `udevadm` warnings
>
> Do not run the same command twice
>
> DO NOT REBOOT YOUR PHONE if you think you made a mistake, ask for help in the [Telegram chat](https://t.me/+ZZQCSx2n6Pk1M2Y9)
>
> Do not run all commands at once, execute them in order!
>
> DO NOT MAKE ANY MISTAKE!!! YOU CAN BREAK YOUR DEVICE WITH THE COMMANDS BELOW IF YOU DO THEM WRONG!!!

##### Boot OFOX recovery through the PC with the command
```cmd
fastboot boot <ofpx.img>
```

#### Unmount all partitions
Go to OFOX settings and unmount all partitions

#### Run the partitioning script
> Replace **$** with the amount of storage you want Windows to have (do not add GB, just write the number)
> 
> If it asks you to run it once again, do so
```sh
adb shell partition $
```

#### Check if Android still starts
Just restart the phone, and see if Android still works


## [Next step: Installing Windows](2-install-en.md)
