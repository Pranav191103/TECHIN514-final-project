# ButtonCounter – Wireless Button Press Gauge

## Slide 1 — Overview
ButtonCounter is a two-device system. A sensor device counts button presses and sends the count wirelessly. A display device shows the count using a stepper-motor gauge needle and an LED indicator.

**General sketch:**
[To be added]

---

## Slide 2 — Sensor Device
**Parts:**
- Processor/Wireless: ESP32-C3 development board
- Sensor: Momentary pushbutton
- Indicator: LED
- Power: USB

**Operation:**
The ESP32-C3 detects button presses, increments a counter, and transmits the count wirelessly to the display device.

**Detailed sensor sketch:**
[To be added]

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
The display ESP32-C3 receives the count, maps it to a gauge angle, and drives the stepper motor to move the needle. The LED provides visual feedback, and the reset button zeros the count.

**Detailed display sketch:**
[To be added]

---

## Slide 4 — Communication & System Diagram
**Communication:**
Sensor ESP32-C3 → Wireless (ESP-NOW or Wi-Fi) → Display ESP32-C3

**System logic:**
Button → Count → Transmit → Receive → Map to angle → Drive stepper → Update LED
