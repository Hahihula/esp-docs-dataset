**Title:**
Table 2-9. Peripheral Pin Assignment

**Header Row (with color coding):**
- **Pin No:** [Green]
- **Pin Name:** [Blue]
- **ADC1:** [Light Blue] | **ADC2:** [Light Green] | **DAC:** [Yellow] | **Touch Sensor:** [Orange] | **I2C:** [Purple] | **UART0:** [Pink] | **UART1:** [Red] | **SPI/SPI (recommended):** [Dark Red] | **SPI/SPI (alternative):** [Light Purple] | **SPI2:** [Light Blue] | **SPI3:** [Blue] | **USB OTG:** [Green] | **I2C:** [Purple] | **PCNT:** [Pink] | **RMT1:** [Red] | **LEDC:** [Dark Red]

**Content:**
The table lists various pin names and their assignments to different peripherals. Each cell in the main body of the table is color-coded according to a legend at the bottom, which indicates what each color represents.

**Footer Notes (with references):**
1. For USB OTG, use USB\_D+ when on internal PHY; for the USB\_D-, and USB\_D+, can be swapped by configuring the EFUSE, USB\_EXCH\_PINS bit according to ESP32-S2 Technical Reference Manual.
2. Signals of UART0, UART1, SPI0/1, SPI2 and USB OTG interfaces are mapped as follows: [Read pins via IO MIX]

**Side Text (Vertical):**
- "Espressif Systems"
- "Submit Documentation Feedback"

**Page Numbering:** 
- Page 24
- Series Datasheet v1.8

(Note: The specific pin assignments and their corresponding peripherals in the table are not transcribed here due to length, but they follow a similar pattern as described above.)