# 📱 POCO X5 Pro Flashing Guide

A step-by-step guide for clean and dirty flashing with AOSP Recovery, including the correct way to flash firmware.  
**Beginner-friendly, efficient, and easy to follow!**

---

## 🗂️ What You Need

- **Unlocked bootloader** on your POCO X5 Pro  
- **Windows, Mac, or Linux** computer  
- **USB cable**  
- [Platform Tools (ADB & Fastboot)](https://developer.android.com/tools/releases/platform-tools)  
- ROM, recovery images, firmware, and add-ons (see download links below)

---

## 🚀 Clean Flash with AOSP Recovery

**This method wipes your data. Recommended for major updates or switching ROMs.**

### 1. Download Required Files

- Download `boot.img`, `dtbo.img`, and `vendor_boot.img` from [AOSP Recovery FTS+Goodix (SourceForge)](https://sourceforge.net/projects/poco-x5-pro-roms/files/Aosp_Recovery_Fts%2BGoodix/)
- Unzip the file to extract the images.

### 2. Connect Your Phone to the PC

- Use a reliable USB cable.

### 3. Enter Fastboot Mode

- Power off your phone.
- Hold **Power** + **Volume Down** until you see the fastboot screen.

### 4. Flash Recovery Images

Open a terminal (CMD/PowerShell on Windows, Terminal on Mac/Linux) in the folder with your images, then run:

```
fastboot flash vendor_boot vendor_boot.img
fastboot flash dtbo dtbo.img
fastboot flash boot boot.img
fastboot reboot recovery
```

### 5. Wipe Data / Factory Reset

- In recovery, select **Wipe Data/Factory Reset** and confirm.

### 6. Sideload the ROM

- In recovery, select **Apply Update from ADB**.
- On your PC, run:

    ```
    adb sideload Rom_Name.zip
    ```

### 7. Wipe Data Again

- After sideload completes, select **Wipe Data/Factory Reset** again and confirm.

### 8. Reboot System

- Reboot your device to system.

### 9. (Optional) Sideload Add-ons

- To flash Magisk, GApps, or other add-ons, reboot to recovery and repeat the sideload process.

---

## ⚡ Dirty Flash (Update Without Data Wipe)

**Use this if you want to update your ROM without losing your data.**

1. Reboot to recovery (**Power** + **Volume Up**).
2. Select **Apply Update from ADB**.
3. On your PC, run:

    ```
    adb sideload Rom_Name.zip
    ```

4. After installation, select **Reboot System**.

---

## 🆕 Flashing Firmware (Beginner Friendly)

Flashing the latest firmware can fix compatibility or hardware issues.  
**Always use the correct firmware for your device and region!**

- **Permanent firmware page:** [POCO X5 Pro Firmware (xmfirmwareupdater.com)](https://xmfirmwareupdater.com/firmware/redwood/)

### How to Flash Firmware (AOSP Recovery)

1. **Download the latest firmware zip** for your device from the link above.  
   (File is usually named like `fw_redwood_miui_REDWOOD...zip`)
2. **Boot into AOSP recovery**:
    - Power off your phone.
    - Hold **Power** + **Volume Up** until recovery starts.
3. In recovery, select **Apply Update from ADB**.
4. On your PC, run:

    ```
    adb sideload fw_redwood_xxxxx.zip
    ```

   *(Replace `fw_redwood_xxxxx.zip` with the actual firmware file name.)*

5. Wait for the process to complete.
6. (Optional) After flashing firmware, you can sideload your ROM or reboot the system.

---

## 🔄 Change Partition Slot (Optional)

If your device doesn't switch slots automatically, do this:

```
adb reboot bootloader
fastboot getvar current-slot
fastboot --set-active=b   # (If current slot is A, set to B. If B, set to A.)
fastboot reboot
```

---

## 🐧 Linux Fastboot Permission Issues

If you get permission errors on Linux, use `sudo $(which fastboot)` instead of just `fastboot`:

```
sudo $(which fastboot) devices
sudo $(which fastboot) flash vendor_boot vendor_boot.img
```

---
**You’re ready to flash! If you have questions, check your device’s community or support forums for help.**
