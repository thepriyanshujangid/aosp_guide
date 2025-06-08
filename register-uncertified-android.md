# 🚫 Fix "This device isn’t Play Protect certified" Error

> **Purpose:**  
> This guide helps you attempt to resolve the Play Protect certification error shown below.  
> **Note:** As of June 2025, this process may not guarantee Play Store certification on most custom ROMs, but it can help with registration and troubleshooting.

---

## 🖼️ What You Might See

<a href="https://github.com/user-attachments/assets/eeb81350-482d-4eb7-8b51-c6106b22a1c7" target="_blank">
  <img src="https://github.com/user-attachments/assets/eeb81350-482d-4eb7-8b51-c6106b22a1c7" alt="Play Protect Error" width="300">
</a>

***

## 🛠️ Steps to Try

1. **Get Your GSF Android ID**
    - Connect your device to your PC
    - Enable USB Debugging
    - Open your CMD OR Terminal
    - Run:
  <!-- # adb shell pm clear com.google.android.gsf && adb reboot -->
  
    adb root && adb shell 'sqlite3 /data/user/$(cmd activity get-current-user)/*/*/gservices.db "select * from main where name = \"android_id\";"'

  - Copy the number you get (e.g., `4399677461041051781`)

2. **Register Your Device**
    - Go to: [https://www.google.com/android/uncertified](https://www.google.com/android/uncertified)
    - Paste your GSF Android ID and click **Register**

3. **Reboot is required**
    - run
   
          adb shell pm clear com.android.vending && adb shell pm clear com.google.android.gms && adb reboot

5. **Reboot Your Device**
    - Restart your phone
    - Try opening the Play Store again

---

✨ *Good luck, and happy Android customizing!*

