<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Redmi Note 9 Pro Üzerinde Windows 11 Çalıştırma">


# Redmi Note 9 Pro'da Windows Çalıştırma

## Kaldırma

### Buna neden ihtiyaç duyuldu?

Windows'u kaldırmak istiyorsanız, insan hatasını önlemek için bölümleri manuel olarak silmek yerine bu kullanılır + sadece kaldırmaya özel bir kılavuz yazmak.

Önyükleyicinizi yeniden kilitlemek istiyorsanız, bölümleme tablonuzun stokta olması gerekir.

### Gereksinimler

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)
- [gpt_both0.bin](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/Binaries)

### GPT'yi Geri Yükle
> ``<gpt_both0.bin>`` yerine gpt_both0.bin dosyasının yolunu yazın

```cmd
fastboot flash partition:0 <gpt_both0.bin>
```

### Önyükleme döngüsünü önlemek ve FS boyutunu geri yüklemek için kullanıcı verilerini silme
```cmd
fastboot -w
```
