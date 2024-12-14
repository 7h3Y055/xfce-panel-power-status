# Power Status Plugin for XFCE4 Panel

A simple plugin for the XFCE4 panel that displays:
- The power source (AC or Battery).
- The battery status (Charging or Not Charging).
- The current mode (Performance or Power Save).

## Features
- Quick overview of your system's power status directly on the XFCE4 panel.
- Lightweight and easy to configure.

---

## Requirements
- XFCE4 with the **Generic Monitor** plugin installed.
- Basic Linux shell environment.

---

## Installation

### Step 1: Clone the Repository
Clone this repository to your local machine:
```bash
git clone git@github.com:7h3Y055/xfce-panel-power-status.git
cd xfce-panel-power-status
```

### Step 2: Install the Script
Move the `power_status` script to `/usr/bin`:
```bash
sudo mv power_status /usr/bin/
```
Ensure the script is executable:
```bash
sudo chmod +x /usr/bin/power_status
```

### Step 3: Add the Generic Monitor Plugin
1. Right-click on the XFCE4 panel and select **Panel > Add New Items**.
2. Choose **Generic Monitor** and add it to the panel.
3. Open the **Properties** of the Generic Monitor:
   - In the **Command** field, enter:
     ```bash
     power_status
     ```
   - Set the **Update Interval** (e.g., `5` seconds).
4. Apply and close the settings.

---

## Usage
The plugin will display the following information:
- The current power source (e.g., `AC` or `Battery`).
- The battery status (e.g., `Charging` or `Not Charging`).
- The system mode (e.g., `Performance` or `Power Save`).

---

## Example Output
```
Source: 🔌 | Bat0: 🔋❌ | Bat1: 🔋❌ | Mode: 🌱

```
---

## Customizing Emojis
If you need to edit the emojis displayed by the plugin, you can modify the `power_status` script. You'll find the relevant variables at the beginning of the file:

```bash
Source="Source:"
Bat0="Bat0:"
Bat1="Bat1:"
Mode="Mode:"

AC="🔌"
BAT="🔋"
not_charging="🔋❌"
charging="🔋⚡"
```

Simply change the values of these variables to your preferred emojis and save the file.

---

## Troubleshooting
- **Command Not Found:** Ensure the `power_status` script is in `/usr/bin` and executable.
- **No Output in Generic Monitor:** Verify the script works by running it in the terminal:
  ```bash
  power_status
  ```

---

## Contributing
Feel free to open issues or submit pull requests for improvements!

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
