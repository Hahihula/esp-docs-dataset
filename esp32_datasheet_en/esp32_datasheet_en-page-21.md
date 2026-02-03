**Title:**
2 Pins

---

**Table Title:** Table 2-6 – cont’d from previous page

| Chip Pin | Off-Package PSRAM |
|----------|--------------------|
| SD_DATA_1 | SIO0/SI           |
| SD_DATA_0 | SI01/SO           |
| SD_DATA_3 | SIO2              |
| SD_DATA_2 | SIO3              |
| SD_CLK/GPIO17^3 | SCLK         |
| GPIO16^2  | CE#               |
| GND      | VSS               |
| VDD_SDIO | VDD               |

---

**Note:**

1. As the in-package flash (ESP32-U4WDH) and the in-package PSRAM (ESP32-DOWDRH2-V3) operate at 3.3 V, VDD_SDIO must be powered by VDD3P3_RTC via a 6 Ω resistor. See Figure 2-3 ESP32 Power Scheme.

2. If GPIO16 is used to connect to PSRAM’s CE# signal, please add a pull-up resistor at the GPIO16 pin. See [ESP32-WROVER-E Datasheet > Figure Schematics of ESP32-WROVER-E](https://www.espressif.com/sites/default/files uploads/2021-09/ESP32-WROVER-E.pdf).

3. SD_CLK and GPIO17 pins are available to connect to the SCLK signal of external PSRAM.
   - If SD_CLK pin is selected, one GPIO (i.e., GPIO17) will be saved. The saved GPIO can be used for other purposes. This connection has passed internal tests, but relevant certification has not been completed.

**Please select the proper pin for your specific applications.**

---

*Espressif Systems*

*Submit Documentation Feedback*

ESP32 Series Datasheet v5.2