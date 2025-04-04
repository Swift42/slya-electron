# slya-electron
Standalone version of SLY Assistant (for Electron)

Works with: Windows, Linux, MacOS, ARM64, ...

**Important**: The standalone version doesn't use a wallet extension. Instead SLYA signs the transactions by itself - so it needs your wallet key. For security reasons you should do this only with a lancer wallet!

## Instructions:
1) Go to https://github.com/electron/electron/releases/tag/v35.1.0
2) Download the "electron-v35.1.0-[...]" version for your OS/CPU (e.g. "linux-arm64" is for the Raspberry Pi 5) and unpack it
3) Download slya-electron.zip from here and unpack the ZIP in the electron program folder
4) Start the app with "SLYA.sh" (on Linux) or "SLYA.bat" (on Windows). It may be useful to create a shortcut/launcher for it. Alternatively you can start the electron app with the parameter ".", so e.g. "electron.exe ." on Windows or "./electron ." on Linux.
5) When SLYA has started, you will see the error message "phantom is not defined" in the console. This is because you need to set your wallet key in the SLYA settings (Tools -> Settings -> Advanced). After you set the key, use the reload button. Done.

The SLYA standalone version comes with three additional buttons:

Reload: The app gets reloaded

Update: Check for an update and optionally install it

Console: Open the error console

SLYA's data is saved into the "data" subfolder, so if you want to run multiple instances, just duplicate the full electron folder and start the second instance from the duplicated folder (this way each instance has its own data folder).

## Troubleshooting:
Linux: if you get an error about a "sandbox helper binary", either make sure the file "chrome-sandbox" is owned by root or alternatively start electron with "electron --no-sandbox ." 
