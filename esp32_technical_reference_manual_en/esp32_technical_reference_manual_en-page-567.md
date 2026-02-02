**Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**Diagram Title and Description:**
Figure 26.3-6. Packet Sending Procedure (Initiated by Slave)

**Diagram Content Summary:**
The diagram illustrates the packet sending procedure initiated by a slave in an SDIO context, showing interactions between Host and Slave components.

**Body Text Explanation of Diagram Steps:**

1. **Host Side Actions:**
   - CPU prepares data for transfer.
   - Waits until ready to send (Packet Length Accumulator Register).
   - CPU updates SLCHOST_PKT_LEN register value with the packet length minus last time's accumulated sum, then sends CMD53.

2. **Slave Side Actions and Responses:**
   - Slave module receives interrupt from DMA controller indicating a new packet.
   - DMA transfers data to SDIO Physical Bus for sending out (Packet Length Accumulator Register).

**Additional Information Provided in Text Below Diagram:**

- When the Host is interrupted, it reads relevant information about packets by visiting registers SLCOHOST_INT and SLCHOST_PKT_LEN.

  **Key Points from Text:**
  
  - `SLCOHOST_INT`: Interrupt status register. If its value of SLCO_RX_NEW_PACKET_INT_ST equals to 1, this indicates that the Slave has a packet ready for sending.
  - `SLCHOST_PKT_LEN`: Packet length accumulator register which holds current data minus last time's accumulated sum.

- To start DMA transfer:
  - CPU writes low bits (20) of address in first linked-list element into SLCO_RXLINK_ADDR bit, then sets the SLCORX_START bit.
  - DMA completes packet transfer and interrupts CPU to free buffer space for reuse. 

**Footer:**
Espressif Systems
567

**Link Text at Bottom Right Corner:** 
Submit Documentation Feedback

**Document Version Information (at bottom right):**
ESP32 TRM (Version 5.6)