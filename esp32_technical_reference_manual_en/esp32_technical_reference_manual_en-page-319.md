**Chapter Title:**
Chapter 19 UART Controller (UART)

**GoBack Link:** GoBack

---

### Configuration Registers and Related Information:

- **UART_CONF1_REG**
  - Description: Clock divider configuration register.
  - Offset: 0x3FF40024, 0x3FF50024
  - Size: 0x3FF6E024

- **UART_CLKDIV_REG**
  - Description: Clock divider configuration.
  - Offset: 0x3FF40014, 0x3FF50014
  - Size: 0x3FF6E014

- **UART_FLOW_CONF_REG**
  - Description: Software flow-control configuration register.
  - Offset: 0x3FF40034, 0x3FF50034
  - Size: 0x3FF6E034 (R/W)

- **UART_SWFC_CONF_REG**
  - Description: Software flow-control character configuration.
  - Offset: 0x3FF4003C, 0x3FF5003C
  - Size: 0x3FF6E03C

- **UART_SLEEP_CONF_REG**
  - Description: Sleep-mode configuration register.
  - Offset: 0x3FF40038, 0x3FF50038
  - Size: 0x3FF6E038 (R/W)

- **UART_IDLE_CONF_REG**
  - Description: Frame-end idle configuration register.
  - Offset: 0x3FF40040, 0x3FF50040
  - Size: 0x3FF6E040

- **UART_RS485_CONF_REG**
  - Description: RS485 mode configuration register.
  - Offset: 0x3FF40044, 0x3FF50044
  - Size: 0x3FF6E044 (R/W)

---

### Status Registers:

- **UART_STATUS_REG**
  - Description: UART status register.
  - Offset: 0x3FF4001C, 0x3FF5001C
  - Size: 0x3FF6E01C

- **UART_MEM_TX_STATUS_REG**
  - Description: TX FIFO write and read offset address.
  - Offset: 0x3FF4005C, 0x3FF5005C
  - Size: 0x3FF6E05C (RO)

- **UART_MEM_RX_STATUS_REG**
  - Description: RX FIFO write and read offset address.
  - Offset: 0x3FF40060, 0x3FF50060
  - Size: 0x3FF6E060

---

### Autobaud Registers:

- **UART_AUTOBAUD_REG**
  - Description: Autobaud configuration register.
  - Offset: 0x3FF40018, 0x3FF50018
  - Size: 0x3FF6E018

- **UART_LOWPULSE_REG**
  - Description: Autobaud minimum low pulse duration register.
  - Offset: 0x3FF40028, 0x3FF50028
  - Size: 0x3FF6E028 (RO)

- **UART_HIGHPULSE_REG**
  - Description: Autobaud minimum high pulse duration register.
  - Offset: 0x3FF4002C, 0x3FF5002C
  - Size: 0x3FF6E02C

- **UART_POSPULSE_REG**
  - Description: Autobaud high pulse register.
  - Offset: 0x3FF40068, 0x3FF50068
  - Size: 0x3FF6E068 (RO)

- **UART_NEGPULSE_REG**
  - Description: Autobaud low pulse register.
  - Offset: 0x3FF4006C, 0x3FF5006C
  - Size: 0x3FF6E06C

- **UART_RXD_CNT_REG**
  - Description: Autobaud edge change count register.
  - Offset: 0x3FF40030, 0x3FF50030
  - Size: 0x3FF6E030 (RO)

---

### AT Escape Sequence Detection Configuration:

- **UART_AT_CMD_PRECNT_REG**
  - Description: Pre-sequence timing configuration.
  - Offset: 0x3FF40048, 0x3FF50048
  - Size: 0x3FF6E048 (R/W)

- **UART_AT_CMD_POSTCNT_REG**
  - Description: Post-sequence timing configuration.
  - Offset: 0x3FF4004C, 0x3FF5004C
  - Size: 0x3FF6E04C

- **UART_AT_CMD_GAPOUT_REG**
  - Description: Timeout configuration.
  - Offset: 0x3FF40050, 0x3FF50050
  - Size: 0x3FF6E050 (R/W)

---

**Footer Information:**  
Espressif Systems  
Page Number: 319  
Document Title: ESP32 TRM (Version 5.6)  
Link Texts:
- Submit Documentation Feedback