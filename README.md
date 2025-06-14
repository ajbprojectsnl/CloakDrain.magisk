🛡️ CloakDrain – Magisk Module
Version: 2.6
Author: J
Support: None – this is an “as-is” tool
Requires: Magisk + Root + Android 10+
Tested on: Pixel 6a with LineageOS

💡 What is CloakDrain?
CloakDrain is a lightweight, fully script-based Magisk module designed to aggressively reduce background activity and battery drain — especially while the screen is off.
No apps, no UI, no frills — just clean control via the terminal.

⚙️ What does it do?
When you run cloakdrain on, it activates a “stealth power-saving mode” by:

🔋 Setting the CPU governor to powersave

🧊 Reducing maximum CPU frequency (reinforced twice for persistence)

📍 Disabling location services (location_mode 0)

🛰️ Turning off all sensors (sensors_off 1)

🎙️ Blocking microphone and camera access via AppOps

🚫 Disabling common bloatware apps (e.g., TikTok, Facebook – only if installed)

📡 Enabling Wi-Fi scan throttling

⏱️ Slowing down wake-up timers with alarm_manager_constants

📉 Disabling background data

🧾 Logging every action to: /data/adb/cloakdrain_log.txt

🔁 When you run cloakdrain off, it restores:
CPU governor to schedutil

Sensors and location services back on

Background data and alarms to default

Re-enables previously disabled apps

🧪 Usage
In terminal (via adb shell or Termux):

bash
Copy
Edit
su
cloakdrain on     # Enable stealth battery saving
cloakdrain off    # Restore normal behavior
cloakdrain status # Check if CloakDrain is active
📝 Notes
Works silently in the background

Can be combined with auto-toggle scripts (e.g., screen-off triggers)

“As-is” release – no support, no hand-holding, just works

🔥 Ideal for:
Privacy-focused users

Low-power / offline setups

Phones that heat up unnecessarily

Anyone who wants to tame background processes

