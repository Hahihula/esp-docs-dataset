**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.6. DMASTASUS_REG (0x0014)

**Continuation Note:**
Continued from the previous page...

**List of Register Bits with Descriptions and Access Modes:**

- **RECV_PROC_STOP**: This bit is asserted when the Receive Process enters the Stopped state.
  - **Access Mode:** Read/Write/Shared (R/SS/WC)

- **RECV_BUF_UNAVAIL**: This bit indicates that the host owns the Next Descriptor in the Receive List and the DMA cannot acquire it. The Receive Process is suspended. To resume processing Receive descriptors, the host should change the ownership of the descriptor and issue a Receive Poll Demand command. If No Receive Poll Demand is issued, the Receive Process resumes when the next recognized incoming frame is received. This bit is set only when the previous Receive Descriptor is owned by the DMA.
  - **Access Mode:** Read/Write/Shared (R/SS/WC)

- **RECV_INT**: This bit indicates that the frame reception is complete. When reception is complete, the Bit[31] of RDES1 (Disable Interrupt on Completion) in reset in the last Descriptor, and the specific frame status information is updated in the descriptor. The reception remains in the Running state.
  - **Access Mode:** Read/Write/Shared (R/SS/WC)

- **TRANS_UNDFLOW**: This bit indicates that the Transmit Buffer had an Underflow during frame transmission. Transmission is suspended and an Underflow Error TDESO[1] is set.
  - **Access Mode:** Read/Write/Shared (R/SS/WC)

- **RECV_OVERFLOW**: This bit indicates that the Receive Buffer had an Overflow during frame reception. If the partial frame is transferred to the application, the overflow status is set in RDES0[1].
  - **Access Mode:** Read/Write/Shared (R/SS/WC)

- **TRANS_JABBER_TO**: This bit indicates that the Transmit Jabber Timer expired, which happens when the frame size exceeds 2,048 bytes. When the Jabber Timeout occurs, the transmission process is aborted and placed in the Stopped state.
  - **Access Mode:** Read/Write/Shared (R/SS/WC)

- **TRANS_BUF_UNAVAIL**: This bit indicates that the host owns the Next Descriptor in the Transmit List and the DMA cannot acquire it. Transmission is suspended. Bits[22:20] explain the Transmit Process state transitions.
  - To resume processing Transmit descriptors, the host should change the ownership of the descriptor by setting TDESO[31] and then issue a Transmit Poll Demand command (R/SS/WC).

- **TRANS_PROC_STOP**: This bit is set when the transmission is stopped. 
  - **Access Mode:** Read/Write/Shared (R/SS/WC)

- **TRANS_INT**: This bit indicates that the frame transmission is complete.
  When transmission is complete, Bit[31] (OWN) of TDESO is reset and specific frame status information updated in the descriptor.

**Footer:**
Espressif Systems
493 ESP32 TRM (Version 5.6)
Submit Documentation Feedback