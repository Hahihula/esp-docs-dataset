**Chapter Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**GoBack Link:** [GoBack](#)

---

## Overview

This LCD and Camera (LCD_CAM) controller consists of a LCD module and a camera module. The LCD module is designed to send parallel video data signals, and its bus supports RGB, MOTO6800, and I8080 interface timing. The camera module is designed to receive parallel video data signals, and its bus supports DVP 8-/16-bit modes.

### Features

- **Supports the following operation modes:**
  - LCD master TX mode
  - Camera slave RX mode
  - Camera master RX mode

- Supports simultaneous connection to an external LCD and an external camera when connected with an external LCD, the following is supported:
  - 8-/16-bit parallel output mode
  - RGB, MOTO6800, and I8080 LCD formats
  - LCD data retrieved from internal memory via GDMA

- When connected with an external camera (i.e., DVP image sensor), the following is supported:
  - 8-/16-bit parallel input mode
  - Camera data stored into internal memory via GDMA
  - Supports LCD_CAM interface interrupts

---

## Functional Description

### Block Diagram

Figure **29.3-1** shows the structure of this LCD_CAM module, including:

- 1 x TX control unit (LCD_Ctrl)
- 1 x RX control unit (Camera_Ctrl)

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback  

**Page Number:** ESP32-S3 TRM (Version 1.7)