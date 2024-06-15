<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro Üzerinde Windows 11 Çalıştırma">


# Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro'da Windows Çalıştırma

## Sorunların Giderilmesi


## Cihaz android'e açılabiliyor ancak bootloader'a açılmıyor

### Gereksinimler:

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

Bu, önyükleyicinin işleyemediği birim adlarına sahip bölümlerden kaynaklanır, bunu düzeltmek için:

- Kurtarma'ya boot edin

- Telefonu PC'ye bağlayın

- PC'de Komut İstemini açın

- ``adb shell`` çalıştırın

- ``parted`` çalıştırın

- Tüm bölümleri listelemek için ``print`` komutunu çalıştırın

- Adlarında boşluk olan bölümleri arayın, örneğin "Temel Veri Bölümü" ve birim numaralarını not edin

- Şimdi ``rm <bölüm numarası>`` çalıştırın, örneğin ``rm 36``


## Dokunmatik ekran çalışmıyor

- Ekranı kapatın ve açın
