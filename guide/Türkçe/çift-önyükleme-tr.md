<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Redmi Note 9 Pro Üzerinde Windows 11 Çalıştırma">


# Redmi Note 9 Pro'da Windows Çalıştırma

## Android ve Windows'u sorunsuz bir şekilde çift önyükleme
> [!IMPORTANT]
> Bu kılavuzu kullanmak için root edilmiş olmanız gerekir.

### Gereksinimler
- [Magisk](https://github.com/topjohnwu/Magisk/releases/latest)
- [UEFI](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/UefiV3)
- [WOA Helper app](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/download/dualboot/woahelper.apk)
- [StA Installer](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/download/dualboot/StA_Installer_miatoll.exe)

## Çift Önyükleme uygulamasını ayarlama

### Kurulum - Android
> [!NOTE]
> Dosyaları Windows klasörüne taşıyamıyorsanız, Windows'u yeniden başlatmak yerine kapatmışsınız demektir. Bu sorunu çözmek için, Windows'a geri dönün ve yeniden başlatmayı kullanın, ardından yeniden başlatıldığında kurtarmaya önyükleme yapın ve Android'e dönmek için `Windows` önyükleme yedeğinizi kullanın.

- [WOA Helper Uygulamasını](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/download/dualboot/woahelper.apk) yükleyin ve kurun ardından açın ve root erişimi verin
- [UEFI İmajı](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/UefiV3) Uefi imajını yükleyin ve dahili depolama alanınızdaki `UEFI` adlı klasörün içine yerleştirin, bu klasör mevcut değilse oluşturun.
- WOA Helper uygulamasına dönün ve `Back up Android boot` düğmesine basın. Hem `Windows` hem de `Android` seçeneklerini seçin.
- `Mount Windows` butonuna basın , ardından  [StA_Installer_miatoll.exe](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/download/dualboot/StA_Installer_miatoll.exe) dosyasını indirip dahili depolama alanınızda yeni oluşturulan `Windows` klasörüne taşıyın.
- WOA Helper uygulamasına dönün ve `Quickboot to Windows` tuşuna basın.

### Kurulum - Windows
- C:\StA_Installer_miatoll.exe'ye gidin ve çalıştırın. Çalışmazsa, muhtemelen uygulamanın çalışmasına izin vermeyeceği için herhangi bir antivirüs yazılımının kapalı olduğundan emin olun.


##### Android'e Ön Yükleme
  - Yeni kısayolu masaüstünüzde çalıştırın (erişim kolaylığı için başlat menünüze / görev çubuğunuza da sabitleyebilirsiniz)

##### Windows'a Ön Yükleme
  - Uygulamanın içinden `Quickboot to Windows` seçeneğine basın veya hızlı ayarlar panelinizde yeni oluşturulan geçişi kullanın
  
## Bitti!