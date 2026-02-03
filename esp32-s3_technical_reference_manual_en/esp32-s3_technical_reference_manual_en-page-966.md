**Title:**
Chapter 26 UART Controller (UART)

**Menu:**
GoBack

---

**Section Title:**
UART_DATE Register 26.32. UART_DATE_REG (0x007C)

**Body Text:**
- **Field Name:** UART_DATE
- **Description:** This is the version control register.
- **Access Mode:** (R/W)
- **Address:** 0x2008270

---

**Section Title:**
Register 26.33. UART_ID_REG (0x0080)

**Body Text:**

| Field Name | Description |
|------------|-------------|
| UART_ID    | This field is used to configure the UART_ID. (R/W) |
| UART_UPDATE_CTRL | This bit is used to control register synchronization mode. 0: After registers are configured, software needs to write 1 to UART_REG_UPDATE to synchronize registers; 1: Registers are automatically synchronized into UART Core’s clock domain. (R/W) |
| UART_REG_UPDATE | When this bit is set to 1 by software, registers are synchronized to UART Core's clock domain. This bit is cleared by hardware after synchronization is done. (R/W/SC) |

---

**Subsection Title:**
26.7.2 UHCI Registers

**Body Text:**
The addresses in this section are relative to UHCI Controller base address provided in Table 4.3-3 in Chapter 4 System and Memory.

---

**Footer Information:**
Espressif Systems
966 ESP32-S3 TRM (Version 1.7)

**Link:** Submit Documentation Feedback