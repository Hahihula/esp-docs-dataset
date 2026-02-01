**Title:**
2.6 Pin Mapping Between Chip and Flash/PSRAM

**Body Text:**

Table 2-11 lists the pin mapping between the chip and flash/PSRAM for all SPI modes.

For chip variants with in-package flash/PSRAM (see Table 1-1 Comparison), the pins allocated for communication with in-package flash/PSRAM can be identified depending on the SPI mode used. The recommended pins for connecting to off-package flash/PSRAM can be found in table below.

For variants with in-package flash/PSRAM, the in-package flash or PSRAM must be powered by VDD_SPI, and the corresponding pin cannot be used as a digital function pin.

For off-package flash or PSRAM, the power supply is optional. It can be provided either by VDD_SPI or by an external power source supplied by the user. In general, if VDD_SPI is used to power flash or PSRAM, then the pin cannot be used as a digital function pin.

For more information on SPI controllers, see also Section 4.2.1.2 SPI Controller.

**Notice:**
It is not recommended to use the pins connected to flash/PSRAM for any other purposes.

**Table Title:**
Table 2-11. Pin Mapping Between Chip and Off-Package Flash for ESP32-C61^1

| Pin No. | Pin Name       | Single SPI Flash | Dual SPI Flash | Quad SPI Flash |
|---------|----------------|------------------|----------------|----------------|
|         |                |                  |                |                |
| 26      | SPICLK         | CLK              | CLK            | CLK            |
| 20      | SPICSO^2       | CS#              | CS#            | S#             |
| 27      | SPID           | MOSI             | SIOO^3         | SOO            |
| 22      | SPIQ           | MISO             | SIO1^4        | SO1            |
| 23      | SPIWP          | WP#              | SIO2^5        | SO2            |
| 25      | SPIHD          | HOLD#^6         | SIO3^7        | SO3            |

**Footnotes:**
1. An off-package flash can only be connected if the chip variant does not have in-package flash.
2. SPICSO is used to access flash
3. SI0: Serial Data Input and Output

**Footer:**
Espressif Systems  
ESP32-C61 Series Datasheet v0.5