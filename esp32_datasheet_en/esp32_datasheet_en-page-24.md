**Title: Boot Configurations**

---

### Figure Caption:
Figure 3-2. Chip Boot Flow

### Diagram Description:

1. **Reset**
   - Normal reset or Deep-sleep reset.
     - If normal reset, check strapping value.
       - GPIO0 GPIO2 = 1x -> Initialization
         - Copy the program from flash to RAM (Waiting for download from UART/SDIO)
           - Jump to entry point in RAM

### Text Content:

**3.2 Internal LDO (VDD_SDIO) Voltage Control**

The required VDD_SPI voltage for the chips of the ESP32 Series can be found in Table 1-1 Comparison.

MTDI is used to select the VDD_SDIO power supply voltage at reset:
- MTDI = 0 (by default), VDD_SDIO pin is powered directly from VDD3P3_RTC. Typically this voltage is 3.3V.
- For more information, see Section [2.5.2 Power Scheme](#).

MTDI = 1, VDD_SDIO pin is powered from internal 1.8 V LDO.

This functionality can be overridden by setting EFUSE_SDIOFORCE to 1, in which case the EFUSE_SDIO_TIEH determines the VDD_SDIO voltage:
- EFUSE_SDIO_TIEH = 0, VDD_SDIO connects to 1.8 V LDO.
- EFUSE_SDIO_TIEH = 1, VDD_SDIO connects to VDD3P3_RTC.

---

**Footer:**
Espressif Systems
24 ESP32 Series Datasheet v5.2

Submit Documentation Feedback