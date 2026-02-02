**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.20. EMACDEBUG_REG (0x1024)

**Table Description and Values:**
- The table shows various fields in the register with their bit positions, values when high or low.
- Fields include MTLISFS, MTLTFNES, MACTPFC, MACRFFS among others.

**Field Descriptions:**

1. **MTLTSFSS**
   - When high, this bit indicates that the MTL TxStatus FIFO is full. Therefore, the MTL cannot accept any more frames for transmission.
   
2. **MTLTFNES**
   - When high, this bit indicates that the MTL Tx FIFO is not empty and some data is left for transmission.

3. **MTLTFWCS**
   - When high, this bit indicates that the MTL Tx FIFO Write Controller is active and is transmitting data to the Tx FIFO.
   
4. **MTLTFRCS**
   - This field indicates the state of the Tx FIFO Read Controller:
     - 2'b00: IDLE state
     - 2'b01: READ state (transferring data to the MAC transmitter)
     - 2'b10: Waiting for TxStatus from the MAC transmitter.
     - 2'b11: Writing the received TxStatus or flushing the Tx FIFO.

5. **MACTP**
   - When high, this bit indicates that the MAC transmitter is in the Pause condition (in full-duplex mode) and hence does not schedule any frame for transmission.

6. **MACTFCS**
   - This field indicates the state of the MAC Transmit Frame Controller module:
     - 2'b00: IDLE state.
     - 2'b01: Waiting for status of previous frame or IFG or backoff period to be over.
     - 2'b10: Generating and transmitting a Pause frame (in full-duplex mode).
     - 2'b11: Transferring input frame for transmission.

7. **MACTPES**
   - When high, this bit indicates that the MAC MII transmit protocol engine is actively transmitting data and is not in the IDLE state.
   
8. **MTLRFFLS**
   - This field gives the status of the fill-level of the Rx FIFO:
     - 2'b00: Rx FIFO Empty
     - 2'b01: Rx FIFO fill-level below flow-control deactivate threshold.
     - 2'b10: Rx FIFO fill-level above flow-control activate threshold.
     - 2'b11: Rx FIFO Full.

**Footer Note:** 
Continued on the next page...

**Company Information and Document Version:**
Espressif Systems
508 ESP32 TRM (Version 5.6)

**Action Links:**
Submit Documentation Feedback