**Title:**
2 Pins

**Subtitle:**
2.3 IO Pins

**Subsection Title:**
2.3.1 IO MUX Functions

**Body Text:**
The IO MUX allows multiple input/output signals to be connected to a single input/output pin. Each IO pin of ESP32-C3 can be connected to one of the three signals (IO MUX functions, i.e., F0-F2), as listed in Table 2-4.

**Link Text:**
IO MUX Pin Functions

**List Description:**
Among the three sets of signals:
- Some are routed via the GPIO Matrix (GPIO0, GPIO1, etc.), which incorporates internal signal routing circuitry for mapping signals programmatically. It gives the pin access to almost any peripheral signals. However, the flexibility of programmatic mapping comes at a cost as it might affect the latency of routed signals. For details about connecting to peripheral signals via GPIO Matrix, see ESP32-C3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.
- Some are directly routed from certain peripherals (UOTXD, MTCK, etc.), including UARTO, JTAG, SPI0/1, and SPI2 - see Table 2-3 Peripheral Signals Routed via IO MUX.

**Table Title:**
Table 2-3. Peripheral Signals Routed via IO MUX

| Pin Function | Signal       | Description                                    |
|--------------|-------------|------------------------------------------------|
| UOTXD        | Transmit data | UARTO interface                                |
| UORXD        | Receive data |                                              |
| MTCK         | Test clock   |                                              |
| MDIO         | Test Data Out | JTAG interface for debugging                   |
| MTDI         | Test Data In  |                                              |
| MTMS         | Test Mode Select |                                              |
| SPIQ         | Master in, slave out |                                              |
| SPID         | Master out, slave in | 3.3 V SPI0/1 interface for connection to in-package or off-package flash via the SPI bus. It supports 1-, 2-, 4-line SPI modes. See also Section 2.6 Pin Mapping Between Chip and Flash |
| SPIHD        | Hold        |                                              |
| SPIWP        | Write protect |                                              |
| SPICLK       | Clock       |                                              |
| SPICS...     | Chip select  |                                              |

**Table Title:**
Table 2-4. IO MUX Pin Functions

| Pin No. | IO MUX / F0 | IO MUX Function Type (1, 2, 3) | GPIO Name | Type |
|---------|-------------|----------------------------------|-----------|------|
| 4       | GPIOO       | I/O/T                            |           |      |

**Footer:**
Espressif Systems
ESP32-C3 Series Datasheet v2.2

**Note at the bottom of page:** 
Submit Documentation Feedback