# Endeavor — Personal Linux Scripts

A collection of shell scripts and utilities built for daily use on Arch-based Linux systems (EndeavourOS / CachyOS). Written to automate repetitive tasks and extend desktop functionality.

## Scripts

### `battery.sh`
Automated battery management daemon for laptops.

- Switches to **power-saver** mode below 60%
- **Suspends** the system at 40% (discharging only)
- **Shuts down** at 20% with a 5-second warning notification
- Reverts to **balanced** mode above 70%
- Runs as a background loop, checks every 60 seconds

**Dependencies:** `acpi`, `power-profiles-daemon`, `libnotify`

---

### `hotspot.sh`
Toggle script for a Wi-Fi hotspot using `create_ap`.

- Starts hotspot on `wlan0` at channel 40 with SSID `ARCspot`
- Kills the hotspot if already running
- Sends desktop notifications on enable/disable

**Dependencies:** `create_ap`, `libnotify`, `pkexec`

---

### `Calendar.sh`
Toggle script for an AGS-based calendar/dashboard widget.

- Starts AGS if not running, kills it if it is
- Designed for use as a keybind or panel button

**Dependencies:** `ags`

---

### `Dashboard.py`
Minimal floating system monitor built with Tkinter.

Displays live:
- CPU usage (via `psutil`)
- GPU usage (NVIDIA only via `nvidia-smi`)
- Battery status (percentage + charging state)
- Wi-Fi, Bluetooth status (via `nmcli`, `bluetoothctl`)

**Dependencies:** `python`, `psutil`, `tkinter` (stdlib)

---

## System

Tested on **CachyOS** (Arch-based). Should work on most systemd-based distros with minor adjustments.

---

> Personal scripts — expect rough edges. Built to solve real annoyances, not to be pretty.
