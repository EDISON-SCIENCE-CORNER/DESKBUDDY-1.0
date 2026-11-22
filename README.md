<div align="center">

# 🤖 DeskBuddy 1.0

### A cute desk pet bot with animated eyes, moods, clock & live weather

[![YouTube](https://img.shields.io/badge/YouTube-Edison%20Science%20Corner-red?style=for-the-badge&logo=youtube)](https://www.youtube.com/@EDISON_SCIENCE_CORNER)
[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=black)](https://buymeacoffee.com/esclabs)

</div>

---

## ✨ Features

- 👀 **Animated eyes** – smooth spring-based movement, pupils that follow the gaze, random blinks, idle glances and a gentle "breathing" effect
- 😊 **9 moods** – normal, happy, surprised, sleepy, angry, sad, excited, love and suspicious, each with its own eyelid shape and floating icon
- 🌦️ **Weather-reactive** – the current weather can set DeskBuddy's mood automatically
- 🕒 **Clock & date** – synced over the internet (NTP)
- 🌍 **World clock** – India and Sydney
- ☁️ **Live weather card + 3-day forecast** – from OpenWeatherMap, refreshed every 10 minutes
- 🔄 **Auto-rotating pages** – switches every 8 seconds
- 👆 **Single touch control** – no buttons needed
- 📶 **Wi-Fi setup portal** – configure Wi-Fi from your phone, settings saved to flash
- 🎬 **Boot animation** – circle-wipe intro

---

## 🧰 Hardware Required

| Component | Details |
|---|---|
| Microcontroller | ESP32-C3 board (Wi-Fi) |
| Display | 1.3" 128×64 OLED, **SH1106** driver, I²C (address `0x3C`) |
| Touch sensor | TTP223 touch module (or a touch pad on the pin below) |
| Enclosure | 3D-printed – `deskbuddy.stl` |
| Misc | Jumper wires, USB cable |

See **`component list.jpeg`** for the full parts list.

---

## 🔌 Wiring

| OLED / Sensor | ESP32 Pin |
|---|---|
| OLED SDA | GPIO 8 |
| OLED SCL | GPIO 9 |
| OLED VCC | 3.3V |
| OLED GND | GND |
| Touch signal | GPIO 7 |
| Touch VCC | 3.3V |
| Touch GND | GND |

📐 Full circuit: **`deskbuddy circuit.png`** · Fritzing file: **`deskbuddy files.fzz`**

---

## 👆 Touch Controls

| Action | What it does |
|---|---|
| **Tap** | Next page |
| **Double tap** | Toggle brightness |
| **Long press** | Change eye mood / switch sub-page |
| **Hold at power-on** | Open Wi-Fi setup portal |

---

## 💻 Software Setup

### 1. Install Arduino IDE & ESP32 board support
- Install the [Arduino IDE](https://www.arduino.cc/en/software)
- Add the ESP32 boards package (Boards Manager → search **esp32** by Espressif)

### 2. Install libraries
Through **Library Manager**:
- `Adafruit GFX Library`
- `Adafruit SH110X`
- `Arduino_JSON`

(`WiFi`, `WebServer`, `Preferences`, `HTTPClient` and `Wire` come with the ESP32 core.)

### 3. Get a free weather API key
Sign up at [OpenWeatherMap](https://openweathermap.org/api) and copy your API key.

### 4. Upload
1. Open `deskbuddy.ino`
2. Enter your Wi-Fi details, city and OpenWeatherMap API key
3. Select your ESP32 board and COM port
4. Click **Upload** 🚀

---

## 📶 Wi-Fi Setup Portal

If DeskBuddy can't connect to Wi-Fi (or you hold the touch sensor while powering on), it creates its own hotspot:

1. Connect your phone to the Wi-Fi network **`DeskBuddy-Setup`**
2. Open the setup page in your browser
3. Enter your Wi-Fi and weather details and save
4. DeskBuddy restarts and connects ✅

---

## 🖨️ 3D-Printed Case

Print **`deskbuddy.stl`** in PLA. Fit the OLED in the front window, mount the ESP32 inside and place the touch sensor where it's easy to tap.

---

## 📁 Repository Files

| File | Description |
|---|---|
| `deskbuddy.ino` | Main Arduino firmware |
| `deskbuddy.stl` | 3D-printable enclosure |
| `deskbuddy circuit.png` | Circuit diagram |
| `deskbuddy files.fzz` | Fritzing project |
| `component list.jpeg` | Parts list |
| `tiny/` | Additional files |

---

## 🎥 Watch the Build

Full build video and more projects on my YouTube channel:

👉 **[Edison Science Corner](https://www.youtube.com/@EDISON_SCIENCE_CORNER)**

Don't forget to **Like, Share & Subscribe!** 🔔

---

## ☕ Support

If you enjoyed this project and want to support more open-source builds:

<a href="https://buymeacoffee.com/esclabs" target="_blank">
  <img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" height="50">
</a>

---

## ⭐ Show Your Love

If you like DeskBuddy, give this repo a **star ⭐** and share your builds!

<div align="center">

Made with ❤️ by **[Edison Science Corner](https://www.youtube.com/@EDISON_SCIENCE_CORNER)** · **ESC Labs**

</div>
