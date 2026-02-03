**Title:**
Chapter 26 UART Controller (UART)

**Link:**
GoBack

**Table Title and Content:**
- **Table 26.5-2 – cont’d from previous page**

| Register | Field |
|----------|-------|
|          | UART_AT_CMD_CHA[7:0] |

**Subsection Titles with Text:**
1. **26.5.1.3 Immediate Registers**
   - Except those listed in Table 26.5-1 and Table 26.5-2, registers that can be configured by software are immediate registers read in APB_CLK domain, such as interrupt and FIFO configuration registers.

2. **26.5.2 Detailed Steps**

**Body Text:**
Figure 26.5-1 illustrates the process to program UART controllers, namely initializing the UART, configuring the registers, enabling the transmitter and/or receiver, and finishing data transmission.
   
**Flowchart Description (labeled as Figure 26.5-1):**
- **Start**
- **Initialize UARTn**
- **Configure registers**
   - Check if `UART_REG_UPDATE == 0`
     - If No: Loop back to "Configure other registers"
     - If Yes:
       - Set `UART_REG_UPDATE` to 1
       - Enable UART TX/RX
       - End

**Footer Information:**
Figure 26.5-1. UART Programming Procedures  
Espressif Systems  
941  
ESP32-S3 TRM (Version 1.7)  

**Link at the bottom of page:** Submit Documentation Feedback