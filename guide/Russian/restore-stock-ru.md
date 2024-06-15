<img align="right" src="https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/blob/main/Miatoll.png" width="350" alt="Windows 11 Running On A Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro">

# Windows на Redmi Note 9 Pro / 9 Pro India / 10 Lite / 9S / 9 Pro max India / Poco M2 Pro

## Удаление

### Зачем это нужно?

Если вы хотите удалить Windows, это используется вместо удаления разделов вручную, чтобы избежать человеческой ошибки + написание целого специального руководства по простому удалению.

Если вы хотите заблокировать загрузчик, вам понадобится стандартная таблица разделов.

### Требования

- [```ADB & Fastboot```](https://developer.android.com/studio/releases/platform-tools)
- [```gpt_both0.bin```](https://github.com/Rubanoxd/Port-Windows-11-redmi-note-9_pro/releases/tag/Binaries)

### Восстановление GPT
> Замените ```<gpt_both0.bin>``` путём к файл ```gpt_both0.bin```.

```cmd
fastboot flash partition:0 <gpt_both0.bin>
```

### Отчистите раздел userdata чтобы избежать цикличной перезагрузки и восстановить размер файловой системы
```cmd
fastboot -w
```
