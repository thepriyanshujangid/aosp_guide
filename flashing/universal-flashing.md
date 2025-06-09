# ⚡ Universal Flashing Guide

This guide provides a concise, step-by-step overview for flashing custom AOSP-based ROMs on both A/B (seamless update) and A-only Android devices. It focuses on the essential steps required for a clean installation.

> [!CAUTION]
> Flashing custom ROMs carries risks. **Proceed with extreme caution and at your own risk.** Back up all important data.

## 🛠️ Prerequisites

1.  **Unlocked Bootloader:** Essential for flashing custom software.

2.  **Custom/AOSP Recovery (TWRP/Linage recommended):** Installed and working for your specific device model. If your device does not have custom recovery then install any AOSP recovery or linage recovery

3.  **ADB & Fastboot:** Set up on your PC.

4.  **Custom ROM ZIP:** The correct ROM for your exact device model and Android version.

5.  **GApps ZIP (Optional):** If your ROM doesn't include Google apps.

6.  **Magisk ZIP (Optional):** For rooting.

7.  **Sufficient Battery:** At least 50%.
8.  A working computer or any adb host device that can run adb commands

## 🚀 Step-by-Step Instructions

### Step 1. Perform a Wipe (Clean)
* Firstly, formate the data
* In TWRP, tap `Wipe` > `Advanced Wipe`.

* **Select these partitions:**

    * `Dalvik / ART Cache`

    * `Cache`

    * `System`

    * `Vendor` (if present)

    * `Data`

    * `Internal Storage`
  
> [!TIP]
> If you have AOSP recovery then you can skip this wiping step, but **Format data is required**


## Flashing custom rom
#### For OrangeFox/TWRP recovery:
Goto advance tab, Click on ADB sideload. Swipe to start ADB Sideload
#### On AOSP/Linage recovery
Click on Apply update

Once you have started the ADB sideload, run the follwoing command on CMD to install the rom
```
adb sideload path_to_your_rom.zip
```
Replace the _path_to_your_rom_ with the actual zip

> [!NOTE]
> If it says something like "Signature varification failed, proceed?", simply click **yes**

> [!TIP]
> This method is equalant to the install zip method of any custom recovery. You can flash any flashaable zip using this approch, be it a rom or a kernel or any module.


### 4. Flash GApps/Magisk/KSU (if applicable)

Just like you installed the rom using adb sideload command, you can install gapps, magisk or kernel zip in the same way. Just hit `adb sidelod path_to_your.zip` again.

## ⏳ First Boot

After the sideloading is completed, you can reboot to system from the recovery. The first boot can take 5-15 minutes or longer. Be patient.

## 🐛 Troubleshooting

* If you encounter bootloops, refer to the [Fixing Bootloops Guide](bootloops.md).

* For ADB/Fastboot issues, see the [ADB & Fastboot Not Recognizing Device Guide](/troubleshoots/adb-fastboot-fix.md).
