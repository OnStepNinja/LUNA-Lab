# LUNA Lab Edition Firmware Flashing Guide

**Target Version**: v1.x.x (Lab32 / LabS3 / LabNode)
**Updated**: 2026-07-31

---

## Download the Firmware

Download the firmware from the GitHub Releases page:

> 📦 **GitHub Releases**: [https://github.com/OnStepNinja/LUNA-Lab/releases](https://github.com/OnStepNinja/LUNA-Lab/releases)

### Files Included in the Download

- `LabXX_vX.x.x.ino.bootloader.bin`
- `LabXX_vX.x.x.ino.partitions.bin`
- `LabXX_vX.x.x.ino.bin`
- **`flash_command.txt`** ← Verified flash command (ready to use)

---

### Step 1: Install Python and esptool

1. Download and install Python from [Python.org](https://www.python.org/)
   - **Important**: During installation, check the box **"Add Python to PATH"**
2. Open Command Prompt and run:
   ```
   pip install esptool
   ```

---

### Step 2: Connect the ESP32 to Your PC

1. Depending on your board, use either a **USB cable or an RS-232C cable**
2. Identify the COM port:
   - Right-click the Start button → **Device Manager** → expand **"Ports (COM & LPT)"**
   - Note the port number (e.g., COM3)

---

### Step 3: Enter Flash Mode (if needed)

If flashing does not start automatically:

1. Hold down both the **BOOT button** and the **RESET button** simultaneously
2. **Release the RESET button first**, then release the **BOOT button**

---

### Step 4: Run the Flash Command

1. Open the folder containing the firmware files, then **Shift + Right-click** in an empty area → select **"Open PowerShell window here"**
2. Open `flash_command.txt`, replace `COM3` with your actual port number, then copy and paste the command
3. Press **Enter** to run

A successful flash will show:
```
Hash of data verified.
Hard resetting via RTS pin...
```

Press the **RESET button** once to boot the new firmware.

---

### Step 5: Initial WiFi Setup

After the first boot, LUNA starts in AP mode.

1. Open WiFi settings on your PC or smartphone
2. Connect to **`LUNA_XXXX`** (XXXX is a unique string for your board)
3. Open **`http://192.168.4.1`** in a browser
4. Open **File Manager**
   - **First time only**: Run **Format SPIFFS**
5. In **WiFi Configuration**, press the **Load Config** button, then enter your **SSID** and **Password**, and press **Save Config**
6. Press the **RESET** button — LUNA will reboot and connect to your home router
7. Check your router's DHCP client list or the LUNA Web Console to find the assigned IP address

> **Tip**: Setting a static IP for LUNA in your router (DHCP reservation) ensures a stable connection.

Once WiFi setup is complete, proceed to **LUNA_Getting_Started.md**.

---

## Troubleshooting

| Symptom | Solution |
|---------|---------|
| `'python' not found` | Try using `python3` instead of `python` |
| `Connection Failed` | Repeat the button sequence in Step 3. Charge-only USB cables will not work. |
| `LUNA_XXXX` not found | Press the RESET button once to reboot LUNA |
| Cannot connect after WiFi setup | Double-check SSID and password. LUNA does not support 5GHz WiFi — use 2.4GHz. |

---

*LUNA Lab Edition — talk to your hardware. © 2026 Nishioka Sadahiko*
