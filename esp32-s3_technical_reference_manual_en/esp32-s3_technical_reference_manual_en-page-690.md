Title: Chapter 15 Permission Control (PMS)

Link: GoBack

---

Table Title: Table 15.3-8. Access Configuration to the Data Region of Internal SRAM1

| Buses       | From World     | Configuration Registers                   | Data Region data_region_0 | Data Region data_region_1 | Data Region data_region_2 |
|-------------|----------------|-------------------------------------------|----------------------------|----------------------------|---------------------------|
| IBUS        | Secure         | PM5_CORE_X_IRAMO_PMS CONSTRAINT_2_REG   | [data_region_0]           | [data_region_1]           | Access                    |
|             | World          | PMS_CORE_X_IRAMO_PMS CONSTRAIN_1_REG     | [data_region_0]           | [data_region_1]           | X/W/R                     |
|             | Non-secure     | PMS_CORE_X_IRAMO_PMS CONSTRAIN_1_REG     | [data_region_0]           | [data_region_1]           | X/W/R                     |
| DBUS        | Secure         | [3:2]                                      | [5:4]                      | [7:6]                      | W/R                       |
|             | World          | PMS_Core_XDRAMO_PMS CONSTRAIN_1_REG      | [data_region_0]           | [data_region_1]           | W/R                       |
|             | Non-secure     | PM5_CORE_X_DRAMO_PMS CONSTRAIN_1_REG     | [15:14]                    | [17:16]                    | W/R                       |
| GDMA XX B   | World          | PMS_DMA_APBPERI XX_PMS CONSTRAIN_1_REG    | [3:2]                      | [5:4]                      | W/R                       |

Body Text:

A Configure IBUS' access to the Data Region. However, it's recommended to configure these bits to 0.

B ESP32-S3 has 9 peripherals, including SPI2, SPI3, UCH1O, I2S0, I2S1, AES, SHA, ADC, LCD_CAM, USB, SDIO_HOST, and RMT, which can access internal SRAM via GDMA. Each peripheral can be configured with different access to the Internal SRAM1 independently.

For details on how to configure the split lines, see Section 15.3.2.3.

---

Subtitle: Trace Memory

Body Text:

ESP32-S3 has a low-power Xtensa® dual-core 32-bit LX7 microprocessor, which integrates a TRAX (Real-time Trace) module for easier debugging. For the TRAX module to work, users need to allocate 16 KB from the Internal SRAM1 as Trace memory. Note that, the Trace memories for CPU0 and CPU1 can be configured independently.

Users can allocate 16 KB from Internal SRAM1 as Trace memory by configuring the PMS_INTERNAL_SRAM USAGE_2_REG register.

Detailed steps are provided below:

1. First choose a block from Block2 ~ Block8 by writing 1 to the respective bit in the PMS_INTERNAL_SRAM COREm TRACE USAGE field

   - Block2: 0b00000001
   - Block3: 0b00000010
   - Block4: 0b00000100
   - Block5: 0b00001000
   - Block6: 0b00010000
   - Block7: 0b00100000
   - Block8: 0b10000000

2. Then choose 16 KB from this block as the Trace memory by configuring the PMS_INTERNAL_SRAM COREm TRACE ALLOC field.

   - 'b00': the first 16 KB

---

Footer:

Espressif Systems
Page Number: ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback