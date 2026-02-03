**Title:**
2 Pins

**Body Text:**
The internal LDO can be configured as having 1.8 V, or the same voltage as VDD3P3_RTC. It can be powered off via software to minimize the current of flash/SRAM during the Deep-sleep mode.

**Subtitle:**
2.5.3 Chip Power-up and Reset

**Body Text:**
Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, CHIP_PU – the pin used for power-up and reset – is pulled high to activate the chip. For information on CHIP_PU as well as power-up and reset timing, see Figure 2-4 and Table 2-4.

**Figure:**
- Caption: "Visualization of Timing Parameters for Power-up and Reset"
- Image Description:
  - A graph showing VDD, t_STBL (Time to stabilize), t_RST (Reset time).

**Table Title:**
Table 2-4. Description of Timing Parameters for Power-up and Reset

| Parameter | Description | Min (\(\mu\)s) |
|-----------|-------------|---------------|
| t_STBL    | Time reserved for the 3.3 V rails to stabilize before the CHIP_PU pin is pulled high to activate the chip | 50            |
| t_RST     | Time reserved for CHIP_PU to stay below \(V_{IL_nRST}\) to reset the chip (see Table 5-3) | 50            |

**Body Text:**
In scenarios where ESP32 is powered up and down repeatedly by switching the power rails, while there is a large capacitor on the VDD33 rail and CHIP_PU and VDD33 are connected, simply switching off the CHIP_PU power rail and immediately switching it back on may cause an incomplete power discharge cycle and failure to reset the chip adequately.

An additional discharge circuit may be required to accelerate the discharge of the large capacitor on rail VDD33, which will ensure proper power-on-reset when the ESP32 is powered up again.

When a battery is used as the power supply for the ESP32 series of chips and modules, a supply voltage supervisor is recommended; so that a boot failure due to low voltage is avoided. Users are recommended to pull CHIP_PU low if the power supply for ESP32 is below 2.3 V.

**Subtitle:**
Notes on power supply:

- The operating voltage of ESP32 ranges from 2.3 V to 3.6 V. When using a single-power supply, the recommended voltage of the power supply is 3.3 V, and its recommended output current is 500 mA or more.
  
- PSRAM and flash both are powered by VDD_SDIO. If the chip has an in-package flash, the voltage of VDD_SDIO is determined by the operating voltage of the in-package flash. If the chip also connects to an external PSRAM, the operating voltage of external PSRAM must match that of the in-package flash.
  
  This also applies if the chip has an in-package PSRAM but also connects to an external flash.

**Footer:**
Espressif Systems
ESP32 Series Datasheet v5.2

**Page Number and Feedback Link:**
19 | Submit Documentation Feedback