

```markdown
Register 38.23. TWAIFD_ERR_CAPT_RETR_CTR_ALC_TS_INFO_REG (0x007C)

| Bit | 31 | 30 | 29 | 24 | 23 | 21 | 20 | 16 | 15 | 12 | 11 | 8 | 7 | 5 | 4 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|
|     |    |    |    |    |    |    |    |    |    |    |    |   |   |   |   |   |
| Value | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | OxO | OxO | 0x1f | Reset |

TWAIFD_ERR_POS Represents the position of the last error.
- 0: ERC_POS_SOF - Error in start of frame
- 1: ERC_POS_ARB - Error in arbitration filed
- 2: ERC_POS_CTRL - Error in control field
- 3: ERC_POS_DATA - Error in data field
- 4: ERC_POS_CRC - Error in CRC field
- 5: ERC_POS_ACK - Error in CRC delimiter, ACK field or ACK delimiter
- 6: ERC_POS_EOF - Error in end of frame field
- 7: ERC_POS_ERR - Error during error frame
- 8: ERC_POS_OVRL - Error in overload frame
- 31: ERC_POS_OTHER - Error at other positions (RO)

TWAIFD_ERR_TYPE Represents the type of the last error.
- 0: ERC_BIT_ERR - Bit error
- 1: ERC_CRC_ERR - CRC error
- 2: ERC_FRM_ERR - Form error
- 3: ERC_ACK_ERR - ACK error
- 4: ERC_STUF_ERR - Stuff error (RO)

TWAIFD_RETR_CTR_VAL Represents the current value of the retransmission counter. (RO)

TWAIFD_ALC_BIT Represents the arbitration lost capture bit position. If the value is ALC_BASE_ID, the bit index of the base identifier where arbitration was lost is 11 - ALC_VAL. If the value is ALC_EXTENSION, the bit index of the extended identifier where arbitration was lost is 18 - ALC_VAL. Other values are invalid. (RO)

TWAIFD_ALC_ID_FIELD Represents the part of the CAN identifier where arbitration was lost.
- 0: ALC_RSVD - Arbitration was not lost since last reset
- 1: ALC_BASE_ID - Arbitration was lost during the base identifier
- 2: ALC_SRR_RTR - Arbitration was lost during first bit after the base identifier (SRR of extended frame, RTR bit of CAN 2.0 base frame)
- 3: ALC_IDE - Arbitration was lost during the IDE bit
- 4: ALC_EXTENSION - Arbitration was lost during the extended identifier
- 5: ALC_RTR - Arbitration was lost during RTR bit after the extended identifier (RO)

TWAIFD_TS_BITS Represents the number of active bits of the time base minus 1 (0x3F = 64-bit time base). (RO)
```