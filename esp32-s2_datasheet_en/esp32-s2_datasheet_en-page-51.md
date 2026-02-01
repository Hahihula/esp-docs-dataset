Title: Electrical Characteristics

---

Subtitle: Wi-Fi Current Consumption Depending on RF Modes

Table:
- **Column Headers**: Work Mode, Description, Peak (mA)
- **Rows**:
  - TX Active (RF working): 
    - 802.11b, 20 MHz, 1 Mbps, @19.5 dBm: 310
    - 802.11g, 20 MHz, 54 Mbps, @15 dBm: 220
    - 802.11n, 20 MHz, MCS7, @13 dBm: 200
    - 802.11n, 40 MHz, MCS7, @13 dBm: 160
- **Note**: The consumption in RX mode is measured when peripherals are disabled and the CPU is idle.

---

Subtitle: Current Consumption in Other Modes

Body Text:
The measurements below are applicable to ESP32-S2, ESP32-S2FH2, and ESP32-S2FH4. Since ESP32-S2FN4R2 and ESP32-S2R2 come with in-package PSRAM, their current consumption might be higher.

Table 5-8: Current Consumption in Modem-sleep Mode

- **Column Headers**: Mode, CPU Frequency (MHz), Description
- **Rows**:
  - All Peripherals Clocks Disabled (mA): 
    - Typ: CPU is idle | 20.0 | 240
    - Typ: CPU is running | 16.0 | 80

---

Table:

- **Column Headers**: Mode, Description, Typ (µA)
- **Rows**:
  - Light-sleep^1 VDD_SPI and Wi-Fi are powered down, and all GPIOs are high-impedance: 
    - ULP-FSM is powered on^2 | 750
  - Deep-sleep^3 ULP sensor-monitored pattern^3 | 190

---

Table:
- **Column Headers**: Work mode Description Typ (µA)
- **Rows**:
  - Power off CHIP_PU is set to low level, the chip is powered off: 
    - ESP32-S2 Series Datasheet v1.8
    - Submit Documentation Feedback