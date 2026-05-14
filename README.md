# 🛡️ IoT-Based Air Defence Detection and Response System

> A real-time aerial threat detection prototype built with ESP32, HC-SR04 ultrasonic sensor, and Blynk IoT cloud platform — demonstrating hardware-software co-design and IoT system architecture.

---

## 📌 Project Overview

This project simulates a simplified air defence system using affordable IoT components. An ultrasonic sensor continuously scans for objects in its detection range; upon detecting a potential threat, the system triggers multi-modal alerts and logs the event to a live cloud dashboard — all with a response time under 1 second.

**Project ID:** S-12 | **Institution:** KIIT University | **Year:** 2024–2025

---

## ⚙️ Components Used

| Component | Purpose |
|---|---|
| ESP32 Development Board | Main microcontroller — processes sensor data and manages alerts |
| HC-SR04 Ultrasonic Sensor | Measures object distance (2–400 cm range) |
| Servo Motor (SG90) | Rotates to simulate threat tracking |
| Red LED & Green LED | Visual threat / safe-state indicators |
| Buzzer | Audible alert on object detection |
| 220Ω Resistors | Current limiting for LEDs |
| Breadboard + Jumper Wires | Circuit prototyping |
| Blynk IoT Platform | Real-time cloud dashboard and remote monitoring |

---

## 🔧 Working Principle

1. **Detection** — The HC-SR04 sensor continuously emits ultrasonic pulses and measures the reflected echo to calculate object distance.
2. **Processing** — The ESP32 compares the measured distance against a predefined detection threshold (2–400 cm).
3. **Alert Trigger** — When an object enters the detection zone:
   - Red LED activates (threat indicator)
   - Buzzer sounds an audible alarm
   - Servo motor rotates to simulate object tracking
4. **Cloud Logging** — Detection status and sensor data are transmitted to the Blynk IoT platform for real-time dashboard monitoring.
5. **Safe State** — When no object is detected, the system holds a green-LED standby state.

---

## 📊 System Specifications

| Parameter | Value |
|---|---|
| Operating Voltage | 5V |
| Current Draw | ~200 mA |
| Power Consumption | ~1 W |
| CPU Usage | ~30% average |
| Detection Range | 2–400 cm |
| Response Time | < 1 second |

---

## 🗂️ Repository Structure

```
├── src/
│   └── main.ino          # Main Arduino/ESP32 firmware
├── docs/
│   ├── circuit_diagram/  # Circuit schematic and wiring diagram
│   └── poster.pdf        # Project poster (KIIT exhibition)
├── images/
│   └── hardware_setup/   # Photos of the assembled prototype
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Arduino IDE (v2.x recommended) or PlatformIO
- ESP32 board support package installed
- Blynk library (`Blynk` by Volodymyr Shymanskyy)
- `ESP32Servo` library

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/iot-air-defence-system.git
   cd iot-air-defence-system
   ```

2. Open `src/main.ino` in Arduino IDE.

3. Configure your credentials in the sketch:
   ```cpp
   #define BLYNK_AUTH_TOKEN "your_blynk_auth_token"
   #define WIFI_SSID        "your_wifi_ssid"
   #define WIFI_PASSWORD    "your_wifi_password"
   ```

4. Wire the components as per the circuit diagram in `docs/circuit_diagram/`.

5. Select **ESP32 Dev Module** as the target board and upload the firmware.

6. Open the Blynk app / web dashboard to monitor live detection data.

---

## 🖥️ Blynk Dashboard

The Blynk IoT integration provides:
- Live distance readings from the HC-SR04 sensor
- Threat detection status (Safe / Alert)
- Historical event log of detection triggers

---

## 📱 Applications

- Educational demonstration of air defence concepts
- IoT-based security and intrusion detection prototypes
- Smart surveillance and automation research
- Hardware-software co-design learning platform

---

## 🔭 Future Enhancements

- [ ] Camera module integration for visual surveillance
- [ ] AI-based object classification (drone vs. bird vs. debris)
- [ ] GPS-based threat tracking simulation
- [ ] Multi-sensor array deployment for wider coverage
- [ ] Edge ML inference directly on ESP32

---

## 🧠 Key Concepts Demonstrated

- **IoT System Architecture** — sensor → microcontroller → cloud pipeline
- **Hardware-Software Co-Design** — embedded C firmware with cloud integration
- **Real-Time Systems** — sub-1-second detection-to-alert latency
- **Power-Efficient Embedded Design** — ~1W operation at ~30% CPU usage

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).

---

## 👤 Author

Built as part of a project exhibition at **KIIT University (2024–2025)**.  
Feel free to open issues or submit pull requests for improvements!
