  <img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro Üzerinde Windows 11 Çalıştırma">


# Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro'da Windows Çalıştırma

## Kurulum

## Cihazınızı bölümlere ayırma

### Gereksinimler

- [Modded OFOX](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/modded-ofox)
- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)
- Beyin (Çok önemli)

### Notlar:
> [!Warning]
> Tüm verileriniz silinecek! Gerekirse şimdi yedekleyin.
>
> Bu komutlar test edilmiştir.
>
> Aynı komutu iki kez çalıştırmayın.
>
> Bir hata yaptığınızı düşünüyorsanız TELEFONUNUZU YENİDEN BAŞLATMAYIN, [Telegram](https://t.me/woamiatoll) adresinden yardım isteyin
>
> Tüm komutları aynı anda çalıştırmayın, sırayla çalıştırın!
>
> HİÇBİR HATA YAPMAYIN!!! AŞAĞIDAKİ KOMUTLARI YANLIŞ YAPARSANIZ CİHAZINIZI BOZABİLİRSİNİZ!!!

##### Bu komut ile PC üzerinden OFOX kurtarmayı önyükleyin
```cmd
fastboot boot <ofpx.img>
```

#### Bölümleme Komut Dosyasını Çalıştırın
> Windows'un sahip olmasını istediğiniz depolama miktarını **$** ile değiştirin (GB eklemeyin, sadece sayıyı yazın)
> 
> Bir kez daha çalıştırmanızı isterse, bunu yapın
```sh
adb shell partition $
```


#### Android'in hala başlayıp başlamadığını kontrol edin
Sadece telefonu yeniden başlatın ve Android'in hala çalışıp çalışmadığına bakın


## [Sonraki Adım: Windows'u Yükleme](2-kurulum-tr.md)
