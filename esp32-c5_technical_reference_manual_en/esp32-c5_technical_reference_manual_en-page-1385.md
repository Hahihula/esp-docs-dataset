

```markdown
Figure 38.3-8. TX buffer states

After software driver stores CAN frames to a TX buffer, it issues “set ready” command to this TX buffer to request transmission of stored CAN frames. TX buffer moves to “ready” state, and CAN FD can transmit frames from this TX buffer. When CAN FD starts transmission from this TX buffer, it moves to “TX in progress” state. CAN FD starts transmission from TX buffer which is in “ready” state if it samples dominant bits during the third bit of intermission (SOF bit is skipped in this case), or as soon as the bus is idle. Note that in time triggered transmission mode, the behavior differs (see Section 38.3.8.2).

When CAN FD is error-passive and it is the transmitter of the previous frame, it suspends consecutive transmission for 8 bit times. When CAN FD transmits CAN frames successfully (no arbitration lost, no error frame), the TX buffer moves to “TX OK” state. If an error frame occurs or arbitration is lost, the TX buffer moves to “ready” state and transmission will start again in the nearest intermission or bus idle.

When CAN FD operates in bus monitoring mode (TWAIFD_BMM = 1) or restricted operation mode (TWAIFD_ROM = 1) it always ends up in “TX failed” state when “set ready” command is issued, without any attempt to transmit the frame.

38.3.8.1 TX Buffer Selection

If there are multiple TX buffers in “ready” state, CAN FD selects the highest priority TX buffer in “ready” state and transmits CAN frames from this TX buffer. Priority of TX buffers is configured in TWAIFD_TX_PRIORITY_REG. If two TX buffers have equal priority, TX buffer with the lower index has precedence. The overall flow of transmission is shown in Figure 38.3-9.

Higher value of TWAIFD_TX_PRIORITY_REG[TX*P] means TX buffer * has the higher priority. For example, if TWAIFD_TX_PRIORITY_REG[TX1P] = 2 and TWAIFD_TX_PRIORITY_REG[TX2P] = 5, then TX buffer 2 has priority 5, a higher priority than TX buffer 1. Consequently, when both TX buffers are in “ready” state, CAN FD will pick TX buffer 2 before TX buffer 1.
```