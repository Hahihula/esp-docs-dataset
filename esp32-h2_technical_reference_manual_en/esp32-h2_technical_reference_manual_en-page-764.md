

```markdown
Register 28.67. UHCI_STATE0_REG (0x0018)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 6   | UHCI_DECODE_STATE   |
| 5   |                     |
| 3   |                     |
| 2   |                     |
| 1   |                     |
| 0   | Reset               |

UHCI_RX_ERR_CAUSE Represents the error type when DMA has received a packet with error.
- 0: Invalid. No effect
- 1: Checksum error in the HCI packet
- 2: Sequence number error in the HCI packet
- 3: CRC bit error in the HCI packet
- 4: 0xCO is found but the received HCI packet is not complete
- 5: 0xCO is not found when the HCI packet has been received
- 6: CRC check error
- 7: Invalid. No effect (RO)

UHCI_DECODE_STATE Represents the UHCI decoder status. (RO)

Register 28.68. UHCI_STATE1_REG (0x001C)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 3   |                     |
| 2   |                     |
| 1   |                     |
| 0   | Reset               |

UHCI_ENCODE_STATE Represents the UHCI encoder status. (RO)

Register 28.69. UHCI_RX_HEAD_REG (0x002C)

| Bit | Description         |
|-----|---------------------|
| 31  | 0                   |
|     |                     |
|     | Reset               |

UHCI_RX_HEAD Represents the header of the current received packet. (RO)
```