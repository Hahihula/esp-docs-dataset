**Chapter Title:**
Chapter 24. Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.7. DMA OPERATION_MODE_REG (0x018)

**Table Description and Values:**
- The table lists various registers with their bit positions, descriptions of the bits' functions when set or reset.

**Bit Descriptions in Markdown Format:**

- **DIS_DROP_TCPIP_ERR_FRAM**: When this bit is set, the MAC does not drop frames which only have errors detected by the Receive Checksum engine. When this bit is reset, all error frames are dropped if the Fwd_Error_Frame bit is reset.
  - (R/W)

- **RX_STORE_FORWARD**: When this bit is set, the MTL reads a frame from the Rx FIFO only after the complete frame has been written to it.
  - (R/W)

- **DIS_FLUSH_RECV_FRAMES**: When this bit is set, the Rx DMA does not flush any frames because of the unavailability of receive descriptors or buffers. This ensures that no data loss occurs during transmission interruptions due to buffer unavailability.

- **TX_STR_FWD**: When this bit is set, transmission starts when a full frame resides in the MTL Transmit FIFO.
  - (R/W)

- **FLUSH_TX_FIFO**: When this bit is set, the transmit FIFO controller logic resets its default values and thus all data in the Tx FIFO if lost or flushed. This ensures that upon reset of these bits to their initial state after a flush operation.

- **TX_THRESH_CTRL**: These bits control the threshold level of the MTL Transmit FIFO.
  - Transmission starts when the frame size within the MTL Transmit FIFO is larger than this threshold, and additional full frames with lengths less than or equal are also transmitted. The specific thresholds listed in binary format (3'b101: 32, 3'b110: 24, 3'b111: 16) indicate the range of frame sizes that trigger transmission.

- **START_STOP_TRANSMISSION_COMMAND**: When this bit is set, transmission state and the DMA checks the Transmit List at its current position for a frame to be transmitted.
  - This ensures proper management during stop states after completing transmissions. The specific binary format (3'b001: 64, 3'b001: 128, 3'b010: 192, 3'b011: 256) indicates the range of frame sizes that trigger transmission.

- **FWD_ERR_FRAME**: When this bit is reset, the Rx FIFO drops frames with error status (CRC error, collision error, giant frame, watchdog timeout).
  - This ensures data integrity by discarding erroneous packets to prevent further processing errors.
  
- **FWD_UNDER_GF**: When set, the Rx FIFO forwards Undersized frames that are less than or equal in length and include pad-bytes plus CRC. 
  - Ensures proper handling of incomplete frame transmissions.

- **DROP_GFRM**: When set, if the MAC drops received giant frames from the Rx FIFO.
  - This ensures efficient memory management by discarding oversized packets to prevent buffer overflow issues during transmission processing.


**Footer:**
Continued on the next page...

**Document Footer Information:**
Espressif Systems
494 ESP32 TRM (Version 5.6)
Submit Documentation Feedback