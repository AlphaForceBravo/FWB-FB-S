# 🎣 Bridger: Western Fishing Bot | v3.2.9

A high-performance automation utility designed for fishing in **Bridger Western**. This bot utilizes **Real-Time FFT Audio Frequency Analysis**, **Lightning-Fast OpenCV Template Matching**, and a **Customizable Macro System** to provide a near-perfect, hands-free fishing experience.

> **Note:** Version 3.2.9 is a critical hotfix update that makes the Minigame QTE bulletproof across all monitor sizes and resolves a stubborn UI loop bug for the `Live Debug Viewer`.  
> If you need support, join the Discord Server and create a ticket: https://discord.gg/euQnmmAnDj

---

## 🚀 Getting Started

* **Download:** Grab the latest `FishingBot.exe` from the **Releases** tab. 
* **One-Time Setup:** On your first launch, a **Requirements Wizard** will appear. You **MUST** install the **Tesseract OCR** and **Visual C++ Redistributable** using the clickable links provided to prevent the bot from crashing.
* **Permissions:** Double-click the `.exe` to start. The bot automatically requests **Administrator** privileges to ensure keystrokes properly reach the Roblox client.
* **Monitor Selection:** Go to the **⚙ Bot Settings** tab and select the monitor where Roblox is running to ensure the bot captures the correct screen coordinates. 
* **Tesseract Link:** Click **Browse**, navigate to where you installed Tesseract (usually `C:\Program Files\Tesseract-OCR\tesseract.exe`), and click **Save**. 
* **Calibrate (F3):** Once in-game, fish until the minigame appears. Press **F3** and drag the red box over the minigame area, then press Enter to save the box coordinates. *(Note: The box dynamically scales to the exact monitor you selected in Settings).*

### Player Positioning & Setup
1. **The Corner Anchor:** Position yourself backed perfectly into a physical wall or corner. This is your "Anchor Point" which prevents the bot from drifting over time. *(Note: If you don't have walls nearby, you can set the Corner Direction to "None" in the settings).*
2. **View:** Enter **First Person** and face your character towards the water, aim your mouse towards the middle of your left arm to guarantee that the bot will hear the splash while in the rain.
3. **Audio Routing:** The bot uses FFT Frequency subtraction to ignore rain. 
   > **⚠️ Important Audio Setup:** Because the bot listens for the splash, loud background apps like Discord or YouTube can trigger false catches. To prevent this, you have two options:
   > 1. Keep your background media at a very low volume.
   > 2. Use a Virtual Audio Cable to completely separate Roblox's audio (recommended if you want to listen to loud music or calls). Go to the **🔊 Audio** tab and select the specific device to route Roblox into. This isolates the game audio entirely!

---

## 🖥️ The Dashboard & Tools

The bot features a sleek sidebar navigation system with several powerful tools to help you optimize your catches and prevent ghost bites.

### 🔊 Live Audio Visualizer
Found in the **Audio** tab. This opens a real-time visual meter showing exactly what the bot's FFT analyzer hears. 
* **Raw Bar:** Current total volume level.
* **Clean Bar:** The isolated "Splash" sound after the bot actively subtracts the live rain/ambient noise profile.
* **Red Line:** Your Clean Threshold. The splash must cross this line to trigger a catch!

### 👁️ Live Vision Debugger
Found on the **Dashboard**. This opens a live feed showing exactly what the bot sees.
* **Red Box:** Where the bot is looking for the "Spooked" text (Top 35% of the screen).
* **Green Box:** Where the bot is looking for the "Caught / Full" text.
* **Blue Box:** Your calibrated minigame letter zone. 

---

## ⟳ Movement & Positioning (The Anchor System)

Because Roblox chests ragdoll your character, the bot uses a customizable recovery system.

1. Go to the **⟳ Movement & Pos** tab.
2. Set your **Corner wall direction** (Left, Right, or None).
3. Press **F5** to record your **Ledge Path**, walking from your safe corner wall to the edge of the water.
4. Press **F6** to record your **Wander Path**, walking away from the water for your Anti-AFK Spooked sequence.
5. **Macro Editor:** Click the **✏️ Edit** button to manually fine-tune your recorded paths down to the exact millisecond!
6. **How it works:** When you catch a chest, the bot waits for you to stand up, physically rams you backward into your corner wall to reset your 3D coordinates, walks your Ledge Path back to the water, collects the chest, and continues fishing flawlessly!

---

## ⚙️ Understanding the Settings

### Delays, Audio, & Vision
* **Disable Bait Toggle:** If enabled, the bot skips pressing the bait key and automatically adds +5.0s to your fish timeout so you don't infinite loop.
* **Fish Timeout (s):** How long to wait for a bite before re-casting. Set to **15.0s** (or 20.0s without bait). 
* **Clean Threshold:** How loud the fish splash must be *above* the background rain to trigger.
* **Reel Click Delay (s):** Found in the Advanced tab. Manually fine-tune the delay between hearing the splash and clicking to reel the fish in.
* **Minigame Vision Mode:** Found in the Advanced tab. Highly recommended to leave this on **Template (Fastest: ~2ms)** for lightning-fast minigame reaction times.

### Failsafe System
If the bot times out 5 times in a row, it assumes you are stuck or disconnected. It will generate a `failsafe_report.json` file and Alt+F4 the game to protect your character. The next time you launch the bot, a popup will display your exact stats (Catches, Rares, and Stack Status). 

---

## ⌨️ Hotkeys

### Script Hotkeys (Customizable in the 'Keys' & 'Movement & Pos' tabs)
* **Start (F1):** Begins the fishing loop.
* **Stop (F2):** Safely stops the bot after the current cast.
* **Calibrate (F3):** Opens the screen region selector.
* **Overlay (F4):** Toggles the mini-stats box. 
* **Record Ledge Path (F5):** Starts/Stops recording your movement from the wall to the water.
* **Record Wander Path (F6):** Starts/Stops recording your Anti-AFK path away from the fishing spot.

---

## ⚠️ Important Information

* **Save Buttons:** When a value is changed, the **Save** button turns **Red**. You **MUST** click it until it turns **Green** to apply changes.
* **Account Risk:** This macro is **BANNABLE**. You accept all risks by using it.
