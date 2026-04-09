# 🎣 Bridger Western Fishing Bot

A macro designed specifically for fishing in **Bridger Western**. This bot uses local brightness spike detection and template matching to provide a reliable fishing experience.

**Note:** This script uses on-screen detection rather than audio cues to detect whether the fish has or hasn't hooked onto the fishing rod. It may occasionally provide false positives when detecting visual changes in the environment.

---

## 🚀 Getting Started

* **Download:** Grab the latest `FishingBot.exe` from the Releases tab. (**Note:** Ensure you download `FishingBot.exe`, `Tesseract.exe`, and the `Letter.png` files. For ease of use, place them all in the same folder. Do **NOT** download the **Source Code**, as it will not run.)
   
* **Permissions:** Double-click the `.exe` to start. If the script does not function correctly, right-click the `.exe` and select **Run as Administrator**.

* **Setup:** Select the **Main Monitor** that will have the **Roblox Game Window** open. (**Note:** Even if the correct monitor appears selected on startup, click the dropdown and re-select it to ensure the script properly reads your **Display Width and Height**.)
  
* **Tesseract:** This `.exe` requires `Tesseract.exe` to be installed (preferably in the same folder as your bot). Link the path by clicking the **Browse** button, selecting the file, and clicking **Open**.

* **Calibrate:** Once in-game, manually fish until the minigame appears. Quickly press **F3** to open the calibration overlay and drag the red box over the minigame area. (**Note:** If the script fishes normally but fails the minigame, re-calibrate the red box until it completes it successfully.)

* **Player Positioning:**  
  #1. Position yourself in a corner where there are walls on your left, right, and back. Ensure you have a few feet of walking room so that if a chest spawns and ragdolls you, you aren't launched into the water or out of your original spot.    
  #2. Enter **First Person** and press **Ctrl** to disable the regular mouse and enable the shift-lock crosshair.    
  #3.  Ensure your crosshair is **SLIGHTLY** above the red bobber in the water so the script can detect it constantly.
 
 (**Note:** Depending on the spot you choose, Bandits and Zombies may be able to spawn. Find a spot where either NPCs cannot reach you, or they cannot spawn at all. Monitor your character on the first use the script to make sure whether or not your spot is suitable for fishing.)

---

## ⚙️ Understanding the Settings

### **Delays & Settings**
* **Bait Delay (s):** How long the bot waits after pressing the bait hotkey before switching to the rod.
* **Rod Delay (s):** The pause after equipping the rod before attempting to cast.
* **Bobber Radius:** The size of the search box around the red bobber. Increase this **ONLY** if the script isn't seeing the fish trail in time or if the server has **high ping/lag**.  
  (**Note:** If the number is too low, the script won't see the trail in time to reel; if it is too high, it may reel too early before the fish actually hooks.)

---

### **Weather Thresholds**
*These values determine the "spike" in brightness needed to trigger a reel.*

* **Day Clear:** The primary threshold for sunny weather. High values (e.g., 2000) help ignore sun reflections.
* **Day Rain:** Adjust this if the bot is "false-reeling" due to rain streaks.
* **Night Clear:** Lower values are used because the fish trail is harder to see against dark water at night.
* **Night Rain:** Specifically tuned to handle the visual noise of nighttime rain.

---

### **Environment Sensitivity**
* **Night Brightness:** The lighting level where the bot switches from "Day" to "Night" thresholds.
* **Rain Saturation:** Determines how "gray" the screen must be to activate "Rain" thresholds.
  
 (**Note:** Depending on your spot, if your view is heavily obstructed by walls or roofs, the script may struggle to tell if it is Day or Night. However, the daytime thresholds will usually still work in these cases so no need to worry, but if they don’t, then you can manually change the thresholds yourself.)
    
 (**Second Note:** Rain detection is unfortunately janky and may not work 100% of the time. This should not significantly affect catch rates, but it may affect the final session stats.)

---

## ⌨️ Hotkeys
### **In-Game Hotkeys**
* **Rod Key:** The hotbar number associated with your Fishing Rod.
* **Bait Key:** The hotbar number associated with your Bait.

### **Script Hotkeys**
* **Start (F1):** Begins the fishing loop.
* **Stop (F2):** Safely stops the bot after the current cast.
* **Calibrate (F3):** Opens the screen region selector.

---

## ⚠️ Important Information (TOS)
* **Save Buttons:** When a value is changed, the **Save** button turns **Red**. You MUST click it until it turns **Green** to apply the change.
* **Account Risk:** This macro is **BANNABLE**. You accept all risks by using it.
* **Auto-Updater:** The bot automatically checks GitHub for new updates on launch!
