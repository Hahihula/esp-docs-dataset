**Title:**
2 Pins

**Subtitle:**
2.3 IO Pins

**Subsection Title:**
2.3.1 IO MUX Pin Functions

**Body Text:**
The IO MUX allows multiple input/output signals to be connected to a single input/output pin. Each IO pin of ESP32-C6 can be connected to one of the three signals (IO MUX functions, i.e., FO-F2), as listed in Table 2-4 QFN40 IO MUX Pin Functions and Table 2-5 QFN32 IO MUX Pin Functions.

Among the three sets of signals:

- Some are routed via the GPIO Matrix (GPIO0, GPIO1, etc.), which incorporates internal signal routing circuitry for mapping signals programmatically. It gives the pin access to almost any peripheral signals. However, the flexibility of programmatic mapping comes at a cost as it might affect the latency of routed signals. For details about connecting to peripheral signals via GPIO Matrix, see ESP32-C6 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.
- Some are directly routed from certain peripherals (UOTXD, MTCK, etc.), including UARTO, JTAG, SPI0/1, SPI2, and SDIO - see Table 2-3 Peripheral Signals Routed via IO MUX.

**Table Title:**
Table 2-3. Peripheral Signals Routed via IO MUX

| Pin Function | Signal       | Description                                |
|--------------|-------------|--------------------------------------------|
| UOTXD        | Transmit data | UARTO interface                            |
| UORXD        | Receive data |                                            |
| MTCK         | Test clock   |                                            |
| MDIO         | Test Data Out | JTAG interface for debugging                |
| MTDI         | Test Data In  |                                            |
| MTMS         | Test Mode Select |                                            |
| SPIQ         | Master in, slave out | 3.3 V SPI0/1 interface for connection to in-package or off-package flash via the SPI bus. It supports 1-, 2-, 4-line SPI modes. See also Section 2.6 Pin Mapping Between Chip and Flash |
| SPID         | Master out, slave in |                                            |
| SPIHD        | Hold        |                                            |
| SPIWP        | Write protect |                                            |
| SPICLK       | Clock       |                                            |
| SPICS0       | Chip select  |                                            |
| FSPIQ        | Master in, slave out |                                            |
| FSPID        | Master out, slave in | SPI2 interface for fast SPI connection. It supports 1-, 2-, 4-line SPI modes |
| FSPIWP       | Write protect |                                            |
| FSPICLK      | Clock       |                                            |
| FSPICS...    | Chip select  |                                            |
| SDIO_CMD     | Command     | SDIO interface                             |
| SDIO_CLK     | Clock       |                                            |
| SDIO_DATA... | Data        |                                            |

**Footer:**
Table 2-4 QFN40 IO MUX Pin Functions or Table 2-5 QFN32 IO MUX Pin Functions shows the IO MUX functions of IO pins.

Espressif Systems
ESP32-C6 Series Datasheet v1.4

Submit Documentation Feedback