**Title:**
Chapter 19 UART Controller (UART)

**Subtitle:**
19.3.7.1 Hardware Flow Control

**Diagram Title and Description:**
Hardware Flow Control  
Figure 19.3-5 illustrates how the UART hardware flow control works.

**Body Text with Diagram Annotations:**

- **Diagram Components:** 
  - UART_SW_RTS
  - Comparator
  - UART_RTS_INV
  - UART_LOOPBACK
  - UART_CTSInv
  - UART_DSRInv

- **Text Explanation of Figure (Figure Caption):**
  - "Figure 19.3-5 Hardware Flow Control"

**Detailed Description:**

- **Flow Control Mechanism:** 
  - A high state of the output signal rtsn_out signifies that a data transmission is requested, while a low state notifies the counterpart to stop data transmission until rtsn_out is pulled high again.
  
- **Configuration Options for UART_RX_FLOW_EN (0 or 1):**
  - When UART_RX_FLOW_EN is set to `0`, the level of rtsn_out can be changed by configuring UART_SW_RTS.
  - When UART_RX_FLOW_EN is set to `1`, if data in Rx_FIFO is greater than UART_RX_FLOW_THRHD, the level of rtsn_out will be lowered.

- **Interrupt Handling:**
  - If the UART controller detects an edge on ctsn_in, it generates interrupt UART_CTS_CHG_INT and stops transmitting data once current transmission completes.
  
- **Data Preparation Indication (dtrn_out):**
  - The high level of dtrn_out signifies that the transmitter has finished data preparation. UART controller will generate interrupt UART_DSR_CHG_INT after detecting an edge on input signal dsrn_in.

- **Interrupt Handling for Data Reception:**
  - After software detects the mentioned interrupt, it can figure out if the input signal level is `dsrn_in` by reading UART_DSRN.
  
- **Loopback Function (UART_LOOPBACK):**
  - Setting UART_LOOPBACK enables loopback detection function. The output signal txd_out of UART connected to its input signal rxd_in; rtsn_out connects to ctsn_in, and dtrn_out is connected to dsrn_out.

**Subsection Title:**

19.3.7.2 Software Flow Control

**Body Text for Subsection 19.3.7.2:** 

- **Software Control Mechanism Description:**
  - Software can force the transmitter to stop transmitting data by setting UARTFORCE_XOFF, as well as forcing the transmitter to continue sending data by setting UARTFORCE_XON.

**Footer Information:**

- Page Number and Document Version:
  - "316 ESP32 TRM (Version 5.6)"
  
- Submission Options:
  - Submit Documentation Feedback