# 🔐 Smart Intrusion Alert System using ESP32

Developed a modular and real-time Smart Intrusion Alert System using the ESP32 
microcontroller to detect unauthorized motion and respond with immediate alerts 
across multiple interfaces.

## 🔧 Technologies Used
ESP32 · Embedded C/C++ · GPIO · PWM (LEDC) · Interrupts · WiFi · Bluetooth · 
I2C (OLED) · Finite State Machine · Non-blocking Programming (millis)

## 💡 Key Features
- Real-time intrusion detection using PIR and IR sensors
- Finite State Machine (DISARMED → ARMED → ALERT)
- Interrupt-driven button input for responsive control
- OLED display with dynamic UI and alert countdown
- WiFi-based web dashboard with real-time status
- Bluetooth command interface via mobile device
- Event logging (last trigger source + total alert count)
- Non-blocking firmware — sensors, display, commands run simultaneously

## 🏗 System Architecture
The firmware uses a 3-state FSM ensuring predictable behaviour. 
State transitions happen based on sensor input and user commands, 
with automatic reset from ALERT → ARMED after a fixed duration.

## 🖥 Multi-Interface Control
| Interface | Method |
|---|---|
| Physical | Interrupt-driven push button |
| Wireless | WiFi web dashboard |
| Mobile | Bluetooth serial commands |

