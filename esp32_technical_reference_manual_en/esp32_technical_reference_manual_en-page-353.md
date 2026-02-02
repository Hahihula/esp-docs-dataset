**Chapter Title:**
Chapter 19 UART Controller (UART)

**Register Information for Register 19.51, UHCI_HUNG_CONF_REG (0x68):**

- **Field Descriptions and Values in Binary:**
  - `31` to `24`: Reserved bits.
  - `23`: UHCI_RXFIFO_TIMEOUT_ENA
    - Description: This is the enable bit for DMA send-data timeout. (R/W)
  - `22`: UHCI_TXFIFO_TIMEOUT_ENA
    - Description: The enable bit for Tx FIFO receive-data timeout. (R/W)
  - `21`: UHCI_RXFIFO_TIMEOUT_SHIFT
    - Description: This register stores the timeout value. When DMA takes more time to read data from RAM than what this register indicates, it will produce the UHCI_RX_HUNG_INT interrupt.
  - `20`: UHCI_TXFIFO_TIMEOUT_SHIFT
    - Description: The tick count is cleared when its value is equal to or greater than (17’d8000»reg_rx_fifo_timeout_shift). (R/W)
  - `19`: Reserved bits with binary values of `0`.
  - `12` to `11`: UHCI_TXFIFO_TIMEOUT_ENA
    - Description: The enable bit for Tx FIFO receive-data timeout. (R/W)
  - `10` and `8`: UHCI_RXFIFO_TIMEOUT_ENA, respectively.
  - `7`: Reserved bits with binary values of `0`.
  - `6`: Reserved bits with binary value of `0`.
  - `5`: Reserved bits with binary value of `0`.
  - `4`: Reserved bits with binary value of `0`.
  - `3`: UHCI_TXFIFO_TIMEOUT_SHIFT
    - Description: The tick count is cleared when its value is equal to or greater than (17’d8000»reg_tx_fifo_timeout_shift). (R/W)
  - `2`: Reserved bits.
  - `1`: Reserved bits with binary values of `0`.
  - `0`: Reset bit.

**Register Information for Register 19.52, UHCI_ESC_CONF_n (n: 0-3) (0x80+4*n):**

- **Field Descriptions and Values in Binary:**
  - `31` to `24`: Reserved bits.
  - `23`: UHCI_ESC_SEQ2_CHA1
    - Description: This register stores the second char used to replace the reg_esc_seq2 in data. (R/W)
  - `22`: UHCI_ESC_SEQ2_CHARO
    - Description: This register stores the first char used to replace the reg_esc_seq2 in data.
  - `16` and `15`: Reserved bits with binary values of `0`.
  - `8` to `7`: UHCI_ESC_SEQ2_CHA0, respectively.

- **Field Descriptions for Specific Registers:**
  - `31`: Reserved bit (Reset).
  - `24`: Reserved.
  - `23`: UHCI_ESC_SEQ2_CHA1
    - Description: This register stores the second char used to replace the reg_esc_seq2 in data. (R/W)
  - `22`: UHCI_ESC_SEQ2_CHARO
    - Description: This register stores the first char used to replace the reg_esc_seq2 in data.
  - `16` and `15`: Reserved bits with binary values of `0`.
  - `8` to `7`: UHCI_ESC_SEQ2_CHA0, respectively.

**Footer Information:**
- Page number: 353
- Document version: ESP32 TRM (Version 5.6)
- Company name and link for feedback submission:
  - Espressif Systems
  - Submit Documentation Feedback

**Navigation Link:** GoBack