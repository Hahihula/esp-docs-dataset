**1 Module Overview**

### Operating Conditions

- **Operating voltage/Power supply:** 3.0 ~ 3.6 V
- Test: Green certification; RoHS/REACH
- **Operating ambient temperature:** -40 ~ 105 °C
- HTOL/HTSL/uHAST/TCT/ESD

### Certification

- RF certification (See [certificates](#))

**1.2 Series Comparison**

ESP8685-WROOM-01 is a powerful, generic Wi-Fi and Bluetooth LE module that has a rich set of peripherals.
This module is an ideal choice for smart homes, industrial automation, health care, consumer electronics,
etc.

ESP8685-WROOM-01 comes with an on-board PCB antenna. It can be mounted onto the surface of a PCB board, or connected to a PCB board via pin headers.

The series comparison for ESP8685-WROOM-01 is as follows:

| Ordering Code | Flash         | Ambient Temp. (°C) | Size^2 (mm) |
|----------------|---------------|--------------------|-------------|
| ESP8685-WROOM-01-H4 | 4 MB (Quad SPI)^3, ^4 | -40 ~ 105 | 16.0 x 24.0 x 3.1 |

1. Ambient temperature specifies the recommended temperature range of the environment immediately outside the Espressif module.
2. For details, refer to Section [10 Module Dimensions](#).
3. The flash is in the chip package. For specifications, refer to Section [6.5 Memory Specifications](#).
4. By default, the SPI flash on the module operates at a maximum clock frequency of 80 MHz and does not support auto suspend feature.
   - If you have a requirement for higher flash clock frequency or need the flash auto suspend feature, please contact us.

At the core of this module is the ESP8685H4 chip. ESP8685 series chips are designed with an integrated 32-bit RISC-V single-core processor that integrates various peripherals such as UART, I2C, I2S, remote control peripheral, LED PWM controller, general DMA controller, TWAI® controller, USB Serial/JTAG controller, temperature sensor, and ADC.

**Note:**
For more information on ESP8685 chip series, please refer to [ESP8685 Series Datasheet](#).

### 1.3 Applications

Espressif Systems
[Submit Documentation Feedback](#)  
ESP8685-WROOM-01 Datasheet v1.5