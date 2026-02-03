**Title: Chapter 30 SPI Controller (SPI)**

---

### Table of Contents:
- Quad Output Read
- Octal I/O Read
- QPI
- OPI

#### Subtitle: Introduction to FSPI Bus and SPI3 Bus Signals

Functional description of FSPI/SPI3 bus signals is shown in **Table 30.5-2**.

---

### Table Title (Subtitle): 
**Table 30.5-2. Functional Description of FSPI/SPI3 Bus Signals**

| FSPI Bus Signal | SPi3 Bus Signal | Function |
|------------------|-----------------|----------|
| FSPICLK         | SPI3_CLK        | Input and output clock in master/slave mode |
| FSPICS0         | SPI3_CS0        | Input and output CS signal in master/slave mode |
| FSPICS1 ~ 5     | SPI3_CS1 ~ 2    | Output CS signal in master mode |
| FSPIID          | SPI3_D          | MOSI/SI0 (serial data input and output, bit0) |
| FSPIQ           | SPI3_Q          | MISO/SI1 (serial data input and output, bit1) |
| FSPIWWP         | SPI3_WP         | SI02 (serial data input and output, bit2) |
| FSPIHD          | SPI3_HD         | SI03 (serial data input and output, bit3) |
| FSPII04 ~ 7     | SI04 ~ 7        | serial data input and output, bit4 ~ 7) |
| FSPIDQS         |                | Output data mask signal in master mode |

---

**Footer:**
- Espressif Systems
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback