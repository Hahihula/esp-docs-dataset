**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.6. DMASTATUS_REG (0x0014)

**Continuation Note:**
Continued from the previous page...

---

### ERROR BITS

This field indicates the type of error that caused a Bus Error, for example, error response on the AHB interface. This field is valid only when Bit[13] (FIFO) is set. This field does not generate an interrupt.

- 3'b000: Error during Rx DMA Write Data Transfer.
- 3'b011: Error during Tx DMA Read Data Transfer.
- 3'b100: Error during Rx DMA Descriptor Write Access.
- 3'b101: Error during Tx DMA Descriptor Write Access.
- 3'b110: Error during Rx DMA Descriptor Read Access.
- 3'b111: Error during Tx DMA Descriptor Read Access.

---

### TRANS_PROC_STATE

This field indicates the Transmit DMA FSM state. This field does not generate an interrupt (RO).

- 3'b000: Stopped. Reset or Stop Transmit Command issued.
- 3'b001: Running. Fetching Transmit Transfer Descriptor.
- 3'b010: Reserved for future use.
- 3'b011: Running. Waiting for TX packets.
- 3'b100: Suspended. Receive Descriptor Unavailable.
- 3'b101: Running. Closing Transmit Descriptor.
- 3'b110: Reserved.
- 3'b111: Running. Transferring the TX packets data from transmit buffer to host memory.

---

### RECV_PROC_STATE

This field indicates the Receive DMA FSM state. This field does not generate an interrupt (RO).

- 3'b000: Stopped. Reset or Stop Receive Command issued.
- 3'b001: Running. Fetching Receive Transfer Descriptor.
- 3'b010: Reserved for future use.
- 3'b011: Running. Waiting for RX packets.
- 3'b100: Suspended. Receive Descriptor Unavailable.
- 3'b101: Running. Closing Receive Descriptor.
- 3'b110: Reserved.
- 3'b111: Running. Transferring the TX packets data from receive buffer to host memory.

---

**Continuation Note (at bottom):**
Continued on the next page...

**Footer Information:**
Espressif Systems
491 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Navigation Link:**
GoBack