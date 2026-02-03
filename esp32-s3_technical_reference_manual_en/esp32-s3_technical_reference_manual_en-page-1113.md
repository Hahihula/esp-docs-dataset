**Title:**
Chapter 30 SPI Controller (SPI)

**Section Title:**
30.5.3 Bit Read/Write Order Control

**Subsection Heading: In master mode:**

- The bit order of the command, address and data sent by the GP-SPI master is controlled by `SPI_WR_BIT_ORDER`.
  
- The bit order of the data received by the master is controlled by `SPI_RD_BIT_ORDER`.

**Subsection Heading: In slave mode:**

- The bit order of the data sent by the GP-SPI slave is controlled by `SPI_WR_BIT_ORDER`.

- The bit order of the command, address and data received by the slave is controlled by `SPI_RD_BIT_ORDER`.

**Body Text:**
Table 30.5-5 shows the function of `SPI_RD/WR_BIT_ORDER`. In Table 30.5-5, FSPI Bus signals are used for description. The bit order of SPI3 Bus signals can be referred to Table 30.5-5.

**Footer Information:**
Espressif Systems
1113 ESP32-S3 TRM (Version 1.7)

**Navigation Links:**
GoBack, Submit Documentation Feedback