# 🛡️ CloakDrain – A Stealth Battery Saver (Magisk Module)

**Version:** 2.6  
**Author:** J  
**Support:** None – this is an “as-is” tool. Use at your own risk.  
**Requires:** Magisk + Root + Android 10+  
**Tested on:** Pixel 6a running LineageOS

---

## 💡 What is CloakDrain?

CloakDrain is a lightweight, script-only Magisk module that enables a stealthy, aggressive battery saving mode — especially when the screen is off.  
It requires no user interface, no apps, and no background services.  
Control everything via simple terminal commands.

---

## 🔧 Features

When running `cloakdrain on`, the module will:

- 🧊 Set CPU governor to `powersave`
- 🔻 Lower maximum CPU frequency (applied twice to enforce)
- 📍 Disable location services (`location_mode 0`)
- 🛰️ Turn off sensors (`sensors_off 1`)
- 🎙️ Block microphone and camera access via AppOps
- 🚫 Disable known bloatware apps (TikTok, Facebook) if installed
- 📡 Enable Wi-Fi scan throttling
- ⏱️ Slow down wake-up timers (`alarm_manager_constants`)
- 📉 Disable background data usage
- 🧾 Log activity to: `/data/adb/cloakdrain_log.txt`

When running `cloakdrain off`, the module:

- Restores CPU governor to `schedutil`
- Re-enables sensors and location
- Reverts background and alarm settings
- Re-enables previously disabled apps (if any)

---

## 🧪 Usage

In a root shell (`adb shell` or Termux):

```bash
su
cloakdrain on      # Enable stealth mode
cloakdrain off     # Restore normal mode
cloakdrain status  # Check current status
📂 Installation
Flash the ZIP via Magisk

Reboot

Use the terminal to toggle on/off

(Optional) Automate with screen-off triggers via screen_monitor.sh (included in module)

🚫 Disclaimer
This module is provided “as-is”. No support, no updates, no guarantees.
If it breaks your device, sets your phone on fire, or ruins your coffee... that’s on you.

✅ Ideal for:
Power users and privacy nerds

Minimalist / Google-free setups

Digital detoxing or “offline-first” use

Anyone annoyed by excessive wake locks and background drain
