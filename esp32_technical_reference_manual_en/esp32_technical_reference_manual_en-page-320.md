Title: Chapter 19 UART Controller (UART)

Menu:
- GoBack

Table of contents with entries and corresponding details:

1. **UART_AT_CMD_CHAR_REG**
   - Description: AT escape sequence detection configuration
   - Address range in UDMA0, UDMA1 registers: 0x3FF40054 to 0x3FF6E054 (R/W)

2. **FIFO configuration**
   - **UART_FIFO_REG**: FIFO data register; Address ranges are 0x3FF40000 and 0x3FF6E000, R/W
   - **UART_MEM_CONF_REG**: UART threshold and allocation configuration; Address range is 0x3FF40058 to 0x3FF6E058 (R/W)
   - **UART_MEM_CNT_STATUS_REG**: Receive and transmit memory configuration; Address ranges are 0x3FF40064, R/O

3. **Interrupt registers**
   - **UART_INT_RAW_REG**: Raw interrupt status
     - Address range in UDMA1 register: 0x3FF50004 to 0x3FF6E004 (R/W)
   - **UART_INT_ST_REG**: Masked interrupt status; Address ranges are 0x3FF40008, R/O
   - **UART_INT_ENA_REG**: Interrupt enable bits; Address range in UDMA1 register: 0x3FF5000C to 0x3FF6E00C (R/W)
   - **UART_INT_CLR_REG**: Interrupt clear bits; Address ranges are 0x3FF40010, W/O

Subtitle:
- Section Title: "19.4.2 UHCI Register Summary"

Body Text:

The addresses in this section are relative to the UDMA base address provided in Table 3.3-6 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

Table:
- **Name**: Configuration registers
  - **Description**: UART and frame separation config; Address ranges: 0x3FF54000 to 0x3FF4C000 (R/W)
  - **UDMA0, UDMA1**: Access types

- **Name**: UHCI_CONFO_REG
  - **Description**: UHCI config register; Address range in UDMA2: 0x3FF5402C to 0x3FF4C02C (R/W)

- **Name**: UHCI_CONF1_REG
  - **Description**: Escape characters configuration; Address ranges are 0x3FF54064, R/W

- **Name**: UHCI_ESCAPES_CONF_REG
  - **Description**: Timeout configuration; Address range in UDMA2: 0x3FF54068 to 0x3FF4C068 (R/W)

- **Name**: UHCI_HUNG_CONF_REG
  - **Description**: Escape sequence configuration register O; Address ranges are 0x3FF540B0, R/W

- **Name**: UHCI_ESC_CONFO_REG
  - **Description**: Escape sequence configuration register I (1); Address range in UDMA2: 0x3FF540B8 to 0x3FF4C0B8 (R/W)

- **Name**: UHCI_ESC_CONF2_REG
  - **Description**: Escape sequence configuration register II; Address ranges are 0x3FF540BC, R/W

- **Name**: UHCI_ESC_CONF3_REG
  - **Description**: Escape sequence configuration register III (3); Address range in UDMA1: 0x3FF540B8 to 0x3FF4C0B8 (R/W)

Subtitle:
- DMA configuration:

Table with entries and corresponding details for DMA configuration registers.

Footer Information:
- Company Name: Espressif Systems
- Document Version: ESP32 TRM (Version 5.6)
- Page Number: 320

Button:
- Submit Documentation Feedback