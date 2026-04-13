# 🎣 Bridger: Western Fishing Bot | v3.0+

A high-performance automation utility designed for fishing in **Bridger Western**. This bot utilizes **Real-Time Audio Frequency Analysis** and **OCR (Optical Character Recognition)** to provide a near-perfect fishing experience.

> **Note:** Version (v3.0 Onwards) has transitioned to **Audio-Based Detection**. It listens for the specific frequency of the "Splash" sound, making it significantly more reliable than old visual-based macros.  
> If you need support, join the Discord Server and create a ticket - https://discord.gg/euQnmmAnDj

---

## 🚀 Getting Started

* **Download:** Grab the latest `FishingBot.exe` from the **Releases** tab.
* **One-Time Setup:** On your first launch, a **Requirements Wizard** will appear. You **MUST** install the **Tesseract OCR** and **Visual C++ Redistributable** using the clickable links provided to prevent the bot from crashing.
* **Permissions:** Double-click the `.exe` to start. If the script does not function correctly, right-click and select **Run as Administrator**.
* **Monitor Selection:** On first launch, the dropdown will say **"Please Select the Game Window Monitor."** Select the monitor where Roblox is running to ensure the bot captures the correct screen coordinates. 
* **Tesseract Link:** Click **Browse**, navigate to where you installed Tesseract (usually `C:\Program Files\Tesseract-OCR\tesseract.exe`), and click **Save**. The bot now links the engine instantly without needing a restart!
* **Calibrate (F3):** Once in-game, fish until the minigame appears. Press **F3** and drag the red box over the minigame area.

### Player Positioning
1. **Safety First:** Position yourself in a corner with walls on your left, right, and back to prevent being launched by chests.
2. **View:** Enter **First Person** and face towards eye level. 
3. **Audio:** Ensure your **Roblox volume is maxed** out. The bot listens for the splash; it does not need to "see" the bobber anymore!

---

## 🧪 Advanced Audio Calibration (Stop "Ghost Bites")

If the bot is reeling in the rain without a fish (Ghost Bites), you need to calibrate your settings using the live data from your terminal.

### 1. Identify the Noise
When a ghost bite happens, look at the bottom of the bot's terminal for a line that looks like this:
`[BITE] Splash! Peak: 0.2708 | Baseline: 0.1221 | Ratio: 2.2x`

### 2. Adjust Your Settings
To stop the rain from triggering a reel, you must set your "Goalposts" just above the numbers produced by the rain:
* **Min Volume Threshold**: Look at the `Peak` number. If the rain hit **0.2708**, set your **Min Volume** to **0.28** to block it.
* **Spike Sensitivity (Ratio)**: Look at the `Ratio` number. If the rain hit **2.2x**, set your **Spike Sensitivity** to **2.3** or **2.4**.

> **Note:** You must toggle the Advanced Settings Option at the top of the script to unlock these settings that appear at the bottom of the script.  
> **Pro Tip:** If you continue to get ghost bites, simply check the terminal again for the *new* highest peak and ratio the rain is producing and adjust slightly higher.

---

## ⚙️ Understanding the Settings

### Chest & Movement
* **Chest Movement:** (None | Left | Right) If you get ragdolled by a chest, this setting moves you back into position.
* **Side Walk (s):** How many seconds the script holds the movement key after a catch.

### Delays & Audio
* **Bait/Rod Delay (s):** How long you want the script to wait before clicking the items in your hotbar. (Optimized to **0.1s** in v3.1 for lightning-fast equipping.)
* **Reel Timeout (s):** How long to wait for a bite before re-casting. After 5 timeouts, the **Emergency Failsafe** will Alt+F4 your game.
* **Reel Click Delay (s):** How long the script should wait to reel in the fishing rod after a spike is detected. (Optimized to 0.0 after v3.0, this shouldn't be touched at all)

---

## ⌨️ Hotkeys

### In-Game Hotkeys
* **Rod/Bait Keys:** The hotbar numbers (1-9) for your equipment.

### Script Hotkeys
* **Start (F1):** Begins the fishing loop.
* **Stop (F2):** Safely stops the bot after the current cast.
* **Calibrate (F3):** Opens the screen region selector.
* **Overlay (F4):** Toggles the mini-stats box. Double-click this box to re-open the main menu.

---

## 🖥️ Extra Features

* **Sticky Menu:** Forces the GUI to stay on top of the Roblox window.
* **ToolTips:** Hover over any setting to see a detailed description of what it does.
* **Hide/Show Categories:** Collapse sections of the GUI to save screen space.
* **Black Box Terminal:** If the bot stops, the terminal will print a **[CRASH REPORT]** with exact details.
* **Auto-Migration:** v3.1+ automatically detects old v2.5 settings and updates your delays to the new 0.1s standard.
* **Send Feedback:** Send bug reports directly to the developer (Max 350 characters).

---

## ⚠️ Important Information

* **Save Buttons:** When a value is changed, the **Save** button turns **Red**. You **MUST** click it until it turns **Green** to apply changes.
* **Account Risk:** This macro is **BANNABLE**. You accept all risks by using it.
* **Auto-Updater:** The bot automatically checks GitHub for new updates!
