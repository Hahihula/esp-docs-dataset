**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Table of Pin Information:
| GPIO | Pin Name | Function 0 | Function 1 | Function 2 | Function 3 | Function 4 | DRV | RST | Notes |
|-------|----------|------------|------------|------------|------------|-----------|-----|-----|-------|
| 42    | MTMS     | MTMS       | GPIO42     | -          | -          | -         | 2   | 1   | -     |
| 43    | UOTXD    | UOTXD      | GPIO43     | CLK_OUT1  | -          | -         | 2   | 4   | -     |
| 44    | UORXD    | UORXD      | GPIO44     | CLK_OUT2  | -          | -         | 2   | 3   | -     |
| 45    | GPIO45   | GPIO45     | GPIO45     | -          | -          | -         | 2   | 2   | -     |
| 46    | GPIO46   | GPIO46     | GPIO46     | -          | -          | -         | 2   | 2   | -     |
| 47    | SPICLK_P | SPICLK_P   | SPICLK_PDIFF | -       | SUBSPICLK_P_DIFF | - | 2 | 1 | - |
| 48    | SPICLK_N | SPICLK_N   | SPICLK_N_DIFF | -      | SUBSPICLK_N_DIFF | - | 2 | 1 | - |

### Drive Strength
**Note:** "DRV" column shows the drive strength of each pin after reset:

- GPIO17 and GPIO18:
  - 0: Drive current = ~5 mA
  - 1: Drive current = ~20 mA
  - 2: Drive current = ~10 mA
  - 3: Drive current = ~40 mA

**Other GPIOs**
- 0: Drive current = ~5 mA
- 1: Drive current = ~10 mA
- 2: Drive current = ~20 mA
- 3: Drive current = ~40 mA

### Reset Configurations
**Note:** "RST" column shows the default configuration of each pin after reset:

- 0: IE = 0 (input disabled)
- 1: IE = 1 (input enabled)
- 2: IF = 1, WPD = 1 (input enabled, pull-down resistor enabled)
- 3: IE = 1, WPU = 1 (input enabled, pull-up resistor enabled)
- 4: OE = 1, WPU = 1 (output enabled, pull-up resistor enabled)

**Special Notes**
- If EFUSE_DIS_PAD_JTAG = 1, the pin MTCK is left floating after reset i.e., IE = 1. If EFUSE_DIS_PAD_JTAG = 0, the pin MTCK is connected to internal pull-up resistor i.e., IE = 1, WPU = 1.
- R: Pin has RTC/analog functions via RTC IO MUX.

---

**Footer:**  
Please refer to Appendix A – ESP32-S3 Pin Lists in [ESP32-S3 Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet.pdf) for more details.  

Espressif Systems  
494  
[Submit Documentation Feedback](#)  
ESP32-S3 TRM (Version 1.7)