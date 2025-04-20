# slya-electron
Standalone version of SLY Assistant (for Electron)

Works with: Windows, Linux, MacOS, ARM64, ...

**Important**: The standalone version doesn't use a wallet extension. Instead SLYA signs the transactions by itself - so it needs your wallet key. For security reasons you should do this only with a lancer wallet!

## Instructions:
1) Go to https://github.com/electron/electron/releases/tag/v35.1.0 and download the "electron-v35.1.0-[...]" version for your OS/CPU and unpack it.\
Or use a direct link from this list:
 - Windows (Intel/AMD): https://github.com/electron/electron/releases/download/v35.1.0/electron-v35.1.0-win32-x64.zip
 - Windows (ARM): https://github.com/electron/electron/releases/download/v35.1.0/electron-v35.1.0-win32-arm64.zip
 - Linux (Intel/AMD): https://github.com/electron/electron/releases/download/v35.1.0/electron-v35.1.0-linux-x64.zip
 - Linux (ARM, e.g. Raspberry Pi 5): https://github.com/electron/electron/releases/download/v35.1.0/electron-v35.1.0-linux-arm64.zip
 - MacOS: https://github.com/electron/electron/releases/download/v35.1.0/electron-v35.1.0-darwin-arm64.zip
2) Download slya-electron.zip from this repository and unpack the ZIP in the electron program folder - or alternatively unpack it somewhere else and copy all files into the Electron folder.\
Direct link to the latest version : https://github.com/Swift42/slya-electron/raw/refs/heads/main/slya-electron.zip
3) Start the app with "SLYA.sh" (on Linux) or "SLYA.bat" (on Windows). It may be useful to create a shortcut/launcher for it. Alternatively you can start the electron app with the parameter ".", so e.g. "electron.exe ." on Windows or "./electron ." on Linux.
4) When the standalone app has started, it will automatically download the latest SLYA version and tells you that the wallet key is missing. Follow the instructions to add the key.

The SLYA standalone version comes with three additional buttons:

Reload: The app gets reloaded

Update: Check for an update and optionally install it

Console: Open the error console

SLYA's data is saved into the "data" subfolder, so if you want to run multiple instances, just duplicate the full electron folder and start the second instance from the duplicated folder (this way each instance has its own data folder).

## Troubleshooting:
Linux: if you get an error about a "sandbox helper binary", either make sure the file "chrome-sandbox" is owned by root or alternatively start electron with "electron --no-sandbox ." 
