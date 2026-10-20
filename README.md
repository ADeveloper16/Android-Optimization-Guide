# Android-Optimization-Guide

<div align="center">

![Android Optimization Guide](https://capsule-render.vercel.app/api?type=waving&color=0:00F2FE,100:4FACFE&height=220&section=header&text=Android%20Optimization%20Guide&fontSize=38&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Ultimate%20ADB%20%7C%20Debloating%20%7C%20Kernel%20%7C%20Performance%20Tuning&descAlignY=62&descAlign=50)

[![GitHub Stars](https://img.shields.io/github/stars/ADeveloper16/Android-Optimization-Guide?style=for-the-badge&color=00F2FE&logo=github)](https://github.com/ADeveloper16/Android-Optimization-Guide/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/ADeveloper16/Android-Optimization-Guide?style=for-the-badge&color=4FACFE&logo=github)](https://github.com/ADeveloper16/Android-Optimization-Guide/network/members)
[![Android](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://github.com/ADeveloper16/Android-Optimization-Guide)
[![License](https://img.shields.io/github/license/ADeveloper16/Android-Optimization-Guide?style=for-the-badge&color=ff758c)](https://github.com/ADeveloper16/Android-Optimization-Guide/blob/main/LICENSE)

</div>


This repository contains Android optimization tips, performance tweaks, debloating recommendations, and lightweight app alternatives.

## 📋 Table of contents
1. [Enable Developer options on Samsung & Xiaomi Devices](#enable-developer-options-on-samsung-&-xiaomi-devices)
2. [Performance tweaks](#performance-tweaks)
3. [Debloat list](#debloat-list)
4. [On Linux debloat tutorial](#linux-os-tutorial-adb)
4. [Recommended apps to use](#recommended-apps-to-use)
6. [Credits](#credits-&-app-developers)
7. [Development](#development)

---

## Enable Developer options on Samsung & Xiaomi devices

Before starting let's enable Android Developer options.

### 📱 On Samsung

 ⚙️ Before we begin you'll need to enable Developer options.

1. Open **Settings**.

2. Press on **About phone**.

3. Tap on **Software information**.

4. Tap **Build number** 7 times continuous.

5. If prompted, please enter your **Password** to unlock Developer options.

6. A message will appear confirming that Developer options have been enabled.

7. Return to the main  **Settings** menu.

8. Scroll all the way **Down**

9. Tap on **Developer options**.

### 📱 On Xiaomi

⚙️ Now Lets do it on Xiaomi devices

1. Open **Settings**

2. Press on **My Device**

3. Tap on **Detailed info and specs**

4. From there you shall see **Build number**

5. Tap **Build number** 7 times continuous

6. A Message will appear near Navigation bar that confirming the Dev Options Have been **Enabled**

7. Go back to main Settings menu Scroll all the way down. until you see an option saying **Additional settings** press on it 

8. Scroll down again until you see Developer Options in Additional settings

---

## Performance tweaks
---

### Logger buffer sizes

Let's start by changing the **Logger buffer sizes**.

⚠ **WARNING**: Changing developer options may affect your device's behavior. Proceed only if you're comfortable making these changes.

**Watch the video below for a tutorial**.

[![Watch the video below to find this option:](https://img.youtube.com/vi/sFqN02OOgU4/0.jpg)](https://www.youtube.com/shorts/sFqN02OOgU4)

Once you've finished, log recording will be disabled. On some devices, this may reduce background logging, although any performance impact can vary.
---
### System tracing

**Watch the video below for a tutorial**.

[![Watch the video below to find this option:](https://img.youtube.com/vi/zEo_5j1Mnyw/0.jpg)](https://youtube.com/shorts/zEo_5j1Mnyw)
---
### Suspend Execution for Cached Apps

Let's enable **Suspend Execution for Cached Apps** After enabling this option, device may need to restart. to apply the change.

This setting allows Android to pause cached apps when they are not being used. The effect on performance can vary depending on your device and usage.

**Watch the video below for a tutorial**.

[![Watch the video below to find this option:](https://img.youtube.com/vi/O2BOmCmVk64/0.jpg)](https://youtube.com/shorts/O2BOmCmVk64)
---
### Shizuku Setup

Now that were finished here, we'll continue with Shizuku. Shizuku allows you to debloat system apps without rooting your device. You can download it from [Shizuku](https://github.com/RikkaApps/Shizuku/releases/tag/v13.6.0) <img src="logos/logo%20shizuku.png" width="18" height="18" valign="middle">. It requires ADB setup on your computer but it's worth it for advanced debloating **Find Tutorial On YouTube For Detailed Steps**.

---

## Debloat list
| Category | Apps |
| :--- | :--- |
| **Samsung Bloat** | Bixby, Voice Wake Up, Bixby Vision, Bixby Vision Framework, Customisation Service, Galaxy Avatar, Samsung News, Smart Switch, Crocro And Friends, Personal data intelligence, Recommended apps, Samsung Visit In, SmartThings Companion, Samsung Kids Installer |
| **Google/Meta** | Chrome, Gmail, Maps, Meet, Meta App Installer, Meta App Manager, Meta Services, Messages, Google Location History, System Parental Controls, Google Play Services For AR, Android System Intelligence, Live Transcribe & Sound Notifications |
| **Microsoft** | Microsoft Swiftkey Factory Settings, Microsoft Swiftkey, OneDrive |
| **System/Other** | Link To Windows, Speech Synthesis, WiFi Tips |

To debloat apps i suggest you [Canta](https://github.com/samolego/Canta/releases/tag/v3.2.2) <img src="logos/Canta.png" width="18" height="18" valign="middle">.


If you have computer you can try ADB step by step **Linux OS**

### Linux OS Tutorial Adb

1.Firstly lets download android platform tools from your terminal copy this text paste it on terminal
```bash
sudo apt install adb
```
2.Connect your device to laptop or PC and type this exactly in your terminal
```bash
adb devices
```
3.If it doesnt show up make sure you enabled USB Debugging on developer options

If it shows up your phone ID type this command 
```bash
adb shell pm disable-user --user 0 *package.name.here*
```
4.If you dont know what is the package name type
```bash
adb shell pm list | grep "*example: bixby,samsung,google,meta,facebook,windows*"
```

After reviewing the list, you can remove any apps you don't use.

⚠ Only remove apps you don't use. Some apps may be required for certain features.

After debloating unused apps, consider replacing them with lightweight open-source alternatives.

---

## Recommended apps to use

1. * **[Sterna Mail](https://f-droid.org/packages/app.sterna)** <img src="logos/iconSM.png" width="18" height="18" valign="middle"> - A lightweight email app designed with a no bloat. It uses Material Design You (MDY) and focuses on low usage. while it can be a bit hard to setting it up
2. * **[Easy Notes](https://f-droid.org/packages/com.kin.easynotes)** <img src="logos/iconEN.png" width="18" height="18" valign="middle"> - A Simple lightweight notes app no bloat and easy to use, with Material Design You.
3. * **[Translator](https://f-droid.org/packages/dev.davidv.translator)** <img src="logos/offtranslator%20logo-modified.png" width="18" height="18" valign="middle"> - An offline translator app that works without an internet connection. Useful for translating text when network access is unavailable
4. * **[Cromite](https://github.com/uazo/cromite/releases/tag/v153.0.8010.37-11507ac1061b5ea227806f5e84db5a57df6ccf6a)** <img src="logos/cromite%20logo-modified.png" width="18" height="18" valign="middle"> - A privacy-focused browser based on chromium. It includes built-in ad blocking, privacy improvements, and a clean browsing experience while keeping compatibility with modern websites.
5. * **[Booming Music](https://f-droid.org/packages/com.mardous.booming)** <img src="logos/iconBM.png" width="18" height="18" valign="middle"> - A Music player that has really useful features while keeping size ideal.
6. * **[PassVault](https://f-droid.org/packages/com.jksalcedo.passvault)** <img src="logos/iconPV.png" width="18" height="18" valign="middle"> - Ever bored about normal autofill's like Google Autofill Service and Samsung Pass? well this app brings better Password management on Browser's and supports JSON, CSV, KDBX.
---
## Credits - App Developers
Special thanks to the developers who created these apps. All credit goes to their respective creators.
---
## Development
I Will cannot make video tutorials for Xiaomi yet. (i dont have a Xiaomi device XD).