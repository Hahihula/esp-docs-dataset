**Chapter Title:**
Chapter 26 UART Controller (UART)

**Subsections and Lists with Descriptions:**

- **GoBack**: This is a clickable link or button.

- **Bullet Points under Chapter Header:**
  - UHCI_TX_START_INT: Triggered when GDMA detects a separator character.
  - UHCI_RX_START_INT: Triggered when a separator character has been sent.

**Section Title and Subsection with Content:**

26.5 Programming Procedures

26.5.1 Register Type
- **Body Text**: All UART registers are in APB_CLK domain. According to whether clock domain crossing and synchronization are required, UART registers that can be configured by software are classified into three types, namely synchronous registers, static registers, and immediate registers. Synchronous registers are read in Core Clock domain, and take effect after synchronization. Static registers are also read in Core Clock domain, but would not change dynamically. Therefore, for static registers, clock domain crossing is not required, and software can turn on or off the clock for the UART transmitter or receiver to ensure that the configuration sampled in Core Clock domain is correct. Immediate registers are read in APB_CLK domain, take effect after being configured via the APB bus.

26.5.1.1 Synchronous Registers
- **Body Text**: Since synchronous registers are read in core clock domain, but written in APB_CLK domain, they implement the clock domain crossing design to ensure that their values sampled in Core Clock domain are correct. These registers as listed in Table 26.5-1 are configured as follows:
  - Enable register synchronization by clearing UART_UPDATE_CTRL to 0;
  - Wait for UART_REG_UPDATE to become O, which indicates the completion of last synchronization;
  - Configure synchronous registers;
  - Synchronize the configured values to Core Clock domain by writing 1 to UART_REG_UPDATE.

**Table:**
- **Title**: Table 26.5-1. UART™ Synchronous Registers
- **Columns**: Register | Field
- **Rows (Example)**:
  - UART_CLKDIV_REG | UART_CLKDIV_FRAG[3:0]
  - UART_CLKDIV | [11:0]
  - UART_CONFO_REG | UART_AUTOBAUD_EN
  - ... (Additional fields continue in the table)

**Footer Information**: 
- Espressif Systems, Page number "938", Document version information "ESP32-S3 TRM (Version 1.7)".
- Link: Submit Documentation Feedback