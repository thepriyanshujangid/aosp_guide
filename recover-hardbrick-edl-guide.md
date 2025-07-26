---

```markdown
# 🛠 Recover Hardbricked POCO X5 Pro (EDL Unbrick Guide)

> **Purpose:**  
> This guide helps you recover a hardbricked POCO X5 Pro using Emergency Download Mode (EDL) and Mi Flash.  
> Works even if your phone is completely unresponsive (no boot, no fastboot, no recovery).

---

## ⚠️ When to Use This Guide

Use this if:
- Your phone doesn’t boot at all.
- It doesn't enter Fastboot or Recovery mode.
- The screen stays black and only EDL mode works.

---

## 🧰 What You Need

- **A Windows PC**
- **USB-C cable**  
- **Xiaomi Mi Flash Tool** (latest version)
- **Stock Fastboot ROM** for POCO X5 Pro (Redwood)  
- **No Authentication Firehose file** (special `prog_firehose_ddr.elf`)
- (Optional) **EDL Cable** or knowledge of **Test Point** method

---

## 🔁 Step-by-Step Recovery Instructions

### 1. Download the Required Files

- **Download a full stock Fastboot ROM** for POCO X5 Pro from:  
  [MIUI ROM Download - Xiaomi](https://mirom.ezbox.idv.tw/en/phone/redwood/)
- Extract the `.tgz` ROM file completely until you get folders and `.img` files.

### 2. Replace the Firehose File

- Download the **No Authentication Firehose** ELF for Snapdragon 778G from:  
  [https://t.me/redwoodroms/1/146464](https://t.me/redwoodroms/1/146464)
- Go to your extracted firmware folder.
- Replace the existing `prog_firehose_ddr.elf` with the downloaded **No Auth** version.

---

### 3. Boot Device into EDL Mode (Emergency Download Mode)

You can enter EDL mode using one of the following methods:

#### ✅ A. Via ADB (if device responds)
```

adb reboot edl

```

#### ✅ B. Via Fastboot (if Fastboot still works)
```

fastboot oem edl

```

#### ✅ C. Using EDL Cable  
- Plug in the EDL cable (shorts USB D+ and GND internally).
- Phone will boot into EDL automatically.

#### ✅ D. Using Test Point  
- Power off the device completely.
- Open the back cover carefully.
- Short the **Test Points** using metal tweezers while plugging in USB cable.

📷 [Test Point Image](https://t.me/redwoodroms/1/146422)

---

### 4. Flash the Firmware with Mi Flash Tool

1. Open **Mi Flash Tool** as Administrator.
2. Click **Select** and choose the extracted firmware folder.
3. Choose flashing option:
    - **Clean all** *(recommended)*
4. Connect your phone (in EDL mode) to the PC.
5. You should see a COM port like `COM3` or `COM10` in Mi Flash.
6. Click **Flash** to start the process.
7. Wait until it finishes and shows success.

---

## ✅ Done!

- Your phone should reboot after flashing.
- First boot may take up to 5-10 minutes — be patient.

---

## 🧠 Tips & Troubleshooting

- If Mi Flash doesn’t detect your device:
  - Reinstall Qualcomm drivers.
  - Try different USB ports.
  - Use a different cable.

- Make sure the `prog_firehose_ddr.elf` is **replaced correctly** before flashing.
- If flashing fails midway, try again with another USB port or cable.

---

**Need help? Ask in your POCO X5 Pro Telegram community or support groups.**

```

---

