# Token & Browser Protector 🛡️

An all-in-one security tool that proactively protects you from Discord token grabbers, malicious scripts, and clipboard hijackers.

## 📥 Download

**[📥 Click here to Download the latest version](https://github.com/sn9x0/AntiDiscordTokenGrabber/releases/download/AntiGrabber/TokenProtector.exe)**
*(Note: Replace the link above with your actual download link)*

---

## ✨ Features

### 1. Discord Core & Sandbox Protection
Modern token grabbers and malware directly attack Discord to steal passwords and tokens. This tool blocks these attacks on two levels:
- **`app.asar` Sandboxing:** Creates an isolated "vault" folder for the Discord session. A virus will no longer find a token in the usual `AppData` location.
- **`discord_desktop_core` Auto-Heal:** On every startup, the tool checks the notorious `index.js` file, which is targeted by almost all token grabbers. If malicious code is found, it deletes it, restores the file to its original state ("heals" it), and subsequently locks it as Read-Only via the Windows file system.
- **Supported Clients:** Discord Stable, PTB, Canary, Development, Lightcord, ArmCord, Vesktop.

### 2. Anti-Clipboard-Hijacker (Clipper Protection)
Clipboard hijackers run invisibly in the background and wait for you to copy a cryptocurrency address (e.g., for a transaction). In milliseconds, they swap your copied address with the hacker's address.
- Our tool runs completely invisibly in the background (when enabled in settings).
- It scans the clipboard in real-time for BTC, ETH, LTC, XMR, TRX, and SOL addresses.
- If an address is swapped for a *different* crypto address in under 1.5 seconds, the tool **blocks the virus**, instantly restores your original address, and warns you with a native Windows popup!

### 3. Auto-Start (Persistence)
- You can configure the tool to seamlessly integrate into the Windows startup (Registry).
- It starts in the background (without a visible window), lightning-fast checks Discord for new infections, heals them if necessary, and activates the Anti-Clipboard-Hijacker.

## 🚀 Installation & Usage

The tool has been compiled as a standalone `.exe`, so you don't need to install Python or any other dependencies.

1. **Download** the `TokenProtector.exe` from the link above.
2. Run the file **`TokenProtector.exe`**.
3. **In the Dashboard:**
   - **"Discord Protect" Tab:** Shows you whether your Discord is infected or protected. Click on "Protect" to arm the protection.
   - **"Browser Protect" Tab:** *(Currently under construction)* The direct file lock for Chrome/Edge cookies will be implemented here soon.
   - **"Clipboard Protect" Tab:** Check the box for "Enable Anti-Clipboard-Hijacker" so the tool watches out for viruses in the background.
4. Check the box at the very bottom for **"Enable Auto-Protection on PC Restart"** so you don't have to think about the tool after rebooting your PC.

## ⚠️ Warning
This tool modifies core files of Discord to lock them away from hackers. When there is an official Discord update, Discord might occasionally fail to update. In this case, simply open the tool, click on **"Unprotect"**, let Discord update normally, and then click on **"Protect"** again.
