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

### **Chest Movement** ###
* **Options: *None* | *Left* | *Right***: These options are for when the fishing minigame ends, if your spot requires you to move either to the left or right, then this is what that options is for, any input below 1.0 will tap the a or d button, anything above will hold the a or d button.
* **Side Walk (s):** How many seconds the script walks your character to the left or right. (Only really needed if your spot requires you to move to the left or right AFTER the chest minigame launches and ragdolls you)

### **Delays & Settings**
* **Bait Delay (s):** How long the bot waits after pressing the bait hotkey before switching to the rod.
* **Rod Delay (s):** The pause after equipping the rod before attempting to cast.
* **Bobber Radius:** The size of the search box around the red bobber. Increase this **ONLY** if the script isn't seeing the fish trail in time or if the server has **high ping/lag**.  
  (**Note:** If the number is too low, the script won't see the trail in time to reel; if it is too high, it may reel too early before the fish actually hooks.)
* **Reel Timeout (s):** How long the script is told to wait to see if it can catch a fish, if it can't get a large enough spike to trigger the threshold by the time the seconds are over, the script will count it as a timeout and re-cast the fishing rod. (5 timeouts in a row will initiate the failsafe which Alt F4's your game)
* **Reel Click Delay (s):** How long the script is told to wait AFTER the threshold is met before reeling in the fish. (Ex: if reel click delay is 0.0, the moment a spike passes a threshold, it will **INSTANTLY** reel. If it's set to 1.0, it'll wait a second after the threshold is met to click to reel in the fish. Setting is mainly for whether the script is reeling in too early or too late, or also in a high ping/laggy server) (Default should be either 0.9 or 0.8 or in-between, around their is usually good)

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
* **Overlay (F4):** Opens a small overlay box that is moveable and shows current fish status, successful catches compared to totals casts, and your total consecutive timeouts to initiate the failsafe, default is 0/5. (You can also double click the small overlay to re-open the larger GUI)

---

## ⌨️ Extra
### **More Buttons**
* **Sticky Menu: ON/OFF:** Sticky menu is whether the GUI is forced to stay as the top overlay. (So if it's enabled, even if you alt tab into the game, although the script is not tabbed in, it's still forced as the top overlay and stays on top of the game window.)
* **Hide/Show**: The hide shows buttons are for whether or not you wanna hide or show the categories settings. (If the large GUI is taking up a lot of screen, then click the hide buttons to decrease the height of the overlay.)
* **Hide terminal / Show Terminal:** Button shows or hides the GUI terminal at the bottom.
* **Send Feedback:** You can send feedback / bug reports to me via the button, just type your concerns in the box (Max of 350 characters) and click **"SEND TO DEVELOPER"**. (A message will pop up in the ui terminal saying whether or not it was successfully sent)

---

## ⚠️ Important Information
* **Save Buttons:** When a value is changed, the **Save** button turns **Red**. You MUST click it until it turns **Green** to apply the change.
* **Account Risk:** This macro is **BANNABLE**. You accept all risks by using it.
* **Feedback:** When sending feedback or bug reports via the send feedback button on the bottom of the GUI, the only info currently collected is your Software Version.
* **Auto-Updater:** The bot automatically checks GitHub for new updates on launch!
