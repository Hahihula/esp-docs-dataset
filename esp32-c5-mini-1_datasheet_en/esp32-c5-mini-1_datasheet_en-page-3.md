**1 Module Overview**

### IEEE 802.15.4

- Compliant with IEEE 802.15.4-2015 protocol
- OQPSK PHY in 2.4 GHz band
- Data rate: 250 Kbps
- Thread 1.4
- Zigbee 3.0

### Integrated Components on Module

- 48 MHz crystal oscillator
- SPI flash

### Antenna Options

- On-board PCB antenna

### Operating Conditions

- Operating voltage/Power supply: 3.0 ~ 3.6 V
- Operating ambient temperature: -40 ~ 85 °C

### Peripherals

- GPIO, SPI, parallel IO interface, UART, I2C, I2S, RMT (TX/RX), pulse counter, LED PWM, USB Serial/JTAG controller, MCPWM, GDMA, CAN FD controller, SDIO slave controller, BitScrambler, event task matrix, ADC, temperature sensor, brownout detector, analog voltage comparator, system timer, general-purpose timers, RTC timer, watchdog timers, etc.

### Certification

- RF certification: See [certificates](#)
- Green certification: RoHS/REACH Test
  - HTOL/HTSL/uHAST/TCT/ESD

### Series Comparison (1.2)

ESP32-C5-MINI-1 modules are powerful, generic Wi-Fi MCUs that have a rich set of peripherals. They are an ideal choice for a wide variety of application scenarios related to Internet of Things (IoT), such as embedded systems, smart home, wearable electronics, etc.

ESP32-C5-MINI-1 comes with a PCB antenna.
The ordering information for the modules is as follows:

**Table 1-1. ESP32-C5-MINI-1 (ANT) Series Comparison**

| Part Number | Flash^1,2 | Ambient Temp.^3 | Embedded Chip^4 | Size^4 |
|-------------|-----------|------------------|------------------|--------|
| ESP32-C5-MINI-1-N4 | 4 MB (Quad SPI) | -40 ~ 85 °C | ESP32-C5NF4 | 15.4 x 21.3 x 2.4 mm |

1 For specifications, refer to Section 6.5 Memory Specifications.
2 By default, the SPI flash on the module operates at a maximum clock frequency of 80 MHz and does not support the auto suspend feature. If you have a requirement for a higher flash clock frequency of 120 MHz or if you need the flash auto suspend feature, please contact us.
3 Ambient temperature specifies the recommended temperature range of the environment immediately outside the Espressif module.
4 For details, refer to Section 10 Module Dimensions.

Espressif Systems  
ESP32-C5-MINI-1 Datasheet v1.0

[Submit Documentation Feedback](#)