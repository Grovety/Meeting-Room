# CrowPanel Meeting Room - ESP32S3

**CrowPanel Meeting Room** is a full-featured firmware for smart control of meeting rooms and conference spaces, built for the ELECROW CrowPanel Advance platform with a touchscreen and cloud service support.

## 📋 Description

The firmware is intended for the ELECROW CrowPanel Advance (5.0″ and 7.0″ variants) based on the ESP32-S3 with a display resolution of 800×480 pixels.
The application supports both hardware revisions (v1.0 and v1.1) and automatically detects the board revision at startup.

The system provides an intuitive touch interface for managing a meeting room schedule, booking time slots, displaying weather information, and monitoring indoor air quality.

---
## Installation and Setup

Installation and setup take less than 5 minutes.
See the detailed instructions here: https://github.com/Grovety/Meeting-Room/blob/main/Installation_and_Setup
___


## ⚙️ System Requirements

Before installation make sure you have:

* **Operating System:** Windows 10 or Windows 11 (64-bit)
* **USB driver:** CP210x USB-to-UART (for board communication)
* **Connection:** USB-C cable to connect the board to your computer

---

## ✨ Key Features

### 🗓️ Meeting Management

* **Room booking** — create and edit bookings directly from the panel
* **Google Calendar integration** — automatically display schedule from a cloud calendar
* **Schedule view** — clear representation of upcoming meetings on the screen

### 🌤️ Weather Information

* **Mini weather widget** — compact info on the dashboard (current temperature and conditions)
* **Detailed weather screen** — a dedicated screen with extended weather data
* **3-day forecast** — planning assistance using the short-term forecast

### 💨 Air Quality Monitoring

* **IAQ (Indoor Air Quality) index** — assessment of indoor air quality
* **CO₂ level** — monitoring of carbon dioxide concentration

### 🌐 Localization

* **Supported languages:** English (default), Deutsch (German)

### 😴 Sleep / Power Saving Mode

* **Auto sleep** — the device automatically enters a low-power mode after 5 minutes of inactivity (no touchscreen interaction)
* **Quick wake** — any touch instantly wakes the device and returns it to full operation

### 📱 Wireless Connectivity

* **Wi-Fi** — full wireless connectivity support
* **Cloud sync** — calendar and weather data fetched via the internet

---

## 📺 Available Screens

| Screen                      | Function                                                                        |
| --------------------------- | ------------------------------------------------------------------------------- |
| **Main Screen (Dashboard)** | Current time, mini weather widget, current meeting status, quick action buttons |
| **Calendar**                | List of all meetings with times and titles from the connected calendar          |
| **Weather**                 | Detailed weather information, 3-day forecast, temperature charts                |
| **Climate**                 | Indoor air quality monitoring (IAQ) and CO₂ level (requires EnSens module)      |
| **Booking**                 | Create new bookings                                                             |
| **Settings**                | Language selection, Wi-Fi setup, configure data sources for Google Calendar     |

## Main Screen (Dashboard)

![Main screen — mini widget and quick buttons](assets/images/dashboard.png)

## Weather Screen (Weather)

![Weather screen — detailed forecast](assets/images/weather_screen.png)

## Booking Screen (Booking room)

![Booking screen — booking UI](assets/images/booking.png)


---

## 📁 Repository Structure

```
Meeting-room/
├── README.md                      
├── Binaries/ - folder with binaries to flash to your panel
├── flash_tool.exe - automatic flasher for your panel
├── CrowPanelConfiguration.exe - configuration tool (Wi-Fi, calendar setup)
```

---

## 🔧 Technical Specifications

| Parameter               | Value                                 |
| ----------------------- | ------------------------------------- |
| **Microcontroller**     | ESP32-S3                              |
| **Display resolution**  | 800 × 480 pixels                      |
| **Display type**        | TFT LCD with touch                    |
| **Enclosure**           | ELECROW CrowPanel Advance 5.0″ / 7.0″ |
| **Supported revisions** | v1.0, v1.1 (auto-detection)           |
| **Interfaces**          | WiFi 802.11 b/g/n, USB-C (UART)       |
| **RAM**                 | 8 MB PSRAM                            |
| **Flash**               | 16 MB QSPI Flash                      |

---

## 📊 Data Sources

| Feature         | Source                    | Requirements                        |
| --------------- | ------------------------- | ----------------------------------- |
| **Calendar**    | Google Calendar (via ICS) | Internet connection, Google account |
| **Weather**     | OpenWeatherMap API        | Internet connection                 |
| **Air quality** | EnSens module (local)     | Connected sensor module             |
| **Time**        | NTP server                | Internet connection                 |

___

## 📋 Known Limitations

* Active internet connection is required for weather and calendar data
* Weather updates occur every 10 minutes
* Calendar updates occur every 5 minutes
* Maximum number of calendar events per day: 50
* Default system language: English

---

## 🔐 Security & Privacy

* **Cloud data:** Google Calendar access uses secure HTTPS connections
* **Local storage:** Weather and calendar data are stored locally on the device and not synchronized elsewhere


