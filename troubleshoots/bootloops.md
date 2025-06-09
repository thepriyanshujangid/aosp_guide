# 🔄 Fixing Bootloops

Has your Android phone gotten stuck in a loop, showing the boot animation over and over without starting up? Don't worry, that's a **bootloop**, and it's a common issue with custom ROMs. This guide will help you understand why it happens and how to fix it!

## 🤔 What's a Bootloop?

A bootloop happens when your phone tries to start Android but fails, then restarts and tries again, endlessly looping. It's like your phone is stuck in a restart cycle.

## 🤷‍♀️ Why Does My Phone Bootloop?

Bootloops usually happen after you've flashed something to your phone, like:

* **A new Custom ROM:** The ROM might be faulty, incompatible, or flashed incorrectly.
* **GApps (Google Apps):** You might have flashed the wrong version, or it conflicted with your ROM.
* **Magisk or other Mods:** Rooting tools or other system modifications can sometimes cause conflicts.
* **Wrong Wipes:** Not wiping the correct partitions before flashing (or wiping too much!).
* **Corrupted Files:** The ROM or mod files you downloaded might be damaged.

## 🛠️ Fixing the boot loops (Common)

- If bootloops happens just after flashing the rom, then you will need to clean flash the rom or **try another rom**. The rom might not be compatible with your device
- If bootloop happens after flashing a kernel, then the kernel is not supported or compatible with your rom or device. **Flashing a compatible kernel will fix** the bootloop
- If bootloop happens after flashing gapps, then try another gapps. **Flash a compitable version of gapps**
- If bootloop happend after flashing magisk, download and flash the **Magisk Uninstaller ZIP** by clicking [here](https://drive.google.com/uc?export=download&id=1A6Av4vtRUc_6tbeva6l-4GhThfRSAMX9)
- If bootloop happend after flashing a magisk/ksu module then you will need to uninstall that module. To uninstall a Magisk module using TWRP, you need to boot into TWRP recovery, navigate to the file manager, locate the module's folder within /data/adb/modules, and delete it. After deletion, reboot your device to ensure the module is removed.
- If you don't have custom recovery like TWRP then you will need to uninstall the magisk or unroot your device
- If you still can't fix the bootloop then just flash another rom or stock rom
- 
## 🛑 Important Note

If none of these steps work, your issue might be more complex or device-specific. You might need to:
* Flash your phone's **stock (factory) ROM** to fully reset it. This process varies greatly by phone brand.
* Seek help on your device's specific **XDA Developers forum** or your ROM's Telegram group.

## ✨ Helpful Tips to Avoid Bootloops

* **Always read the ROM's instructions!** They often have specific steps or requirements.
* **Back up your phone** using TWRP before flashing anything new.
* **Use the correct files:** Make sure the ROM, GApps, and other ZIPs are for your **exact phone model** and **Android version**.
