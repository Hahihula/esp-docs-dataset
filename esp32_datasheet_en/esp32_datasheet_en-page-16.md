**Table:**

| Name | No. | Type | Function |
|------|-----|------|----------|
| CAP1 | 48  | I    | Connects to a 10 nF series capacitor to ground |
| GND | 49  | P    | Ground |

---

**Notes for Table 2-1 Pin Overview:**

1. Function names:
   - CLK_OUT... clock output
   - SPICLK
   - HSPICLK
   - VSPICLK
   - HS..._CLK SDIO Master clock signal
   - SD_CLK SDIO Slave clock signal
   - EMAC_TX_CLK EMAC clock signal
   - EMAC_RX_CLK
   - U..._RTS UARTO/1/2 hardware flow control signals
   - U..._CTS
   - U..._RXD UARTO/1/2 receive/transmit signals
   - U..._TXD
   - MTMS
   - MTDI JTAG interface signals
   - MTCK
   - MTDO GPIO... General-purpose input/output with signals routed via the GPIO matrix. For more details on the GPIO matrix, see [ESP32 Technical Reference Manual](#) Chapter IO MUX and GPIO Matrix.

2. Regarding highlighted cells, see Section 2.3.1 Restrictions for GPIOs and RTC_GPIOs.
   
3. For a quick reference guide to using the IO_MUX, Ethernet MAC, and GPIO Matrix pins of ESP32, please refer to Appendix [ESP32 Pin Lists](#).