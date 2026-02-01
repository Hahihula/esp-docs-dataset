**Title: Pins**

---

### **2.3 IO Pins**

For details on configuring IO pins, see [ESP32-C5 Technical Reference Manual > Chapter IO MUX and GPIO Matrix (GPIO, IO MUX)](#).

#### 2.3.1 IO MUX Functions

The IO MUX allows multiple input/output signals to be connected to a single input/output pin. Each IO pin of ESP32-C5 can be connected to one of the three signals (IO MUX functions, i.e., FO-F2), as listed in Table 2-3 [IO MUX Pin Functions](#).

Among the three sets of signals:

- Some are routed via the GPIO Matrix (GPIO0, GPIO1, etc.), which incorporates internal signal routing circuitry for mapping signals programmatically. It gives the pin access to almost any peripheral signals.
- However, the flexibility of programmatic mapping comes at a cost as it might affect the latency of routed signals.

For details about connecting to peripheral signals via GPIO Matrix, see [ESP32-C5 Technical Reference Manual > Chapter IO MUX and GPIO Matrix](#).

- Some are directly routed from certain peripherals (UOTXD, MTCK, etc.), including UARTO, JTAG, SPI0/1, and SPI2 - see Table 2-2 Peripheral Signals Routed via IO MUX.

**Table 2-2. Peripheral Signals Routed via IO MUX**

| Pin Function | Signal       | Description                                    |
|--------------|-------------|------------------------------------------------|
| UOTXD        | Transmit data | UARTO interface                                |
| UORXD        | Receive data | UARTO interface                                |
| MTCK         | Test clock   |                                               |
| MDIO         | Data Out     | JTAG interface for debugging                   |
| MTDI         | Test Data In  |                                               |
| MTMS         | Test Mode Select |                                               |
| SPIQ         | Master in, slave out |                                               |
| SPID         | Master out, slave in |                                               |
| SPIHD        | Hold         | SPI0/1 interface for connection to the off-package flash via SPI bus. |
| SPIWP        | Write protect |                                               |
| SPICLK       | Clock        |                                               |
| SPICS...     | Chip select  |                                               |
| FSPIQ        | Master in, slave out |                                               |
| FSPID        | Master out, slave in |                                               |
| FSPIHD      | Hold         | SPI2 main interface for fast SPI connection. Among these pins, FSPICSO is for input or output signals in master or slave mode |
| FSPIWP       | Write protect |                                               |
| FSPICLK      | Clock        |                                               |
| FSPICS0      | Chip select  |                                               |
| SDIO_CLK     | Clock        | SDIO interface for connection to external SDIO hosts |
| SDIO_CMD     | Command      |                                               |
| SDIO_DATA... | Data         |                                               |

---

Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32-C5 Series Datasheet v1.0