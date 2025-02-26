<p align="center">
  <img src="https://i.imgur.com/irnHU8d.png" />
</p>

# Project Elixir for Redmi K20 Pro/Mi 9T Pro (raphael/in) シ
> <p>"Redefine Simplicity with your Android experience on our minimalistic custom ROM — where sleek design meets robust security, performance, and stability."</p>

## ⊀ Unleash Innovation ⊁
> Elevate your user interface with a minimalist design and the perfect balance of customization options.

---

## ⚠️ Disclaimer  
> **Important:**  
> - Your warranty is void. Or valid, probably?  
> - We are not responsible for any damage to your device by installing custom ROMs or kernels.  
> - You do it at your own risk and take full responsibility.  
> - Be careful while following installation steps.  
> - If you are moving from Android 12/13/14 to Android 15, a **clean flash (format data) is mandatory**.  
> - Join our support group for any queries: [Tap Here](https://telegram.me/Elixir_Discussion).  

---

## 📥 Download Required Files
1. **Platform Tools (Windows)**: [platform-tools-latest-windows.zip](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)  
2. **Recovery for Android 15**: [Recovery](https://projectelixiros.com/download)  
3. **Project Elixir ROM (raphael)**: [DOWNLOAD](https://projectelixiros.com/device/raphael)  

---

## 🛠️ Installation Guide  

### Step 1: Download Required Files
1. Download the latest Android platform tools for Windows from the link below:
   - **Platform Tools Link (Windows)**: [platform-tools-latest-windows.zip](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)

2. Download the Recovery from the link below:
   - **Recovery Link [ For Android 15 ]:** [Recovery](https://projectelixiros.com/download)

3. Download the Project Elixir ROM for from a reliable source.
   - **Project Elixir ROM Link**: [DOWNLOAD](https://projectelixiros.com/download)

### Step 2: Install ADB and Boot into Fastboot Mode
1. Make sure you have ADB (Android Debug Bridge) installed on your computer. 
2. Extract the downloaded platform-tools zip file on your computer.
3. Connect your device to your computer using a USB cable.
4. Open a command prompt (Windows) or terminal (macOS and Linux) on your computer.
5. Navigate to the location where you extracted the platform-tools.
6. Enter the following command to check if your device is connected and detected by ADB:
```
adb devices
```
> [!Important]
> If your device is listed, proceed to the next step. If not, make sure your device is connected properly and that USB debugging is enabled in the developer options.
7. Now, reboot your device into Fastboot Mode using the following command:
```
adb reboot bootloader
```

### Step 3: Flash Recovery using Fastboot
1. Once your device is in Fastboot Mode, use the following command to check if Fastboot still detects your device:
```
fastboot devices
```
> [!Note] 
> If your device is listed, you are ready and If you don’t get any output or an error:
> * **On Windows:** Download [latest fastboot driver](https://xdaforums.com/t/official-tool-windows-adb-fastboot-and-drivers-15-seconds-adb-installer-v1-4-3.2588979/) and copy the folder into your desktop, then go again in Device Manager, locate your device, right-click on your device and choose "Update driver", choose "Browse my computer for driver software", then “Browse…” and select the folder you copied in your desktop. Click “ok” and then on “next”.
> * **on Linux or macOS:** If you see no permissions fastboot try running fastboot as root. When the output is empty, check your USB cable and port!

2. Download the  Recovery ZIP (`.img` file will be in zip) from the link provided in Step 1.
3. Place the downloaded  Recovery image (`.img` file) in the same location as the platform-tools folder on your computer.
4. Now, flash the  Recovery using the following command:
```
fastboot flash recovery recovery_file_name.img
```
> [!Important]
> Replace `recovery_file_name.img` with the actual name of the  Recovery image you downloaded if needed.
5. After flashing the recovery, use the following command to reboot your Recovery:
```
fastboot reboot recovery
```
6. Your device will reboot with Recovery installed.
> [!Note]
> If your recovery does not show the logo, then you have ccidentally booted into the wrong recovery. Please start at the top of this section!

### Step 5: Flash Project Elixir ROM

**Retrofit Dynamic Partitions** `(v4.0 and above versions)` - Clean Flash
```
- Download the latest build (Need to clean flash if you are on 4.2 or below)
- Take a backup for safe side (If you are coming from 4.2 or below you need to do a clean flash)
- Flash provided recovery Retrofit Supported Recovery
- Boot to Retrofit Supported Recovery
- Wipe dalvik-cache-sytem-vendor-data (wipe only dalvik-cache-data if coming from other dynamic roms)
- Flash legacy to retrofit dynamic by @raphael_alpha.zip (skip if coming from other dynamic roms)
- Flash latest a11 firmware (If coming from miui or a10 fw based rom)
- Flash Elixir rom
- Flash DFE NEO (if you want to be decrypted or already decrypted)
- Format Data (if your data on ext4 then change it to f2fs instead of format data)
- Reboot to system
- Enjoy
```

**Retrofit Dynamic Partitions** `(v4.0 and above versions)` - Dirty Flash
```
- Boot to Retrofit Supported Recovery
- Wipe only Dalvik/cache
- Flash or sideload the ROM zip
﻿﻿- Note if you want to decryption or already decrypted then only flash DFE NEO
- Reboot System
```
> [!Warning]
> **NOTE: We have Switched Retrofit Dynamic Partitions from v4.0 or above**


**Legacy ROM** `(v3.13 or below versions)` - **Clean Flash**
```
1. Copy the Project Elixir ROM (v3.13 or below) file to Internal storage or use OTG
2. Boot In the recovery that supports Legacy ROM Android 13
3. Wipe dalvik-cache-system-vendor-data
4. Flash latest a11 firmware (If coming from miui or a10 fw based rom)
5. Go to Install and Navigate to the location where you have kept the Project Elixir ROM.
6. Select the ROM file and swipe the slider to confirm the installation.
7. If you want decryption then only Flash DFE (optional)
8. After insatlling successfully reboot to system.
```

**Legacy ROM** `(v3.13 or below versions)` - **Dirty Flash**

Encryption to Encryption :
```
1. Download the Latest Build
2. Boot to Android 13 recovery that support encryption
3. Flash ROM zip
4. Clear Dalvik and Cache in advance wipe
5. Reboot
```

Decryption to Decryption `(Android 13 to Android 13)`
```
1. Download the Latest Build
2. Boot to Android 13 recovery that support decryption
3. Clear Dalvik and Cache in advance wipe
3. Flash ROM zip
4. Flash DFE (Compulsory)
5. Reboot
```

> [!Important]
> **May Required Files:**
> * Retrofit Supported Recovery : 1.[OrangeFox Recovery](https://t.me/Al_Arabis_Cloud/301) 2.[TWRP Recovery](https://t.me/Al_Arabis_Cloud/312)
> * Android 13 Legacy Recovery (For encrypted user's): [Tap here for link](https://t.me/Al_Arabis_Cloud/104)
> * Android 13 Legacy Recovery (For decrypted user's): [Tap here for link](https://t.me/Al_Arabis_Cloud/107)
> * Legacy2Retrofit.zip : [Tap Here for link](https://t.me/Al_Arabis_Cloud/108)
> * A11 Firmware.zip : [Tap Here for link](https://t.me/ElixerRaphael/7390)
> * DFE.zip (for a13) : [Tap Here for link](https://t.me/Al_Arabis_Cloud/299)
> * DFE NEO.zip (for a14) : [Tap Here for link](https://t.me/Al_Arabis_Cloud/298)


> [!Note]
> **Notes Specific to Raphael Build**
> * ROM uses Retrofit Dynamic Partitions, EROFS system, and FBEv2 (casefolding) encryption.
> * Gapps included – no need to flash separately.
> * First boot may take up to 15 minutes.
> * If switching from PORTs, format data & flash latest firmware.
> * Moving from A12/A13/A14 to A15? Clean flash is required.

<br>

> [!Tip]
> **Donate**: [Do consider donating or buying us a coffee](https://projectelixiros.com/donate)

<p align="center">
  <img src="https://i.imgur.com/bETSPlo.png" />
</p>
