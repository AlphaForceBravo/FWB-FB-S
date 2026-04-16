# 🎣 Bridger: Western Fishing Bot | v3.0.0+

A high-performance automation utility designed for fishing in **Bridger Western**. This bot utilizes **Real-Time Audio Frequency Analysis**, **Advanced OCR (Optical Character Recognition)**, and a **Smart Anti-AFK Macro System** to provide a near-perfect, hands-free fishing experience.

> **Note:** Version 3.2.0 introduces a massive UI overhaul, moving away from the old black console window to a sleek, modern, all-in-one dashboard with built-in live debugging tools. 
> If you need support, join the Discord Server and create a ticket - https://discord.gg/euQnmmAnDj

---

## 🚀 Getting Started

* **Download:** Grab the latest `FishingBot.exe` from the **Releases** tab. 
* **One-Time Setup:** On your first launch, a **Requirements Wizard** will appear. You **MUST** install the **Tesseract OCR** and **Visual C++ Redistributable** using the clickable links provided to prevent the bot from crashing.
* **Permissions:** Double-click the `.exe` to start. If the script does not function correctly, right-click and select **Run as Administrator**.
* **Monitor Selection:** Go to the **⚙ Bot Settings** tab and select the monitor where Roblox is running to ensure the bot captures the correct screen coordinates. 
* **Tesseract Link:** Click **Browse**, navigate to where you installed Tesseract (usually `C:\Program Files\Tesseract-OCR\tesseract.exe`), and click **Save**. 
* **Calibrate (F3):** Once in-game, fish until the minigame appears. Press **F3** and drag the red box over the minigame area, then click enter to save the box coordinates.

### Player Positioning
1. **Safety First:** Position yourself in a corner with walls on your left, right, and back to prevent being launched by chests.
2. **View:** Enter **First Person** and face towards eye level. 
3. **Audio:** Ensure your **Roblox volume is maxed** out. The bot listens for the splash.

---

## 🖥️ The New Dashboard & Tools

The bot now features a sleek sidebar navigation system with several powerful new tools to help you optimize your catches and prevent ghost bites.

### 🔊 Live Audio Visualizer
Found in the **Audio** tab. This opens a real-time visual meter showing exactly what the bot hears. 
* **Green Bar:** Current volume level.
* **Red Line:** Your Minimum Volume Threshold (Noise Gate).
* **Yellow Dashed Line:** Your Spike Ratio threshold (The exact volume needed to trigger a catch).

### 👁️ Live Vision Debugger
Found on the **Dashboard**. This opens a live feed showing exactly what the bot sees.
* **Red Box:** Where the bot is looking for the "Spooked" text.
* **Green Box:** Where the bot is looking for the "Caught / Full" text.
* **Blue Box:** Your calibrated minigame letter zone. 

---

## ⟳ Smart Anti-AFK & Movement

The new anti-macro system added is no more after this update. Version 3.2.0 introduces a custom macro recording system.

1. Go to the **⟳ Anti-AFK** tab and click **Record New Path**.
2. Walk your character *away* from the water using W, A, S, D, and Space.
3. Stop recording.
4. When the bot detects the fish are "Spooked", it will play your recorded path, double-click to reset your cast radius, and **automatically reverse your exact keystrokes** to walk you back to your original fishing spot!

---

## ⚙️ Understanding the Settings

### Delays & Audio
* **Bait/Rod Delay (s):** Optimized to **0.1s** for lightning-fast equipping.
* **Fish Timeout (s):** How long to wait for a bite before re-casting. Set to **15.0s**. After 5 consecutive timeouts, the **Emergency Failsafe** will trigger.
* **Reel Click Delay (s):** Optimized to **0.0s**. Do not change this for maximum speed.

### Failsafe System
If the bot times out 5 times in a row, it assumes that you either got killed, rejoined the server due to dev shutdown, or got stuck in a spot in which it cannot cast the fishing rod into the water anymore. It will generate a `failsafe_report.json` file and Alt+F4 the game to protect your characters age. The next time you launch the bot, a popup will display your exact stats at the time of the emergency shutdown.  
> Note: A **"Disable Failsafe"** button can be found in the **"Advanced Settings"** panel if you'd like to disable the failsafe from initiating.

---

## ⌨️ Hotkeys

### In-Game Hotkeys
* **Rod/Bait Keys:** The hotbar numbers (0-9) for your equipment.

### Script Hotkeys (Customizable in the 'Keys' tab)
* **Start (F1):** Begins the fishing loop.
* **Stop (F2):** Safely stops the bot after the current cast.
* **Calibrate (F3):** Opens the screen region selector.
* **Overlay (F4):** Toggles the mini-stats box. Click the Overlay Hotkey again or Double-click the mini-box to re-open the main menu.

---

## ✨ Extra Features

* **Built-in Session Log:** The black console window is gone! All terminal outputs, debug info, and OCR text readings now print directly into the green terminal at the bottom of the app.
* **Seamless Auto-Updater:** The bot automatically checks GitHub for updates, downloads the new `.exe`, and safely restarts itself.
* **Auto-Migration:** The bot automatically detects old `settings.json` values and forces optimal delays (0.1s equip, 0.0s reel) upon launch.
* **Sticky Menu:** Pin the GUI or the mini-overlay to stay on top of the Roblox window.
* **In-App Feedback:** Send bug reports directly to the developer and it is located in the **Social** tab.

---

## ⚠️ Important Information

* **Save Buttons:** When a value is changed, the **Save** button turns **Red**. You **MUST** click it until it turns **Green** to apply changes.
* **Account Risk:** This macro is **BANNABLE**. You accept all risks by using it.
