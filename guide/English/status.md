<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro">


# Running Windows on the Redmi Note 9 Pro

## Project Status

Beta, Most of the hardware works, but some components do not work yet.

#### Features

- [ ] Audio ```It seems that it can be achieved, but it is not easy```
- [ ] Battery status
- [x] Bluetooth 
- [X] Brightness
- [ ] Camera
- [ ] Charging 
- [x] Display
- [x] GPU
- [X] LTE ```Only SIM 1 and you need to do the steps below```
- [ ] SD 
- [X] Touchscreen
- [x] UFS
- [x] USB
- [x] Wi-Fi ```You have to install it manually after starting Windows```

##### For LTE to work, you need:
1. Boot into android with SIM card inserted in slot 1.
2. Reboot into fastboot and flash the latest version of uefi.img
3. Boot into windows and everything should work
4. It will stop working if you remove the sim card tray, or switch sim slot in windows, and you will have to do these steps again

#### Sensors
- [ ] Accelerometer
- [ ] Fingerprint
- [x] GPS
- [ ] Gyroscope
- [ ] Light sensor
- [ ] Magnetometer
- [ ] Proximity
