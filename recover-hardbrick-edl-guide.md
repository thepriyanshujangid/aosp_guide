# Unbrick Poco X5 Pro (Redwood) via EDL Mode – No Auth Needed

---

## ✅ Requirements

- 📱 Poco X5 Pro detected as **Qualcomm HS-USB QDLoader 9008 (EDL mode)**
- 🖥️ Windows PC + USB cable
- 🧰 [MiFlash Tool (2022+)](https://xiaomiflashtool.com/)
- 📦 Full **Redwood Fastboot ROM** (MIUI stock)
- 🔓 Custom no-auth firehose:  
  [`prog_firehose_ddr.elf`](https://github.com/thepriyanshujangid/aosp_guide/releases/download/recover-hardbrick-edl-guide/prog_firehose_ddr.elf)

---

## ⚙️ Flashing Steps

1. **Download** & **extract** a full fastboot ROM for *Redwood*.
2. **Replace** the original `prog_firehose_ddr.elf` in the ROM folder with this one:  
   [`prog_firehose_ddr.elf`](https://github.com/thepriyanshujangid/aosp_guide/releases/download/recover-hardbrick-edl-guide/prog_firehose_ddr.elf)
3. ✅ If your device is **already detected as Qualcomm HS-USB QDLoader 9008**, you’re good to go — it’s already in EDL mode!

   <a href="https://github.com/user-attachments/assets/70ed863d-f572-4469-be7b-3d1863093f48" target="_blank">
     <img src="https://github.com/user-attachments/assets/70ed863d-f572-4469-be7b-3d1863093f48" alt="9008 Port Detected" width="350">
   </a>

4. ❗If not detected, enter EDL mode using:
   - 🔌 **EDL cable**, or  
   - 🔧 **Test Point method**:
     
     <a href="https://github.com/user-attachments/assets/54414b57-5a6b-489a-ab52-3ef28979a34a" target="_blank">
       <img src="https://github.com/user-attachments/assets/54414b57-5a6b-489a-ab52-3ef28979a34a" alt="Test Point Method" width="400">
     </a>

5. Launch **MiFlash Tool**:
   - Click `Select` → Choose the ROM folder
   - Set flashing mode to `Clean all`
   - Click 🔘 **Flash**

---

## 🎉 Flash Success Example

<a href="https://github.com/user-attachments/assets/2f669346-6f87-45f0-8161-2edd4904f6c6" target="_blank">
  <img src="https://github.com/user-attachments/assets/2f669346-6f87-45f0-8161-2edd4904f6c6" alt="Flash Success" width="350">
</a>

---

## 📝 Notes

- 🔓 This firehose **bypasses Xiaomi authentication**
- 💡 No bootloader unlock or Mi Account is needed
- ✅ Works even if your device is fully bricked, as long as it enters 9008 (EDL) mode
- ⚠️ You **don’t need** to short motherboard pins or use an EDL cable **if 9008 is already detected**

---

## 🙌 Credits

- ✍️ Guide by [@thepriyanshujangid](https://github.com/thepriyanshujangid)
- 🔧 Firehose & method by **Telexec**
