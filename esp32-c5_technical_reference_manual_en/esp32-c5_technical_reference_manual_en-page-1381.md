

```markdown
### 38.3.7.2 Transmitter Delay

Transmitter delay is the propagation delay of signals transmitted by CAN FD on CAN_TX output back to CAN_RX input, as is visualized in Figure 38.3-4. This delay involves propagation of signals to physical layer transceiver, delay of transceiver itself, and delay from transceiver to CAN_RX input. CAN FD measures its own transmitter delay when transmitting CAN FD frames, regardless of whether the bit rate is switched in the frame. The measurement is taken on the recessive-to-dominant edge between the FDF (EDL) and RO bits, as shown in Figure 38.3-5. Transmitter delay is readable after its measurement from TWAIFD_TRV_DELAY_VALUE.

Transmitter delay is measured in system clock periods.

![Figure 38.3-4. Transmitter delay](image_path)

![Figure 38.3-5. Transmitter delay measurement](image_path)

Measured transmitter delay includes input delay of CAN FD, which is 2 system clock periods. Therefore, measured transmitter delay will always be higher by two than the actual delay from CAN_TX to CAN_RX. For example, if signal propagation from CAN_TX to CAN_RX takes 110 ns (11 system clock periods at 100 MHz), measured transmitter delay will be 13.

Transmitter delay measurement is saturated to 127 system clock periods. If the delay between CAN_TX and CAN_RX is longer, only 127 will be measured. When system clock frequency is 100 MHz, this gives a maximum measurable transmitter delay of 1.27 µs, which is more than most CAN transceivers need.

### 38.3.7.3 Secondary Sampling Point

Secondary sampling point can be used by CAN FD during data bit rate to detect bit errors. Its position is configured as delay from start of bit time (Sync_Seg) in multiple system clock periods (not time quanta). Secondary sampling point position can be fixed (TWAIFD_SSP_OFFSET only), derived from transmitter delay (TWAIFD_SSP_OFFSET and TWAIFD_TRV_DELAY_VALUE), or it can be disabled (no SSP) as is shown in Figure 38.3-6. When the secondary sampling point is disabled, the regular sampling point as configured by TWAIFD_BTR_REG is used by CAN FD when transmitting in data bit rate.
```