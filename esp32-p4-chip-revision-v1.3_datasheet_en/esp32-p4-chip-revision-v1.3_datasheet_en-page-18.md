**Title:**
2 Pins

**Subtitle:**
2.3 IO Pins

**Subsection Title:**
2.3.1 IO MUX Functions

**Body Text:**

The IO MUX allows multiple input/output signals to be connected to a single input/output pin. Each IO pin of ESP32-P4 can be connected to one of the four signals (IO MUX functions, i.e., FO-F3), as listed in Table 2-3.

Among the four sets of signals:

- Some are routed via the GPIO Matrix (GPIO0, GPIO1, etc.), which incorporates internal signal routing circuitry for mapping signals programmatically. It gives the pin access to almost any peripheral signals. However, the flexibility of programmatic mapping comes at a cost as it might affect the latency of routed signals.
  
- Some are directly routed from certain peripherals (UOTXD, MTCK, etc.), including UARTO, JTAG, and SPI2 - see Table 2-2 IO MUX Functions.

**Table Title:**
Table 2-2. Peripheral Signals Routed via IO MUX

| Pin Function | Signal         | Description                                                                 |
|--------------|---------------|-----------------------------------------------------------------------------|
| MTCK         | Test clock     | Description                                                                 |
| MTDO         | Test data out   | Description                                                                 |
| MTDI         | Test data in    | JTAG interface for debugging                                                |
| MTMS         | Test mode select| Description                                                                 |
| SPI2_HOLD_PAD | Hold           | 3.3 V SPI2 Interface which can operate in master and slave modes. The interface supports 1-line, 2-line, 4-line, and 8-line modes (the 8-line mode is supported only in the master mode).|
| SPI2_CS_PAD   | Chip select     | Description                                                                 |
| SPI2_D_PAD    | Data in         | Description                                                                 |
| SPI2_CK_PAD   | Clock           | Description                                                                 |
| SPI2_Q_PAD    | Data out        | Description                                                                 |
| SPI2_WP_PAD   | Write protect   | Description                                                                 |
| SPI2_IO...PAD  | Data           | The high 4-bit data line interface and the DQS interface for 3.3 V SPI2 interface in 8-line SPI mode|
| SPI2_DQS_PAD  | Data strobe/data mask | Description                                                                 |
| UARTO_TXD_PAD | Transmit data   | UART0 Interface                 |
| UARTO_RXD_PAD | Receive data    | Description                                                                 |
| REF_50M_CLK_PAD | 50 MHz reference clock output | Provides 50 MHz clock for internal and external modules|
| GMAC_PHY_RXD_PAD | Receive data line 0/1 | Description                                                                 |
| GMAC_PHY_RXER_PAD | Receive error   | Description                                                                 |
| GMAC_PHY_TXDV_PAD | Transmit data valid | RMII Ethernet PHY interface        |
| GMAC_PHY_TXER_PAD | Transmit error  | Description                                                                 |
| GMAC_PHY_TXEN_PAD | Transmit enable | Description                                                                 |
| GMAC_RMI2_CLK_PAD | RMI2 clock       | Description                                                                 |
| SD1_CDATA_PAD | Card data line 0-7 of SD1 | SDIO3.0 interface        |
| SD1_CCMD_PAD  | Card command of SD1 | Description                                                                 |

**Footer:**
Table 2-3 IO MUX Functions shows the IO MUX functions of IO pins.

Espressif Systems  
ESP32-P4 Series Datasheet v0.6

Submit Documentation Feedback