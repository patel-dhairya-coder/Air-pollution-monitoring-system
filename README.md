# 🌍 Smart Air Pollution Monitoring System using Arduino UNO

A portable **Air Pollution Monitoring System** built using **Arduino UNO** that monitors multiple environmental parameters including air quality, temperature, humidity, and dust concentration. The system displays live sensor values on a **16x2 I2C LCD**, provides visual alerts using an RGB LED, and sounds a buzzer when pollution exceeds predefined thresholds.

---

## 📷 Project Preview
<img width="896" height="1190" alt="APMS" src="https://github.com/user-attachments/assets/e3161420-bd69-4057-8799-eb1587ad3d3d" />

```
images/
├── front_view.jpg
```

---

## ✨ Features

* 🌡 Temperature Monitoring (DHT22)
* 💧 Humidity Monitoring
* 🌫 Dust Monitoring (Sharp GP2Y1010AU0F)
* ☁ Air Quality Monitoring
* 🏭 MQ-135 Gas Sensor
* 🔥 MQ-2 Smoke/LPG Sensor
* 🚗 MQ-7 Carbon Monoxide Sensor
* 📟 16x2 I2C LCD Display
* 📄 Multiple LCD Pages
* 🔘 Push Button Page Switching
* 🔴🟢🔵 RGB LED Air Quality Indicator
* 🔊 Buzzer Alert System
* 🔋 Portable Battery Powered
* 🔌 Rechargeable using TP4056 Module

---

# Hardware Used

| Component                           | Quantity |
| ----------------------------------- | -------: |
| Arduino UNO                         |        1 |
| MQ135 Gas Sensor                    |        1 |
| MQ2 Gas Sensor                      |        1 |
| MQ7 CO Sensor                       |        1 |
| Sharp GP2Y1010AU0F Dust Sensor      |        1 |
| DHT22 Temperature & Humidity Sensor |        1 |
| 16x2 LCD with I2C                   |        1 |
| RGB LED                             |        1 |
| Active/Passive Buzzer               |        1 |
| Push Button                         |        1 |
| TP4056 Charging Module              |        1 |
| MT3608 Boost Converter              |        1 |
| Lithium-Ion Battery                 |        1 |
| 220µF Capacitor                     |        1 |
| 150Ω Resistor                       |        1 |
| 220Ω Resistors                      |        3 |
| PCB / Perfboard                     |        1 |

---

# Pin Connections

| Component          | Arduino Pin |
| ------------------ | ----------- |
| MQ135              | A0          |
| MQ2                | A1          |
| MQ7                | A2          |
| Dust Sensor Output | A3          |
| LCD SDA            | A4          |
| LCD SCL            | A5          |
| Page Button        | D2          |
| DHT22              | D8          |
| Dust LED Control   | D9          |
| Buzzer             | D10         |
| RGB Red            | D11         |
| RGB Green          | D12         |
| RGB Blue           | D13         |

---

# Dust Sensor Connections

| Dust Sensor Pin | Arduino                  |
| --------------- | ------------------------ |
| VCC             | 5V                       |
| GND             | GND                      |
| Vo              | A3                       |
| LED             | D9                       |
| VLED            | 5V through 150Ω resistor |
| LED-GND         | GND                      |

Additional Components:

* 220µF Capacitor across VCC and GND
* 150Ω resistor in series with VLED

---

# Power Supply

```
Lithium Battery
       │
    TP4056
       │
 Power Switch
       │
 MT3608 Boost Converter
       │
     Arduino UNO (5V)
```

---

# LCD Pages

### Page 1

* Temperature
* Humidity

### Page 2

MQ2 Value

### Page 3

MQ7 Value

### Page 4

MQ135 Value

### Page 5

Dust Sensor Value

### Page 6

Overall Air Quality

---

# Air Quality Levels

| Status       | Condition                  |
| ------------ | -------------------------- |
| 🟢 GOOD      | MQ135 < 200 & Dust < 250   |
| 🔵 MODERATE  | MQ135 < 400 & Dust < 400   |
| 🔴 POOR      | MQ135 < 600 & Dust < 600   |
| 🚨 HAZARDOUS | Above the above thresholds |

---

# Startup Sequence

* 100-second sensor warm-up
* LCD loading animation
* Countdown timer
* System Ready screen

---

# Software

* Arduino IDE
* C++

Libraries:

```
Wire.h
LiquidCrystal_I2C.h
DHT.h
```

---

# Folder Structure

```
Smart-Air-Pollution-Monitor/

│
├── Arduino_Code/
│   └── SmartAirMonitor.ino
│
├── Images/
│   ├── front.jpg
│
├── Schematic/
│   ├── circuit.pdf
│   └── schematic.kicad_sch
│
├── README.md
└── LICENSE
```

---

# Future Improvements

* Wi-Fi Connectivity (ESP8266/ESP32)
* Cloud Data Logging
* Mobile Application
* AQI Calculation using EPA Standards
* GPS Location
* SD Card Data Logging
* Battery Percentage Display
* OLED/TFT Display
* Real-Time Clock (RTC)
* IoT Dashboard

---

# Author

**Dhairya Patel**

Computer Science Engineering Student

---

# License

This project is released under the **MIT License**.

Feel free to fork, improve, and contribute.

⭐ If you found this project useful, consider giving it a star!
