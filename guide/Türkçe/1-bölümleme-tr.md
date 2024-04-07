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

#### Start parted
```sh
Adb shell parted /dev/block/sda
```

#### Delete the `userdata` partition
> You can make sure that 18 is the userdata partition number by running
>  `print all`
```sh
rm 18
```

#### Create partitions
> If you get any warning message telling you to ignore or cancel, just type i and enter

<details>
<summary><b><strong>For 64GB Models</strong></b></summary>

- Create the ESP partition (stores Windows bootloader data and EFI files)
```sh
mkpart esp fat32 11GB 11.4GB
```

- Create the main partition where Windows will be installed to
```sh
mkpart win ntfs 11.4GB 42.4GB
```
  
- Create Android's data partition
```sh
mkpart userdata ext4 42.4GB 59.4GB
```

  </summary>
</details>

<details>
<summary><b><strong>For 128GB Models</strong></b></summary>


- Create the ESP partition (stores Windows bootloader data and EFI files)
```sh
mkpart esp fat32 11GB 11.4GB
```

- Create the main partition where Windows will be installed to
```sh
mkpart win ntfs 11.4GB 65.4GB
```
  
- Create Android's data partition
```sh
mkpart userdata ext4 65.4GB 123GB
```
  </summary>
</details>

#### Make ESP partiton bootable so the EFI image can detect it
```sh
set 18 esp on
```

#### Reboot to OFOX

#### Start the shell again on your PC
```cmd
adb shell
```

#### Format partitions
-  Format the ESP partiton as FAT32
```sh
mkfs.fat -F32 -s1 /dev/block/by-name/esp -n ESPMIATOLL
```

-  Format the Windows partition as NTFS
```sh
mkfs.ntfs -f /dev/block/by-name/win -L WINMIATOLL
```

- Format data
Go to Wipe menu and press Format Data, 
then type `yes`.

#### Check if Android still starts
Just restart the phone, and see if Android still works


## [Next step: Installing Windows](2-install-en.md)
