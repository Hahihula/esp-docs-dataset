**Title:**
2 Pins

**Subtitle:**
2.3 IO Pins

**Subsection Title:**
2.3.1 IO MUX Functions

**Body Text:**
The IO MUX allows multiple input/output signals to be connected to a single input/output pin. Each IO pin of ESP32-C61 can be connected to one of the three signals (IO MUX functions, i.e., F0–F2), as listed in Table 2-3.

**Subsection Text:**
Among the three sets of signals:

- Some are routed via the GPIO Matrix (GPIOO, GPI01, etc.), which incorporates internal signal routing circuitry for mapping signals programmatically. It gives the pin access to almost any peripheral signals. However, the flexibility of programmatic mapping comes at a cost as it might affect the latency of routed signals.
  
- Some are directly routed from certain peripherals (UOTXD, MTCK, etc.), including UARTO, JTAG, SPI0/1, SPI2 and SDIO 2.0 Slave - See Table 2-2 IO MUX Functions.

**Table Title:**
Table 2-2. Peripheral Signals Routed via IO MUX

| Pin Function | Signal       | Description                                    |
|--------------|-------------|------------------------------------------------|
| UOTXD        | Transmit data | UARTO interface                                |
| UORXD        | Receive data |                                              |
| MTCK         | Test clock   |                                              |
| MTDO         | Test data out | JTAG interface for debugging                   |
| MTDI         | Test data in  |                                              |
| MTMS         | Test mode select |                                              |
| SPIQ         | Data out     | 3.3 V SPIO/1 interface for connection to in-package or off-package flash/PSRAM via the SPI bus. It supports 1-, 2-, 4-line SPI modes. See also Section 2.6 Pin Mapping Between Chip and Flash/PSRAM |
| SPIID        | Data in      |                                              |
| SPIHD        | Hold         |                                              |
| SPIWP        | Write protect |                                              |
| SPICLK       | Clock        |                                              |
| SPICS...     | Chip select   |                                              |
| FSPIQ        | Data out     |                                              |
| FSPID        | Data in      |                                              |
| FSPIHD       | Hold         | SPI2 interface for fast SPI connection. It supports 1-, 2-, 4-line SPI modes |
| FSPIWP       | Write protect |                                              |
| FSPICLK      | Clock        |                                              |
| FSPICSO      | Chip select   |                                              |
| SDIO_CLK     | Clock        | The Secure Digital Input Output (SDIO) interface for connecting to an external SDIO host |
| SDIO_CMD     | Command      |                                              |
| SDIO_DATA... | Data         |                                              |

**Table Title:**
Table 2-3. IO MUX Pin Functions

| Pin No. | IO MUX / F0 | IO MUX Function Type (F1) | IO MUX Function Type (F2) | Type |
|---------|-------------|---------------------------|----------------------------|-------|
| 6       | XTAL_32K_P | GPIOO                      | I/O/T                       | Cont'd on next page |

**Footer:**
Espressif Systems
ESP32-C61 Series Datasheet v0.5

Page number:
17