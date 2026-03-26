

```markdown
Register 52.6. DMASTATUS_REG (0x1014)

Continued from the previous page...

RECV_BUF_UNAVAIL Represents whether the Receive Buffer is available.
O: Available
1: Unavailable
This bit is set only when the previous Receive Descriptor is owned by the DMA.
When set, the Host owns the Next Descriptor in the Receive List and the DMA cannot acquire it. The Receive Process is suspended.
To resume processing Receive descriptors, the Host should change the ownership of the descriptor and issue a Receive Poll Demand command. If no Receive Poll Demand is issued, the Receive Process resumes when the next recognized incoming frame is received. (R/SS/WC)

RECV_INT The raw interrupt status of RECV_INT. (R/SS/WC)

TRANS_UNDFLOW Represents whether the Transmit Buffer had an Underflow during frame transmission.
O: No underflow
1: Underflow
When this bit is 1, transmission is suspended and an Underflow Error TDESO[1] is set. (R/SS/WC)

RECV_OVFLOW Represents whether the Receive Buffer had an Overflow during frame reception.
O: No overflow
1: Overflow
If the partial frame is transferred to the application, the overflow status is set in RDESO[11]. (R/SS/WC)

TRANS_JABBER_TO Represents whether the Transmit Jabber Timer expired, which happens when the frame size exceeds 2,048 (10,240 bytes when the Jumbo frame is enabled).
O: Not expired
1: Expired
When the Jabber Timeout occurs, the transmission process is aborted and placed in the Stopped state. This causes the Transmit Jabber Timeout TDESO[14] flag to assert. (R/SS/WC)

TRANS_BUF_UNAVAIL Represents whether the Transmit Buffer is available.
O: Available
1: Unavailable
When this bit is 1, the Host owns the Next Descriptor in the Transmit List and the DMA cannot acquire it. Transmission is suspended. Bits[22:20] explain the Transmit Process state transitions.
To resume processing Transmit descriptors, the Host should change the ownership of the descriptor by setting TDESO[31] and then issue a Transmit Poll Demand command. (R/SS/WC)

TRANS_PROC_STOP Represents whether the transmission is stopped.
O: Not stopped
1: Stopped
(R/SS/WC)

TRANS_INT The raw interrupt status of TRANS_INT. (R/SS/WC)
```