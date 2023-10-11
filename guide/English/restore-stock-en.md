<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">


# Running Windows on the Redmi Note 9 Pro

## Uninstallation

### Why is this needed?

If you want to uninstall windows this is used instead of deleting partitions manually to avoid human error + writing a whole dedicated guide to just uninstalling.

If you want to relock your bootloader you'll need your partition table to be stock.

### Prerequisites

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)
- [gpt_both0.bin](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/Binaries)

### Restore GPT
> Replace ```<gpt_both0.bin>``` with the path to the gpt_both0.bin file.

```cmd
fastboot flash partition:0 <gpt_both0.bin>
```

### Erase userdata to avoid bootloop and restore FS size
```cmd
fastboot -w
```
