# OBS Auto-Recording Timer ⏳🎥

A modern, web-based control panel to automatically start and stop OBS Studio recording on a **10-minute and 1-second loop** (601 seconds) with a **5-second pre-roll countdown**. 

Perfect for creators who want to split their recordings into consistent 10-minute segments automatically without losing footage.

---

## 🚀 How to Run

### Option 1: Run it online (Recommended)
You don't need to install or download anything! Just open the live URL:
👉 **[https://joebelle-01.github.io/obstimer/](https://joebelle-01.github.io/obstimer/)**

### Option 2: Run it locally offline
1. Go to the GitHub repository: [https://github.com/Joebelle-01/obstimer](https://github.com/Joebelle-01/obstimer)
2. Click the green **Code** button and select **Download ZIP**.
3. Extract the ZIP file and double-click the `index.html` file to open it in your browser.

---

## 🔌 How to Connect to OBS Studio

This tool communicates directly with OBS Studio using its built-in WebSocket server. Follow these simple steps to configure it:

### Step 1: Enable WebSockets in OBS Studio
1. Open **OBS Studio** (v28.0 or newer).
2. In the top menu, go to **Tools** ➜ **WebSocket Server Settings**.
3. Check the box to **Enable WebSocket Server**.

### Step 2: Get Connection Details
1. **Server Port**: The default port is **`4455`**. 
   * This matches the default WebSocket URL in the web app: `ws://127.0.0.1:4455`
2. **Server Password**: 
   * Click the **Show Connect Info** button in OBS to reveal your password.
   * *If no password exists, click **Generate Password** to create one.*
   * Copy the password.

### Step 3: Connect in the Web App
1. Open the **OBS Auto-Recording Timer** in your browser.
2. In the **Connection** card:
   * Keep the **WebSocket URL** as `ws://127.0.0.1:4455` (change the port if your OBS is configured otherwise).
   * Paste your copied password into the **Password** field.
3. Click the blue **Connect** button.
4. Once connected, the status indicator will turn **Green** and display **Connected**.

---

## ⚙️ How It Works
* **Pre-roll (5s)**: A 5-second countdown gives you time to prepare before the recording begins.
* **Recording Loop (10m 01s)**: OBS starts recording and counts down from 10:01.
* **Auto-Split**: When the timer reaches `00:00`, it stops the recording, waits 1 second, and automatically restarts the cycle.
