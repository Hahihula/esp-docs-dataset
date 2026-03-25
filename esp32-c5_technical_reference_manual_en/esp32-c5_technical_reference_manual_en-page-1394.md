

```markdown
When TWAIFD_TXBBM = 1, and CAN FD detects a parity error in the "original" TX buffer RAM, such TX buffer moves to "Parity error" state, and CAN FD attempts to transmit frames from its "backup" TX buffer (e.g. if CAN FD detects parity error in TX buffer 3, it attempts to transmit a frame from TX buffer 4). If CAN FD successfully transmits a frame from "original" TX buffer, its "backup" Buffer moves to "aborted" state (CAN FD does not transmit frames in the "backup" TX buffer).

When CAN FD is transmitting a frame from a "backup" TX buffer due to parity errors in "original" TX buffer, and it detects parity errors also in "backup" TX buffer RAM, CAN FD sets TWAIFD_TXDPE bit (double parity error).

When CAN FD operates in TX buffer backup mode, software control of TX buffers has following differences compared to non-backup modes:

* Priorities of both TX buffers within TX buffer pair are equal, and they are given by `TWAIFD_TX_PRIORITY_REG[TX*P]` of "original" TX buffer. For example, priority of TX buffers 1 and 2 is given by `TWAIFD_TX_PRIORITY_REG[TX1P]`, and `TWAIFD_TX_PRIORITY_REG[TX2P]` has no effect.
* CAN FD automatically applies commands issued by software to each "original" TX buffer and also to its corresponding "backup" TX buffer. For example, if software gives a command to TX buffer 1 (`TX_COMMAND[TXB1] = 1`), CAN FD automatically applies it to TX buffer 2.

It is assumed that software stores equal CAN frames to both TX buffers from a TX buffer pair when attempting to send CAN frames. In such case, the effect of TX buffer backup mode is as follows: If a parity error occurs in "original" TX buffer RAM, the same frame is transmitted from "backup" TX buffer.

Figure 38.3-16. Operation in TX buffer backup mode
```