  <img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Redmi Note 9 Pro Üzerinde Windows 11 Çalıştırma">


# Redmi Note 9 Pro'da Windows Çalıştırma

## Kurulum

## Cihazınızı bölümlere ayırma

### Ön Koşullar

- [Modded OFOX](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/modded-ofox)

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

### Notlar:
> [!Uyarı]
> Tüm verileriniz silinecek! Gerekirse şimdi yedekleyin.
>
> Bu komutlar test edilmiştir.
>
> `udevadm` uyarılarını yoksay.
>
> Aynı komutu iki kez çalıştırmayın.
>
> Bir hata yaptığınızı düşünüyorsanız TELEFONUNUZU YENİDEN BAŞLATMAYIN, [Telegram sohbet](https://t.me/+ZZQCSx2n6Pk1M2Y9) adresinden yardım isteyin
>
> Tüm komutları aynı anda çalıştırmayın, sırayla çalıştırın!
>
> HİÇBİR HATA YAPMAYIN!!! AŞAĞIDAKİ KOMUTLARI YANLIŞ YAPARSANIZ CİHAZINIZI BOZABİLİRSİNİZ!!!

##### Bu komut ile PC üzerinden OFOX kurtarmayı önyükleyin
```cmd
fastboot boot <ofpx.img>
```

#### Tüm bölümlerin bağlantısını kaldırın
OFOX ayarlarına gidin ve tüm bölümlerin bağlantısını kaldırın

#### Bölümlemeye başla
```sh
Adb shell parted /dev/block/sda
```

#### `userdata` bölümünü silme
> 18'in userdata bölüm numarası olduğundan emin olmak için şu komutu çalıştırabilirsiniz
>  `print all`
```sh
rm 18
```

#### Bölümleri oluştur
> Görmezden gelmenizi veya iptal etmenizi söyleyen herhangi bir uyarı mesajı alırsanız, i yazıp enter tuşuna basmanız yeterlidir

<details>
<summary><b><strong>64GB Modeller İçin</strong></b></summary>

- ESP bölümünü oluşturun (Windows önyükleyici verilerini ve EFI dosyalarını depolar)
```sh
mkpart esp fat32 11GB 11.4GB
```

- Windows'un yükleneceği ana bölümü oluşturun
```sh
mkpart win ntfs 11.4GB 42.4GB
```
  
- Android'in veri bölümünü oluşturun
```sh
mkpart userdata ext4 42.4GB 59.4GB
```

  </summary>
</details>

<details>
<summary><b><strong>128GB Modeller İçin</strong></b></summary>


- ESP bölümünü oluşturun (Windows önyükleyici verilerini ve EFI dosyalarını depolar)
```sh
mkpart esp fat32 11GB 11.4GB
```

- Windows'un yükleneceği ana bölümü oluşturun
```sh
mkpart win ntfs 11.4GB 65.4GB
```
  
- Android'in veri bölümünü oluşturun
```sh
mkpart userdata ext4 65.4GB 123GB
```
  </summary>
</details>

#### EFI görüntüsünün algılanabilmesi için ESP bölümünü önyüklenebilir hale getirin
```sh
set 18 esp on
```

#### OFOX'u Yneiden Başlat

#### Bilgisayarınızda komut istemini yeniden başlatın
```cmd
adb shell
```

#### Bölümleri Biçimlendirme
-  ESP bölümünü FAT32 olarak biçimlendirin
```sh
mkfs.fat -F32 -s1 /dev/block/by-name/esp -n ESPMIATOLL
```

-  Windows bölümünü NTFS olarak biçimlendirme
```sh
mkfs.ntfs -f /dev/block/by-name/win -L WINMIATOLL
```

- Verileri Biçimlendirin
Wipe menüsüne gidin ve Format Data öğesine basın ardından `yes` yazın.

#### Android'in hala başlayıp başlamadığını kontrol edin
Sadece telefonu yeniden başlatın ve Android'in hala çalışıp çalışmadığına bakın


## [Sonraki Adım: Windows'u Yükleme](2-kurulum-tr.md)
