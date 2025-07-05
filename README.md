# 🚗 Car Safety System using ESP32

This repository contains code, documentation, and circuit details for our **Car Safety System** project.  
Built around the **ESP32 microcontroller**, it integrates multiple sensors to detect crashes, gas leaks, and track real-time GPS location.  
Sensor data is published to **Adafruit IO** via **MQTT**, allowing live monitoring through a dashboard.

---

## 📌 About the Project

The system uses:
- **NEO-6M GPS Module** → For real-time car location tracking
- **MQ2 Gas Sensor** → For detecting gas leaks (e.g., LPG, smoke)
- **Piezoelectric vibration sensor** → For detecting physical shocks/crashes
- **ESP32** → Acts as the central controller and communicates over Wi-Fi

All collected data is securely published to Adafruit IO, so emergency services or family members can monitor incidents along with live location.

---


## 🛠️ Components & Tools Used

- ESP32 microcontroller
- NEO-6M GPS module
- MQ2 gas sensor
- Piezoelectric vibration sensor
- Buzzer (for alerts)
- Wi-Fi network (2.4 GHz)
- Adafruit IO account
- Arduino IDE (for coding)

---

## 🚀 How It Works

- **ESP32** reads:
  - GPS location data from NEO-6M
  - Gas levels from MQ2 sensor
  - Vibration values from piezo sensor
- When gas concentration exceeds threshold → triggers buzzer alert
- Publishes:
  - Gas values to Adafruit IO feed `/feeds/gas`
  - Piezo sensor values to `/feeds/piezo`
  - GPS data can also be published for live tracking
- Data is visualized on **Adafruit IO dashboard** in real-time

---

✍️ Contributing
Feel free to:

Suggest improvements

Add new sensors or features (e.g., temperature, camera)

Improve data formatting or visualization

Open an issue or pull request!

📜 License
Project released under the MIT License.
Free to use for academic and learning purposes.


