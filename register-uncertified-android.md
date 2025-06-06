# 🚫 Fix "This device isn’t Play Protect certified" Error

> **Purpose:**  
> This guide helps you attempt to resolve the Play Protect certification error shown below.  
> **Note:** As of June 2025, this process may not guarantee Play Store certification on most custom ROMs, but it can help with registration and troubleshooting.

---

## 🖼️ What You Might See

![Play Protect Error](image.png)

---

## 🛠️ Steps to Try

1. **Get Your GSF Android ID**
    - Connect your device to your PC
    - Enable USB Debugging
    - Run:
      ```
      adb shell 'sqlite3 /data/user/$(cmd activity get-current-user)/*/*/gservices.db "select * from main where name = \"android_id\";"'
      ```
    - Copy the number you get (e.g., `4399677461041051781`)

2. **Register Your Device**
    - Go to: [https://www.google.com/android/uncertified](https://www.google.com/android/uncertified)
    - Paste your GSF Android ID and click **Register**

3. **Clear Data for Google Play Store & Google Play Services**
    - Go to **Settings > Apps > See all apps**
    - Tap **Google Play Store**
        - Tap **Storage & cache**
        - Tap **Clear Cache** and **Clear Storage/Data**
    - Tap **Google Play Services**
        - Tap **Storage & cache**
        - Tap **Clear Cache** and **Clear Storage/Data**

4. **Reboot Your Device**
    - Restart your phone
    - Try opening the Play Store again

---

✨ *Good luck, and happy Android customizing!*

