# Digistump / ATtiny85 Board Manager Backup

This repository serves as a permanent, self-hosted backup of the Digistump Arduino Board Manager configuration for ATtiny85 and related boards. 

### Why does this exist?
The original Digistump infrastructure and associated file servers (like `arduino.esp8266.com`) have been suffering from link rot. Many of the original URLs pointing to compiler toolchains and core files now return 404 errors, making it impossible to install the Digistump boards via the Arduino IDE's native board manager.

This repository fixes that by hosting all 45 required archive files locally as GitHub Release Assets and providing a patched `package_digistump_index.json` that points to these surviving files.

### How to Use

To install the Digistump boards in your Arduino IDE using this backup:

1. Open the Arduino IDE.
2. Go to **File** > **Preferences**.
3. In the "Additional Boards Manager URLs" field, paste the following Raw JSON link:
   https://raw.githubusercontent.com/appdevmon/attiny85-board-backup/main/package_digistump_index.json
4. Click **OK**.
5. Go to **Tools** > **Board** > **Boards Manager...**
6. Search for `Digistump` and click **Install**.

### What is included?
* A patched `package_digistump_index.json`.
* All required `.zip`, `.tar.gz`, and `.tar.bz2` dependencies hosted safely under the Releases tab.
