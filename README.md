### 🌐 Language / Dil: &nbsp; 🇬🇧 [English](README.md) &nbsp; | &nbsp; 🇹🇷 [Turkish](README.tr.md)

---

# 🛠️ Digistump / ATtiny85 Board Manager Backup

This repository serves as a permanent, self-hosted backup of the Digistump Arduino Board Manager configuration for ATtiny85 and related developer hardware. 

### ❓ Why does this exist?
The original Digistump infrastructure and associated downstream file servers (such as `arduino.esp8266.com`) have fallen victim to severe **link rot**. Many of the original hardcoded URLs pointing to compiler toolchains, device binaries, and core definitions now return `404 Not Found` errors. This breaks the installation chain inside the Arduino IDE's native board manager.

This archive completely resolves the issue by hosting all **45 required core archives** locally as secure GitHub Release Assets, paired with a patched, self-referencing `package_digistump_index.json`.

---

### 🚀 How to Use

#### 🔌 1. Driver Installation (Windows Only)
If you are running Windows, your operating system requires low-level USB filters to communicate with the ATtiny85 micronucleus bootloader during compilation and flash routines:

1. Head over to the **Releases** tab of this repository.
2. Download [📦 Digistump.Drivers.zip](https://github.com/appdevmon/attiny85-board-backup/releases/download/v1.0/Digistump.Drivers.zip).
3. Extract the contents completely and execute `Install Drivers.exe` (or your corresponding installer application) to register the device handles.

#### ⚙️ 2. Arduino IDE Environment Setup
To point your native environment directly to this reliable mirror fallback:

1. Fire up your **Arduino IDE**.
2. Navigate to **File** ➡️ **Preferences**.
3. Locate the **Additional Boards Manager URLs** input field and paste the following raw manifest link:
   ```text
   https://raw.githubusercontent.com/appdevmon/attiny85-board-backup/main/package_digistump_index.json](https://raw.githubusercontent.com/appdevmon/attiny85-board-backup/main/package_digistump_index.json
