# macOS: allowing the plugin · macOS: как разрешить плагин

**Why you see a warning · Почему появляется предупреждение.**
Apple asks developers to pay a yearly fee for a certificate ("notarisation"). I cannot pay it from my country, so Best Trigger 3 is
**not notarised**. macOS therefore says that it "cannot verify the developer". The plugin is safe, and you decide to trust it
once. · Apple требует от разработчиков ежегодный платный сертификат («нотаризацию»). Из моей страны оплатить его невозможно,
поэтому Best Trigger 3 **не нотаризован**, и macOS пишет, что «не может проверить разработчика». Плагин безопасен, вы один раз
разрешаете его сами.

---

## English

### 1. The installer will not open
macOS: *"…cannot be opened because the developer cannot be verified"*.
- **Right-click** (or Control-click) the installer file → **Open** → **Open**. This only has to be done once.
- Or: open **System Settings → Privacy & Security**, scroll down to the message about the blocked file and click **Open Anyway**.

### 2. The plugin is installed but your DAW does not show it, or says it cannot be loaded
- Open **System Settings → Privacy & Security** and click **Open Anyway** next to the message about "Best Trigger 3", then rescan plugins in your DAW.
- If there is no such message, remove the quarantine mark. Open **Terminal** (Applications → Utilities) and paste:

```bash
xattr -dr com.apple.quarantine "/Library/Audio/Plug-Ins/VST3/Best Trigger 3.vst3"
```

  (For the free version: `Best Trigger 3 Free.vst3`. If you installed the plugin only for yourself, the folder is
  `~/Library/Audio/Plug-Ins/VST3/`.) Then restart your DAW and rescan.

### 3. Still not loading?
Write to me (the address is on the download page) and tell me your macOS version, your DAW and whether the Mac has an Apple chip (M1/M2/M3…) or Intel.

---

## Русский

### 1. Установщик не открывается
macOS пишет: *«…невозможно открыть, так как не удаётся проверить разработчика»*.
- Нажмите на файл установщика **правой кнопкой** (или Control + клик) → **Открыть** → **Открыть**. Это нужно сделать один раз.
- Или: **Системные настройки → Конфиденциальность и безопасность**, прокрутите вниз до сообщения о заблокированном файле и нажмите **«Всё равно открыть»**.

### 2. Плагин установлен, но DAW его не показывает или не может загрузить
- Откройте **Системные настройки → Конфиденциальность и безопасность**, найдите сообщение про «Best Trigger 3» и нажмите **«Всё равно открыть»**, затем пересканируйте плагины в DAW.
- Если такого сообщения нет, уберите отметку карантина. Откройте **Терминал** (Программы → Утилиты) и вставьте:

```bash
xattr -dr com.apple.quarantine "/Library/Audio/Plug-Ins/VST3/Best Trigger 3.vst3"
```

  (Для бесплатной версии: `Best Trigger 3 Free.vst3`. Если вы ставили плагин только для себя, папка:
  `~/Library/Audio/Plug-Ins/VST3/`.) Затем перезапустите DAW и пересканируйте плагины.

### 3. Всё равно не загружается?
Напишите мне (адрес на странице загрузки): версия macOS, ваш DAW и какой у Mac процессор: Apple (M1/M2/M3…) или Intel.
