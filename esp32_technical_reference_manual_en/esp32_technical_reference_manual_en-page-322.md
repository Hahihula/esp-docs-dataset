**Title:**
Chapter 19 UART Controller (UART)

**Section Title:**
19.5 Registers

**Subsection Title and Content:**
19.5.1 UART Registers

The addresses in this section are relative to the UART base address provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section 19.4.1 UART Register Summary.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Register Information:**
Register 19.1. UART_FIFO_REG (0x0)

- **Diagram Description:** 
The diagram shows a bit map of the UART_FIFO_REG register with labels for each bit position and their corresponding names:
- 31
- 8
- 7

Each label is followed by binary digits indicating whether that particular bit in the register corresponds to a specific function. For example, "UART_RXFIFO_RD_BYTE" has its bits labeled as follows: 
0 0 0 0 0 0 0 0 (indicating no access or reset state) and then "UART_RXFIFO_RD_BYTE" with binary digits indicating the read byte status.

**Footer Information:**  
Espressif Systems  
Submit Documentation Feedback

**Document Version:**
ESP32 TRM (Version 5.6)

**Navigation Link:**
GoBack