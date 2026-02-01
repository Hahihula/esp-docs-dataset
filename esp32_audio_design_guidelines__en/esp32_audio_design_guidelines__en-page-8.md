**Title:**
1. Schematic Design

**Figure Caption and Diagram Description:**
- **Figure Title:** Figure 1-6. Reference Circuit for Part of ESP32 Pin Configuration.
- The diagram shows a schematic design with various components labeled, including "Button Array, ADC R18" connected to "SENSOR_VP," as well as connections between different pins like "ESP_VDD33."

**Subsection Title:**
1.3.4. Dedicated Pins

**Body Text:**

SHD/SD2, SWP/SD3, SCS/CMD, SCK/CLK, SDO/SDO, and SDI/SD1 used for connecting SPI Flash integrated within the module are not recommended for other functions.

If ESP32-WROVER series modules are selected, GPIO16 is reserved as the chip selection pin and GPIO17 as clock of PSRAM within the module; so these two GPIOs are not recommended for other functions. TXD0/RXD0 are UART0 pins used for flashing and communication; they are not recommended for other functions.

**Note:**
ESP32 cannot identify USB directly, so a USB to UART chip is needed in your design such as CP1202-GM. The UART pin of the chip is connected with the UART0 pin of ESP32 which can be used to flash programs to ESP32 and serves an interactive interface with the PC.

In your design it's recommended to reserve test points for TXD0 and RXD0.
For example:

**Footer:**
Espressif
5/19
2019.01