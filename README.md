# Smart Medicine Dispenser

> 📌 **Note:** If you want to view the source code, **please message me**. The code is currently private as it is used in a research paper.

This project is a **Smart Medicine Dispenser** using Arduino. It features a real-time clock (RTC), LCD display, stepper motor, EEPROM/SD card storage, and button-based UI. The system allows users to schedule up to 5 medicine alarms, automatically dispensing the correct dose at the specified time.

## 🔧 Features

- ⏰ Real-time alarm system using RTC DS1302
- 💾 Persistent storage using EEPROM or SD card
- 📟 LCD display with I2C interface
- 🔘 Three-button interface (Left, Right, Select) with long press support
- 🔁 Inactivity timeout system
- 🎵 Buzzer alarm with auto-off timeout
- 🚗 Stepper motor rotates to correct medicine slot
- 🧠 Saves alarm settings across restarts
- 🧪 Simulation commands via Serial monitor (e.g., `slot 1` to trigger an alarm manually)

## 🧠 System Overview

### Hardware Used
- Arduino (e.g., Uno, Mega)
- RTC Module (DS1302)
- I2C LCD (16x2)
- Stepper Motor + Driver (28BYJ-48 + ULN2003 or similar)
- SD Card module (optional)
- EEPROM (built-in)
- Buzzer
- Three push buttons (Left, Right, Select)
- Wires, resistors, etc.

### Alarm Slots
- Maximum: 5
- Customizable:
  - Hour (12-hour format)
  - Minute
  - AM/PM
  - Active/Inactive toggle
- Long press on **Select** enters edit mode

### Storage
- If SD card is available and initialized, it is used to store alarm settings (`slots.txt`)
- Otherwise, EEPROM is used to save/load alarm slot data

## 🧪 Usage Instructions

### Navigation
- **Select Button (Short Press):** Switch between view and set modes
- **Select Button (Long Press):** Enter/exit edit mode
- **Left/Right Buttons:** Navigate between slots or adjust values in edit mode

### Simulation (Optional)
You can trigger alarms manually via the Serial Monitor:
slot 1
slot 2
...
slot 5


## ⚙️ Setup

1. Wire all hardware components according to your pins:
    - Buttons: Pins 5, 6, 7
    - Buzzer: Pin 3
    - Stepper Motor: Pins 30, 32, 34, 36
    - RTC: Pins 8 (RST), 9 (DAT), 10 (CLK)
    - SD Card: Pin 53 (CS)
2. Upload the firmware (not included in this repository)
3. Power the device
4. Set your alarm slots via the UI

## 📁 Repository Notes

The source code for this project is not publicly available. This repository serves only as documentation for the functionality, system design, and setup process.

## 🧠 Future Improvements

- Battery backup for RTC and system
- More flexible alarm scheduling (days of week, repeat)
- OLED or TFT display support
- Wi-Fi/Bluetooth remote control or monitoring
- Full enclosure design

## 📜 License

This project is open for learning and non-commercial use. All rights reserved to the original author.

---

**Developed by:** Veigar CH  
**Project Type:** Arduino-based Medical Utility System
