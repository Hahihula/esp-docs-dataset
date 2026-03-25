
```markdown
## 38.3.7.5 Protocol Exception Handling

CAN FD supports protocol exception detection. This feature is enabled by setting TWAIFD_PEX = 1, which is only permitted when the controller is disabled (TWAIFD_ENA = 0).

The behavior during a protocol exception depends on the CAN implementation type (see Table 38.3-1). When exception detection is enabled (TWAIFD_PEX = 1) and an exception is detected, the controller enters a bus integration state and waits to monitor 11 consecutive recessive bits on the CAN_RX signal.

Under these conditions, the REC and TEC counters are not incremented, and the fault confinement state remains unchanged. The protocol exception status flag, TWAIFD_PEXS, is set upon detection and can be cleared by writing 1 to TWAIFD_OPEXS.

If protocol exception detection is disabled (TWAIFD_PEX = 0) and conditions for a protocol exception occur, CAN FD transmits error frames instead.

## 38.3.7.6 Implementation Type

ISO11898-1:2015 defines three implementation types of CAN protocol: classical CAN, CAN FD tolerant, and CAN FD enabled. CAN FD supports all three implementation types; compliance to each implementation type can be changed via TWAIFD_FDE and TWAIFD_PEX bits. Both of these bits should be modified only when CAN FD is disabled (TWAIFD_ENA = 0).

Table 38.3-1. CAN implementation type

| Implementation type | TWAIFD_FDE | TWAIFD_PEX | Behavior |
|---------------------|------------|------------|----------|
| Classical CAN       | 0          | 0          | When CAN FD detects the recessive FDF bit (bit after IDE in the base frame, bit after RTR/R1 in the extended frame), it responds with error frames. |
| CAN FD tolerant     | 0          | 1          | When CAN FD detects the recessive FDF bit, it detects protocol exception and enters bus integration state. |
| CAN FD enabled      | 1          | 0          | CAN FD is able to receive/transmit CAN FD frames. When CAN FD detects the recessive value on position of “res” bit (one bit after FDF bit), it responds with error frame. |
| CAN FD enabled - with protocol exception | 1          | 1          | CAN FD is able to receive/transmit CAN FD frames. When CAN FD detects the recessive value on position of “res” bit (one bit after FDF bit), it detects protocol exception and enters bus integration state. This configuration complies with future extensions of CAN FD protocols (e.g. CAN XL). |

When CAN FD is configured as the classical CAN/CAN FD tolerant node (TWAIFD_FDE = 0), and users try to send CAN FD frames (FRAME_FORMAT_W[FDF_BIT] = 1 in TX buffer), the frame type in TX buffer will be ignored and CAN 2.0 frame will be sent.

When CAN FD is configured as the classical CAN/CAN FD tolerant node, TWAIFD_NISOFD register has no effect.

According to 10.9.10 of ISO11898-1:2015, CAN FD enabled implementation should not be set to a mode where it behaves as CAN FD tolerant implementation. It is therefore users’ responsibility to use this option only for
```