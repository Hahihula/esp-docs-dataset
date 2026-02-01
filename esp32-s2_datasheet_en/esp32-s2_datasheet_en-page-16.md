**Title:**
2 Pins

**Subtitle:**
2.3 IO Pins

**Subsection Title:**
2.3.1 IO MUX Functions

**Body Text:**
The IO MUX allows multiple input/output signals to be connected to a single input/output pin. Each IO pin of ESP32-S2 can be connected to one of the five signals (IO MUX functions, i.e., FO-F4), as listed in Table 2-3 IO MUX Functions.

Among the five sets of signals:
- Some are routed via the GPIO Matrix (GPIO0, GPIO1, etc.), which incorporates internal signal routing circuitry for mapping signals programmatically. It gives the pin access to almost any peripheral signals. However, the flexibility of programmatic mapping comes at a cost as it might affect the latency of routed signals. For details about connecting to peripheral signals via GPIO Matrix, see ESP32-S2 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.
- Some are directly routed from certain peripherals (U0TXD, MTCK, etc.), including UARTO/1, JTAG, SPI0/1, and SPI2 - see Table 2-2 Peripheral Signals Routed via IO MUX.

**Table Title:**
Table 2-2. Peripheral Signals Routed via IO MUX

| Pin Function | Signal    | Description                                                                 |
|--------------|-----------|-----------------------------------------------------------------------------|
| U...TXD      | Transmit data |UARTO/1 interface                                                            |
| U...RXD      | Receive data |UARTO/1 interface                                                            |
| U...RTS      | Request to send |UARTO/1 interface                                                            |
| U...CTS      | Clear to send |UARTO/1 interface                                                            |
| MTCK         | Test clock  |                                                                              |
| MTD0         | Test Data Out |JTAG interface for debugging                                                 |
| MTDI         | Test Data In  |                                                                              |
| MTMS         | Test Mode Select |                                                                            |
| SPIQ         | Master in, slave out |3.3 V SPIO/1 interface for connection to in-package or off-package flash/PSRAM via the SPI bus. It supports 1-, 2-, 4-line SPI modes. See also Section 2.6 Pin Mapping Between Chip and Flash/PSRAM |
| SPID         | Master out, slave in |                                                                            |
| SPIHD        | Hold       |                                                                            |
| SPIWP        | Write protect |                                                                            |
| SPICLK       | Clock      |                                                                            |
| SPICS...     | Chip select |                                                                            |
| SPIIO...     | Data       |The higher 4 bits data line interface and DQS interface for 3.3 V SPIO/1 interface in 8-line SPI mode|
| SUBSPIQ      | Master in, slave out |1.8 V SPI0/1 interface for connection to in-package or off-package flash/PSRAM via the SUBSPI bus. It supports 1-, 2-, 4-line SPI modes |
| SUBSPID      | Master out, slave in |                                                                            |
| SUBSPIHD     | Hold       |                                                                            |
| SUBSPIWP     | Write protect |                                                                            |
| SUBSPICLK    | Clock      |                                                                            |
| SUBSPICS...  | Chip select |                                                                            |
| FSPIQ        | Master in, slave out |2.4-line SPI modes. It supports 1-, 2-, 4-line SPI modes |
| FSPID        | Master out, slave in |                                                                            |
| FSPIHD       | Hold       |                                                                            |
| FSPIWP       | Write protect |                                                                            |
| FSPICLK      | Clock      |                                                                            |
| FSPICSO      | Chip select |                                                                            |
| FSPIO...     | Data       |The higher 4 bits data line interface and DQS interface for SPI2 interface in 8-line SPI mode|

**Footer:**
Espressif Systems
ESP32-S2 Series Datasheet v1.8

**Navigation Link:**
Submit Documentation Feedback