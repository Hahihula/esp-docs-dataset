Title: Electrical Characteristics

Subtitle: Chip reset voltage (CHIP_PU voltage is within the specified range)
- VIL_nRST: —0.3 to +0.25 × VDD^1 V
  - Note:
    1. VDD – voltage from a power pin of a respective power domain.
    2. VOH and VOL are measured using high-impedance load.

Section Title: 5.4 Current Consumption Characteristics

Body Text:
Owing to the use of advanced power-management technologies, the module can switch between different power modes. For details on different power modes, please refer to Section RTC and Low-Power Management in ESP32-S2 Series Datasheet.

Subsection Title: 5.4.1 Current Consumption in Active Mode

Table:
- Table Caption: RF Current Consumption in Active Mode
- Column Headers: Work mode | Description | Peak (mA)
- Rows:
  - "802.11b, 20 MHz, 1 Mbps, @19.5 dBm" with peak current of 320 mA.
  - "802.11g, 20 MHz, 54 Mbps, @17.5 dBm" with peak current of 273 mA.
  - "802.11n, 20 MHz, MCS7, @16.5 dBm" with peak current of 265 mA (Active RF working).
  - "802.11b/g/n, 40 MHz, MCS7, @16.5 dBm" with peak current of 274 mA.
  - "RX: 802.11n, 40 MHz" with peak current of 81 mA.

Footnotes:
- Note on the table data (in a box):
  The content below is excerpted from Section Power Consumption in Other Modes in ESP32-S2 Series Datasheet.
  
Section Title: 5.4.2 Current Consumption in Other Modes

Body Text:
The measurements below are applicable to ESP32-S2, ESP32-S2FH2, and ESP32-S2FH4. Since ESP32-S2FN4R2 and ESP32-S2R2 come with in-package PSRAM, their current consumption might be higher.

Footer: Espressif Systems
- Page Number: 19
- Document Reference: ESP32-S2-SOLO-2 & SOLO-2U Datasheet v1.3

Link Text:
- Submit Documentation Feedback