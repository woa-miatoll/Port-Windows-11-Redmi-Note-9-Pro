  <img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Redmi Note 9 Pro Üzerinde Windows 11 Çalıştırma">


# Redmi Note 9 Pro'da Windows Çalıştırma

## Kurulum

## Windows'u Yükleme
> Mount'ta MTP'yi devre dışı bırakmanız gerekecek

### Gereksinimler

- [ARM üzerinde Windows ISO'su (Windows 11 önerilir)](https://uupdump.net/)
- [UEFI İmajı](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/UefiV3)
- [Sürücüler](https://github.com/N1kroks/7xx-Drivers/releases/latest)
- Beyin (Çok önemli)

#### Msc Komut Dosyasını Çalıştırın

```cmd
adb shell msc
```

### Disklere Harf Atama
  

#### Windows disk yöneticisini başlatın
> [!Warning]
> DISKPART'TA İKEN SİLME, OLUŞTURMA YA DA BAŞKA BİR DEĞİŞİKLİK YAPMAYIN!!! BU BÜTÜN UFS'NİZİ SİLECEKTİR YA DA FASTBOOT'A BOOT ETMENİZİ ENGELLEYECEKTİR!!! BU CİHAZINIZIN ÇÖZÜMÜ OLMAKSIZIN KALICI OLARAK BRICK OLDUĞU ANLAMINA GELİR! (cihazı Xiaomi servisine götürme ya da EDL ile flashlama elbette bir çözümdür ancak iki çözüm de ücretsiz değildir.)

> Note 9 Pro Bir Disk Olarak Algılandığında

```cmd
diskpart
```


### Windows birimine `X` atayın

#### Telefonun Windows birimini seçin
> Bulmak için `list volume` kullanın, "WINMIATOLL" adlı birimdir.

```diskpart
select volume <sayı>
```

#### X harfini atayın
```diskpart
assign letter=x
```

### Esp birimine `Y` atayın

#### Telefonun ESP birimini seçin
> Bulmak için `list volume` kullanın, "ESPMIATOLL" adlı birimdir.

```diskpart
select volume <sayı>
```

#### Y harfini atayın

```diskpart
assign letter=y
```

#### Diskpart'tan çıkın
```diskpart
exit
```

## Kurulum

> `<path/to/Install.wim>` yerine install.wim dosyasının yolunu yazın

> `install.wim` ISO'nun içinde sources klasöründedir
> ISO'yu monte ettikten veya çıkardıktan sonra alabilirsiniz

```cmd
dism /apply-image /ImageFile:<path/to/install.wim> /index:1 /ApplyDir:X:\
```

### Sürücüleri Kurma

>Sürücü dosyasını çıkarın ve 'OfflineUpdater.cmd' dosyasını açın. WINMIATOLL sürücüsünün harfini yazın (X olmalıdır) ve enter tuşuna basın.

### EFI için Windows önyükleyici dosyaları oluşturma

```cmd
bcdboot X:\Windows /s Y: /f UEFI
```

## İmzasız sürücülere izin ver

> Bunu yapmazsanız bir BSOD(Blue Screen Of Death) alırsınız

```cmd
bcdedit /store Y:\EFI\Microsoft\BOOT\BCD /set {default} testsigning on
```

## Windows'a önyükleme

### Ne tür bir panele sahip olduğunuzu kontrol edin

> Komut istemini açın
```cmd
adb shell panel
```

### `<uefi.img>` dosyasını cihaza taşıyın

```cmd
adb push <uefi.img> /sdcard
```

#### microSD kartınız varsa bunu kullanın

```cmd
adb push <uefi.img> /external_sd
```


### Mevcut önyükleme görüntünüzün yedeğini alın
> Sadece bir kez yapmalısın

> Mümkünse microSD karta yerleştirin


### OFOX'tan uefi görüntüsünü flaşlayın
`uefi.img` dosyasına gidin ve bunu boot bölümüne flaşlayın

## Android'e geri dönün
> OFOX'dan yedek önyükleme görüntünüzü kullanın

## [Sonraki İstege Bağlı Adım: Dualboot (Çift Sistem) Kurma](çift-önyükleme-tr.md)
