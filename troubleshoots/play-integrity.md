# 🛡️ Fixing Play Integrity on Custom ROMs

Google Play Integrity is a crucial security check by Google that determines if your Android device is trustworthy. It largely replaced the older SafetyNet attestation. Passing Play Integrity is essential for many apps to function correctly, including banking apps, streaming services (like Netflix, Disney+), Google Wallet/Pay, and games.


Now a days, Play integrity is a big issue. Google is imposing heavy restrictions on android that is making it impossible to use custom roms. This guide tells you how you can fix play integrity issues on your android.

## Types of integrity

* **`MEETS_BASIC_INTEGRITY`**: Checks if the device is generally free from known malware and basic rooting. This is relatively easy to pass.
* **`MEETS_DEVICE_INTEGRITY`**: Checks the integrity of the device's hardware and software, looking for signs of tampering, such as unlocked bootloaders, custom ROMs, or active root. **This is the primary target for custom ROM users.**
* **`MEETS_STRONG_INTEGRITY`**: This is a hardware-backed security check that uses a secure key. It's almost impossible to pass if you have an unlocked bootloader or custom ROM, as it verifies the device's factory-level integrity. Most users with custom ROMs won't be able to achieve this.

**Our goal is to pass `MEETS_DEVICE_INTEGRITY` and `MEETS_BASIC_INTEGRITY`.**

## 💡 Why Does Play Integrity Fail?

Play Integrity will typically fail on devices with:

* Unlocked Bootloader
* Custom ROMs
* Active Root (e.g., Magisk)
* Custom Kernels
* Modified System Partitions


## 🚀 3 Steps to Pass Google Play Integrity
> [!NOTE]
> You must have either Magisk/KSU or apach installed on your device. If you don't have any of these then you can't proceed with the fix
Follow these steps carefully. The exact order and success can sometimes depend on your device and ROM.

### Step 1: Turn of build in spoofing

1.  Open misclenous/spoofing settings of your rom
2.  Turn of the settings with name **PI spoof** or **GSM Spoof**
3.  Reboot

### Step 2: Installing modules

Download and install the following modules in the same order
- [Zygisk next](https://github.com/Dr-TSNG/ZygiskNext/releases/latest) : Only if you are on KSU/apach, reboot needed
- [PlayIntegrityFork](https://github.com/osm0sis/PlayIntegrityFork/releases/latest)
- [TrickyStore](https://github.com/5ec1cff/TrickyStore/releases/latest)
- [Integrity-Box](https://github.com/MeowDump/Integrity-Box/releases/latest)

### Step 3 : Clearing cached data
After installing all the modules, clear the play store & google play services data.
**Finally, reboot**

🎯 **Now you should have your all three intergrity passing**

> [!Important]
> If your apps does not require strong integrity, then please switch to AOSP keybox by clicking on the action button below the module name and choosing the AOSP keybox option.


## 🐛 Troubleshooting & Common Issues

* **Still Failing?**
    * **Re-flash the Play Integrity Fix module:** Sometimes a re-flash helps.
    * **Check Zygisk:** Ensure Zygisk is still enabled in Magisk settings.
    * **Disable other Magisk modules:** One of your other modules might be causing a conflict. Try disabling all other modules except the Play Integrity Fix, reboot, and check again. Re-enable them one by one to find the culprit.
    * **Try a different version/fork of the fix:** Play Integrity is constantly updated by Google, so module developers release new versions. Your current module might be outdated, or another fork might work better for your device/ROM.
    * **"Device is certified" but apps still complain?** Sometimes clearing Play Store data isn't enough. Go to `Settings > Apps > Show system apps`, find "Google Play services for Instant Apps" and "Google Services Framework", and clear their storage/cache as well. Then reboot.

* **Persistent `MEETS_DEVICE_INTEGRITY` failure:**
    * Some devices or ROMs might require **spoofing your device's fingerprint**. You might need a module like **MagiskHide Props Config**.
        1.  Install the **MagiskHide Props Config** module (from Magisk Modules or its GitHub).
        2.  Reboot.
        3.  Open a terminal app on your phone (e.g., Termux) or use `adb shell` from your PC.
        4.  Type `su` and grant root.
        5.  Type `props`.
        6.  Follow the prompts to select "Edit device fingerprint" (option `1`), then "Pick a certified fingerprint" (option `f`), then choose your device brand and a recent, certified model (e.g., a Pixel model).
        7.  Reboot your device.
        8.  Clear Play Store & Play Services data again (Step 3).
        9.  Verify (Step 4).

* **"Integrity Failed" right after boot/flashing Play Integrity Fix:**
    * This can sometimes be caused by older `zygisk_detatch` modules (if you ever used one). If you have a folder like `/data/adb/modules/zygisk_detatch/`, try deleting it in TWRP or via a root file manager.

## 🚨 Important Notes
Play Integrity is an ongoing battle. Google constantly updates its checks, meaning a working fix today might break tomorrow. Keep an eye on the module's development thread or community discussions. Altho, this method is working as of now (10/6/2025). There is no garuntee that this will also work in future. As we find a new way, we will update this guide.

---

Thanks to @MeowDump , @TrickyStore and @osm0sis for providing the modules. Without of these 3 heros, it would not have been possible to use custom roms in 2025
