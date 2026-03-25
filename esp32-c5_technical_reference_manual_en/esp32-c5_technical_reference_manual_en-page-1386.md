

```markdown
The priority of "backup" TX buffers when TWAIFD_TXBBM = 1 is not configurable by the corresponding TWAIFD_TX_PRIORITY_REG[TX*P], but it is configured by a bit corresponding to the "original" TX buffer. See Section 38.3.11.3.

Figure 38.3-9. TX buffer selection

38.3.8.2 Time Triggered Transmission Mode

CAN FD supports time triggered transmission mode. This mode is enabled when TWAIFD_TTTM = 1. In this mode, CAN FD tries to transmit frames from the highest priority TX buffer only when the value of time base (see Section 38.3.3) reaches timestamp stored in TIMESTAMP_L_W and TIMESTAMP_U_W words of this TX buffer. It is assumed that the time base is an unsigned timer that counts upward. When time base reaches the value stored in TIMESTAMP_L_W, TIMESTAMP_U_W, the frame stored in TX buffer is allowed for transmission (assuming that it is in the highest priority TX buffer in "ready" state), as is visualized in Figure 38.3-10. Note that this does not mean that CAN FD will transmit the frame immediately; it will still wait until the bus is idle. If the TX buffer is in "ready" state, and the time base counter does not reach the moment of transmission yet, CAN FD waits until this condition is satisfied. If during this time, another node on the CAN bus starts transmitting a frame, CAN FD becomes the receiver of such a frame.

Figure 38.3-10. Time triggered transmission

When CAN frames should be transmitted as soon as possible (no time triggered transmission), software driver writes 0x00000000 to TIMESTAMP_L_W and TIMESTAMP_U_W words. Note that time triggered transmission is always considered only from the highest priority TX buffer in "ready" state. TX buffer priority is always
```