**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Body Text:**

- The split line that splitting the Instruction Region and Data Region can be configured anywhere inside Internal SRAM1.
  
- The two split lines further splitting the Instruction Region into 3 split regions must stay inside the Instruction Region.

- The two split lines further splitting the Data Region into 3 split regions must stay inside the Data Region.

**Subsection Title:**
Spilt lines can overlap with each other. For example,

- When the two spilt lines inside the Data Region are not overlapping with each other, then the Data Region is split into 3 split regions

- When the two spilt lines inside the Data Region are overlapping with each other, then the Data Region is only split into 2 split regions

- When the two spilt lines inside the Data Region are not only overlapping with each other but also with the spilt line that splits the Data Region and the Instruction Region, then the Data Region is not split at all and has one region.

**Subsection Title:**
Access Configuration

After configuring the split lines, users can then use the registers described in the Table 15.3-7 and Table 15.3-8 below to configure the access of CPU’s IBUS, DBUS and GDMA peripherals from the Secure World and Non-secure World, to these split regions independently.

**Table Title:**
Table 15.3-7. Access Configuration to the Instruction Region of Internal SRAM1

| Buses       | From World     | Configuration Registers                                      | Instruction Region | Access |
|-------------|----------------|--------------------------------------------------------------|--------------------|-------|
| IBUS        | Secure World   | PMS\_CORE\_X\_IRAMO\_PMS\_CONSTRAIN\_2\_REG                  | [2:0]              | [5:3] | X/W/R  |
|            | Non-secure World| PMS\_Core\_X\_IRAMO\_PMS\_CONSTRAIN\_1\_REG                   | [2:0]              | [8:6] | W/X/R   |
| DBUS        | Secure World   | PMS\_Core\_X\_DRAMO\_PMS\_CONSTRAIN\_1\_REG                   | [1:0]^A            |       | W/R     |
|            | Non-secure World| PMS\_Core\_X\_DRAMO\_PMS\_CONSTRAIN\_2\_REG                   | [13:12]^A          |       | W/R     |
| GDMA        | Peripherals    | PMS\_DMA\_APBPERI\_XX\_PMS\_CONSTRAIN\_1\_REG                 | ^C                 | [1:0]^B | W/R     |

**Footnotes in Table:**
- A Configure DBUS’ access to the Instruction Region. However, it’s recommended to configure these bits to 0.
- B Configure GDMA’s access to the Instruction Region. However, it’s recommended to configure these bits to 0.
- C ESP32-S3 has 9 peripherals, including SPI2, SPI3, UCHIO, I2S0, I2S1, AES, SHA, ADC, LCD_CAM, USB, SDIO_HOST, and RMT, which can access Internal SRAM1 via GDMA. Each peripherals can be configured with different access to the Internal SRAM1 independently.

**Footer:**
Espressif Systems
689 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback