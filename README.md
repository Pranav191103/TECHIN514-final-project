# Wireless Temperature Gauge

## Slide 1 — Overview
Wireless Temperature Gauge is a two-device system. A sensor device measures temperature and sends the value wirelessly. A display device visualizes the temperature using a stepper-motor-driven gauge needle and an LED indicator.

**General sketch:**
![overview](https://github.com/user-attachments/assets/f27abf29-9b91-41e6-9690-4b366f94c466)

---

## Slide 2 — Sensor Device
**Parts:**
- Processor/Wireless: ESP32-C3 development board
- Sensor: Temperature sensor (e.g., LM35 or DS18B20)
- Indicator: LED
- Power: USB

**Operation:**
The ESP32-C3 reads temperature data from the sensor and transmits the measured value wirelessly to the display device.
**Detailed sensor sketch:**
![sensor](https://github.com/user-attachments/assets/3ee4a23c-d7fc-42a9-94dc-10cd20dd2963)

---

## Slide 3 — Display Device
**Parts:**
- Processor/Wireless: ESP32-C3 development board
- Stepper motor: 28BYJ-48 (5V)
- Stepper driver: ULN2003A
- Indicator: LED
- Button: Reset button
- Power: USB

**Operation:**
The display ESP32-C3 receives temperature data, maps the value to a gauge angle, and drives the stepper motor to move the needle. The LED provides visual feedback, and the reset button resets the displayed value.

**Detailed display sketch:**
![display](https://github.com/user-attachments/assets/bea24069-6d76-4a45-afc1-a0a31cf03a0a)

---

## Slide 4 — Communication & System Diagram
**Communication:**

Sensor ESP32-C3 → Wireless (ESP-NOW or Wi-Fi) → Display ESP32-C3
![system](https://github.com/user-attachments/assets/a108482e-50e2-4825-8163-e9fa1360b13f)

**System logic:**
Temperature → Measure → Filter → Transmit → Receive → Map to angle → Drive stepper → Update LED
