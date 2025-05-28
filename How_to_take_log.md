# Android ADB Log Capture Guide (Beginner Friendly)

This guide will help you collect logs from your Android phone using your computer.  
You can use these logs to help fix problems or share them with support teams.

---

## What You Need

- Android phone
- USB cable to connect your phone to your computer
- Windows PC, Mac, or Linux computer
- [Android Platform Tools (ADB)](https://developer.android.com/tools/releases/platform-tools) installed on your computer

---

## Step 1: Enable Developer Options

1. Open the **Settings** app on your phone.
2. Scroll down and tap **About Phone**.
3. Find **Build Number** (sometimes under "Software Information").
4. Tap **Build Number** 7 times quickly.
5. You will see a message:  
   _"You are now a developer!"_

---

## Step 2: Enable USB Debugging

1. Go back to the main **Settings** screen.
2. Tap **Developer Options** (usually at the bottom or under "System").
3. Find **USB Debugging** and turn it ON.
4. If asked, tap **OK** to confirm.

---

## Step 3: Connect Your Phone to Your Computer

1. Use a USB cable to connect your phone to your computer.
2. If your phone asks for permission to allow USB debugging, tap **Allow**.

---

## Step 4: Open Command Prompt or Terminal

- **Windows:**  
  Press `Windows + R`, type `cmd`, and press Enter.

- **Mac or Linux:**  
  Open the **Terminal** app.

---

## Step 5: Check That Your Phone is Connected

1. In the command window, type:
    ```
    adb devices
    ```
2. Press Enter.
3. You should see a list of devices.  
   If you see your device’s serial number, you’re connected!

---

## Step 6: Start Capturing Logs

1. In the same command window, type:
    ```
    adb logcat > file.txt
    ```
2. Press Enter.
3. Your phone is now sending logs to a file called **file.txt**.

---

## Step 7: Reproduce the Problem

- On your phone, do the thing that causes the problem (for example, open the app that crashes).
- Try to make the issue happen while the log is being captured.

---

## Step 8: Stop Capturing Logs

- Go back to the command window.
- Press `Ctrl + C` on your keyboard to stop the logging.

---

## Step 9: Find and Share the Log File

- Look for the **file.txt** file in the folder where you ran the command.
- Send this file to your support team or developer.

---

## Troubleshooting & Tips

- **Device not showing in Step 5?**  
  - Make sure your USB cable supports data transfer.
  - Confirm you allowed USB debugging on your phone.
  - Try another USB port or cable if needed.

- **Keep the log file small:**  
  - Start capturing logs just before you reproduce the problem, and stop right after.

- **Logcat runs in real-time:**  
  - The log collection will continue until you stop it with `Ctrl + C`[2][1].

---

## Video Guide

For a visual walkthrough, see the video and screenshot below:

<br> <a href="https://github.com/user-attachments/assets/81e826a2-cb90-4dcc-8e3c-6c42f0234163" target="_blank"> <img src="https://github.com/user-attachments/assets/81e826a2-cb90-4dcc-8e3c-6c42f0234163" width="300"> </a> <br> <br> 
![Screencast 2024-08-06 18_13_20](https://github.com/user-attachments/assets/fca838d1-fc2b-4542-a96d-ff0b6f1ed7e1)
---

**You’re done! If you have questions, ask your support team for help.**
