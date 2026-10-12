# macOS: allowing the plugin · как разрешить плагин

## English
**The installer will not open:** right-click it → **Open** → **Open** (once). Or **System Settings → Privacy & Security → Open Anyway**.

**The DAW does not show the plugin:** click **Open Anyway** next to the message about "Best Trigger 3" in **Privacy & Security**, then rescan plugins. If there is no message, paste in Terminal:

```
xattr -dr com.apple.quarantine "/Library/Audio/Plug-Ins/VST3/Best Trigger 3.vst3"
```

(Free version: `Best Trigger 3 Free.vst3`.) Restart the DAW and rescan.

## Русский
**Установщик не открывается:** правый щелчок → **Открыть** → **Открыть** (один раз). Или **Системные настройки → Конфиденциальность и безопасность → Всё равно открыть**.

**DAW не видит плагин:** в **Конфиденциальность и безопасность** нажмите **Всё равно открыть** у сообщения про «Best Trigger 3» и пересканируйте плагины. Если сообщения нет, вставьте в Терминал:

```
xattr -dr com.apple.quarantine "/Library/Audio/Plug-Ins/VST3/Best Trigger 3.vst3"
```

(Бесплатная версия: `Best Trigger 3 Free.vst3`.) Перезапустите DAW и пересканируйте.
