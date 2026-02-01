**Title:**
2 Pins

**Subtitle:**
2.3 IO Pins

**Subsection Title:**
2.3.1 IO MUX Functions

**Body Text:**
The IO MUX allows multiple input/output signals to be connected to a single input/output pin. Each IO pin of ESP32-S3 can be connected to one of the five signals (IO MUX functions, i.e., FO-F4), as listed in Table 2-4 IO MUX Functions.

Among the five sets of signals:
- Some are routed via the GPIO Matrix (GPIO0, GPIO1, etc.), which incorporates internal signal routing circuitry for mapping signals programmatically. It gives the pin access to almost any peripheral signals. However, the flexibility of programmatic mapping comes at a cost as it might affect the latency of routed signals. For details about connecting to peripheral signals via GPIO Mux, see ESP32-S3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.
- Some are directly routed from certain peripherals (UOTXD, MTCK, etc.), including UARTO/1, JTAG, SPI0/1, and SPI2 - see Table 2-3 Peripheral Signals Routed via IO MUX.

**Table Title:**
Table 2-3. Peripheral Signals Routed via IO MUX

| Pin Function | Signal       | Description                                    |
|--------------|-------------|------------------------------------------------|
| U...TXD      | Transmit data | UARTO/1 interface                             |
| U...RXD      | Receive data |                                              |
| U...RTS      | Request to send |                                              |
| U...CTS      | Clear to send |                                              |
| MTCK         | Test clock   |                                              |
| MTD0         | Test Data Out | JTAG interface for debugging                   |
| MTDI         | Test Data In  |                                              |
| MTMS         | Test Mode Select |                                              |
| SPIQ         | Master in, slave out | SPI0/1 interface (powered by VDD_SPI) for connection to in-package or off-package flash/PSRAM via the SPI bus. It supports 1-, 2-, 4-line SPI modes. See also Section 2.6 Pin Mapping Between Chip and Flash/PSRAM |
| SPID         | Master out, slave in |                                              |
| SPIHD        | Hold        |                                              |
| SPIWP        | Write protect |                                              |
| SPICLK       | Clock       |                                              |
| SPICS...     | Chip select  |                                              |
| SPIIO...     | Data        | SPI0/1 interface (powered by VDD_SPI or VDD3P3_CPU) for the higher SPIDQS | Data strobe/data mask | 4 bits data line interface and DQS interface in 8-line SPI mode |
| SPICLK_N_DIFF| Negative clock signal | Differential clock negative/positive for the SPI bus |
| SPICLK_P_DIFF| Positive clock signal |                                              |
| SUBSPIQ      | Master in, slave out | SPI0/1 interface (powered by VDD3P3_RTC or VDD3V3_CPU) for connection to in-package or off-package flash/PSRAM via the SUBSPI bus. It supports 1-, 2-, 4-line SPI modes |
| SUBSPID      | Hold        |                                              |
| SUBSPIHD     | Write protect |                                              |
| SUBSPICLK    | Clock       |                                              |
| SUBSPICS...  | Chip select  |                                              |
| SUBSPICKL_N_DIFF| Negative clock signal | Differential clock negative/positive for the SUBSPI bus |
| SUBSPICKL_P_DIFF| Positive clock signal |                                              |

**Footer:**
Espressif Systems
20 ESP32-S3 Series Datasheet v2.1

**Link Texts in Table Description:**
- Chapter IO MUX and GPIO Matrix.
- Section 2.6 Pin Mapping Between Chip and Flash/PSRAM.

**Note:** The text "Cont'd on next page" indicates that the table continues onto another page, which is not shown here.