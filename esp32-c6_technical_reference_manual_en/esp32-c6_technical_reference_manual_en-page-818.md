
```markdown
Chapter 27 UART Controller (UART, LP_UART, UHCI)
Register 27.99. UHCI_STATE0_REG (0x0018)

UHCI_RX_ERR_CAUSE Represents the error type when DMA has received a packet with error.
- 0: Invalid. No effect
- 1: Checksum error in the HCI packet
- 2: Sequence number error in the HCI packet
- 3: CRC bit error in the HCI packet
- 4: 0xC0 is found but the received HCI packet is not complete
- 5: 0xC0 is not found when the HCI packet has been received
- 6: CRC check error
- 7: Invalid. No effect (RO)

UHCI_DECODE_STATE Represents the UHCI decoder status. (RO)
Register 27.100. UHCI_STATE1_REG (0x001C)

UHCI_ENCODE_STATE Represents the UHCI encoder status. (RO)
Register 27.101. UHCI_RX_HEAD_REG (0x002C)

UHCI_RX_HEAD Represents the header of the current received packet. (RO)
```