<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">


# Running Windows on the Redmi Note 9 Pro

## Troubleshooting Issues


## Device can boot into android but not bootloader

### Prerequisites:

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

This is caused by partitions with volume names the bootloader cannot handle, to fix this:

- Boot to recovery

- Connect phone to PC

- Open cmd on PC

- Run ```adb shell```

- Run ```parted```

- Run ```print``` to list all partitions

- Look for partitions that have spaces in the names e.g "Basic Data Partition" and note their volume number

- Now run ```rm <vol number>``` e.g ```rm 36```


## Touchscreen doesnt work

- Turn display off and on, or your panel is Huaxing and not supported yet.
