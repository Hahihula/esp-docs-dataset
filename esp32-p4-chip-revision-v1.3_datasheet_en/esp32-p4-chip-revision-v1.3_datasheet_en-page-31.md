**Title:**
2 Pins

**Table Title:**
Table 2-13. Description of Timing Parameters for Power-up and Reset

| Parameter | Description                                                                                   | Min (µs) |
|-----------|--------------------------------------------------------------------------------------------------|----------|
| t_STBL    | Time reserved for the power rails of VDD_LP, VDD_IO_0, VDD_USBPHY, VDD_PSRAM_0/1, VDD_IO_4, VDD_LDO. | 50       |
|           | VDD_DCDC, VDD_IO_5, VDD_IO_6 and VDD_ANA to stabilize before the CHIP_PU pin is pulled high to activate the chip |          |
| t_RST     | Time reserved for CHIP PU to stay below V_IL_nRST to reset the chip (see Table 5-4)                | 1000     |

**Footer:**
Espressif Systems  
31 ESP32-P4 Series Datasheet v0.6

**Link Texts:**
Submit Documentation Feedback