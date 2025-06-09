When diving into the world of Android custom ROMs, you'll often hear about "firmware." This guide explains what firmware is, why it's crucial for your device, and how to properly install it when flashing custom ROMs.

# ❓ What is Firmware?
In simple terms, firmware is a type of permanent software that's embedded into your device's hardware. Unlike the Android operating system (your custom ROM), which handles applications and user interaction, firmware controls the physical components of your phone.

Think of it as the low-level operating system for specific parts of your phone's hardware. This includes:

- Modem/Baseband: Manages cellular connectivity (calls, SMS, mobile data).

- Bluetooth/Wi-Fi: Controls wireless communication.

- Touchscreen/Display: Interfaces with your screen.

- Cameras: Manages camera sensors and processing.

- Fingerprint Sensor: Handles biometric authentication.

**If you have any of these no working then you need to flash firmware of your device. This does not require formating data.**

> [!Note]
> Not all mobile vendors distribute their firmware separately like xiaomi do. For those device vendors, you will need to flash the stock firmware (stock rom) before flashing the custom rom.

# 🎯 Fixing wifi/bluetooth/fingerprint problem
Unless there is a bug in the rom, these problem can often be fixed by flashing latest firmware of your device. If your device company does not give firmware separatly then you will need to flash the stock rom before installing the custom rom.

**Step 1** : Download the latest firmware for your device
For example, firmware for redwood (Poco x5 pro) can be found [here](https://xmfirmwareupdater.com/firmware/redwood/)

**Step 2**

- If you have custom recovery installed & the downloaded firmware is on your device
  Then just boot into the recovry and install the firmware zip
- If you are on AOSP recovery or you do not have firmware on the device
  Then start adb sideload (Apply update on AOSP recovery) and run the adb sideload command:
  `adb sideload firmware.zip`
Make sure to replace the file path

**Step 3** :  Reboot!
Your firmware is installed and you should be able to use the features that you were not able to before!


> [!IMPORTANT]
> Always read your Custom ROM's installation instructions carefully. They will specify any required firmware version.
> Never flash firmware not explicitly made for your device.
