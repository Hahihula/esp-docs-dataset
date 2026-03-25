

```markdown
Register 38.48. TWAIFD_DEBUG_REG (0x008C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | TWAIFD_PC_SOF | TWAIFD_PC_OVR | TWAIFD_PC_SUSP | TWAIFD_PC_INT | TWAIFD_PC_ECF | TWAIFD_PC_ACKD | TWAIFD_PC_CRCD | TWAIFD_PC_STC | TWAIFD_PC_DAT | TWAIFD_PC_CON | TWAIFD_PC_ARB | TWAIFD_DESTUFF_COUNT | TWAIFD_STUFF_COUNT |
```

**TWAIFD_STUFF_COUNT** The current stuff bit count modulo 8, as defined by the ISO FD protocol. The stuff count is reset at the start of each CAN frame and increments by one for each stuff bit up to the stuff count field in the ISO FD frame, after which it remains fixed until the next frame begins. In non-ISO FD or standard CAN, stuff bits are counted until the end of the frame. Note that this field is NOT Gray-coded as specified in the ISO FD standard. The stuff count is updated only while the controller is actively transmitting or receiving on the bus; during reception, this value remains unchanged. (RO)

**TWAIFD_DESTUFF_COUNT** Represents the current de-stuff bit count modulo 8, as defined by the ISO FD protocol. The de-stuff count is reset at the start of each frame and increments by one for each de-stuffed bit up to the stuff count field in the ISO FD frame, after which it remains fixed until the next frame begins. In non-ISO FD or standard CAN, de-stuff bits are counted until the end of the frame. Note that this field is NOT Gray-coded as specified in the ISO FD standard. The de-stuff count is updated during both transmission and reception. (RO)

**TWAIFD_PC_ARB** Represents whether the protocol control state machine is in the arbitration field.
- 0: Not in the field
- 1: In the field (RO)

**TWAIFD_PC_CON** Represents protocol control state machine is in the control field.
- 0: Not in the field
- 1: In the field (RO)

**TWAIFD_PC_DAT** Represents protocol control state machine is in the data field.
- 0: Not in the field
- 1: In the field (RO)

**TWAIFD_PC_STC** Represents protocol control state machine is in the stuff count field.
- 0: Not in the field
- 1: In the field (RO)

**TWAIFD_PC_CRC** Represents protocol control state machine is in the CRC field.
- 0: Not in the field
- 1: In the field (RO)
```