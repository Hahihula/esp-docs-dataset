

```markdown
2. Configuration of CAN FD:
   (a) Configure interrupts as in Section 38.4 Interrupts
   (b) Configure bit rate as in Section 38.3.7.1 Bit Rate
   (c) Configure other features (filters, special modes, etc.)
3. Enable CAN FD by writing 1 to TWAIFD_ENA.
4. Poll on TWAIFD_EWL_ERP_FAULT_STATE_REG register, or wait for fault confinement state to trigger the interrupt TWAIFD_FCSIINTST. Integration is finished when TWAIFD_ERA=1 (CAN FD becomes error-active).
5. Initialization is finished, software driver can send and receive frames.

38.3.6 De-initialization Sequence

De-initialization sequence consists of the following steps:
1. Ensure that no TX buffer is in “ready”, “TX in progress” or “abort in progress” states. This can be done by issuing “set abort” command (see Section 38.3.8 CAN Frame Transmission) to TX buffers, and not inserting next frames for transmission into TX buffers.
2. Clear TWAIFD_ENA.

38.3.7 CAN Bus Configuration

38.3.7.1 Bit Rate

Bit rate on the CAN bus is derived from the system clock (see Section 38.3.1 Clock). Basic unit of time on the CAN bus is time quanta. Time quanta is derived from system clock by dividing its frequency by bit rate prescaler. CAN FD has a separate prescaler for nominal bit rate (TWAIFD_BRP) and data bit rate (TWAIFD_BRP_FD). Bit rate on CAN FD is configured by specifying Prop_Seg, Phase_Seg1 and Phase_Seg2 durations, as shown in Figure 38.3-3. These are specified in TWAIFD_BTR_REG (nominal bit rate) and TWAIFD_BTR_FD_REG (data bit rate) registers.

Figure 38.3-3. Bit time

Please refer to Section 38.5.1 500 Kbit/2 Mbit Example for programming proceduess.
```