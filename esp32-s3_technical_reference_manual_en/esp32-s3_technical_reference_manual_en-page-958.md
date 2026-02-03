**Chapter Title:**
Chapter 26 UART Controller (UART)

**Section Header:**
Register 26.11. UART_FLOW_CONF_REG (0x0034)

**Binary Register Diagram Description:**
- The diagram shows a binary register with various bits labeled, such as UART_SEND_XON, UARTFORCE_XON, and others.
- Each bit is represented by either '1' or '0'.

**Text Descriptions for Bits in the Binary Register:**

1. **UART_SW_FLOW_CON_EN**: Set this bit to enable software flow control. When UART receives flow control characters XON or XOFF, which can be configured by UART_XON_CHAR or UART_XOFF_CHAR respectively, UART_SW_XON_INT or UART_SW_XOFF_INT interrupts can be triggered if enabled.
   - (R/W)

2. **UART_XONOFF_DEL**: Set this bit to remove flow control characters from the received data.
   - (R/W)

3. **UART FORCE XON**:
   - Set this bit to force the transmitter to send data.

4. **UART FORCE XOFF**:
   - Set this bit to stop the transmitter from sending data.
   - (R/W)

5. **UART_SEND_XON**: 
   - Set this bit to send an XON character. This bit is cleared by hardware automatically.
   - (R/W/SS/SC)

6. **UART_SEND_XOFF**:
   - Set this bit to send an XOFF character. This bit is cleared by hardware automatically.

**Section Header:**
Register 26.12. UART_SLEEP_CONF_REG (0x0038)

**Binary Register Diagram Description for the Second Register:**

- The diagram shows a binary register with various bits labeled, such as UART_ACTIVE_THRESHOLD.
- Each bit is represented by either '1' or '0'.

**Text Descriptions for Bits in the Binary Register of the second section:**

7. **UART_ACTIVE_THRESHOLD**: UART is activated from Light-sleep mode when the input RXD edge changes more times than the value of this field plus 3.

**Footer Information:**
- Page number and document version information:
   - "958 ESP32-S3 TRM (Version 1.7)"
- Company name at bottom left corner.
- Links for submitting documentation feedback are provided but not described in detail here as per the instructions to avoid mentioning them explicitly.

**Navigation Link:**
- There is a link labeled "GoBack" which likely navigates back from this page within the document or application interface, though it's just text and no further details about its functionality.