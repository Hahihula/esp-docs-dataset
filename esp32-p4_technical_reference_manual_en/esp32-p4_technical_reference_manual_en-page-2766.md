

```markdown
Register 54.29. SDHOST_IDSTS_REG (0x0080C)

SDHOST_IDSTS_TI The raw interrupt status of Transmit Interrupt. Indicates that data transmission is finished for a descriptor. (R/W1C)

SDHOST_IDSTS_RI The raw interrupt status of Receive Interrupt. Indicates the completion of data reception for a descriptor. (R/W1C)

SDHOST_IDSTS_FBE The raw interrupt status of Fatal Bus Error Interrupt. Indicates that a Bus Error occurred (SDHOST_IDSTS_REG[12:10]). (R/W1C)

SDHOST_IDSTS_DU The raw interrupt status of Descriptor Unavailable Interrupt. This bit is set when the descriptor is unavailable due to OWNER bit = 0 (DESO[31] = 0). (R/W1C)

SDHOST_IDSTS_CES The raw interrupt status of Card Error Summary. Indicates the status of the transaction to/from the card, also present in SDHOST_RINTSTS_REG. Indicates the logical OR of the following bits:
- EBE: End-bit error/no CRC error
- SBE/BCI: RX Start Bit Error
- DRTO: Data read timeout
- RTO: Response timeout
- DCRC: Data CRC error
- RCRC: Response CRC error
- RE: Response error

The abort condition of the DMA depends on the setting of this field. If this field is enabled, then the DMA aborts on a response error. (R/W1C)

SDHOST_IDSTS_NIS The raw interrupt status of Normal Interrupt Summary. Logical OR of SD-HOST_IDSTS_REG[1:0]. Only unmasked bits affect this bit. This is a sticky bit and must be cleared each time a corresponding bit that causes this field to be set is cleared by software. (R/W1C)

SDHOST_IDSTS_AIS The raw interrupt status of Abnormal Interrupt Summary. Logical OR of SD-HOST_IDSTS_REG[2], SDHOST_IDSTS_REG[4]. Only unmasked bits affect this bit. This is a sticky bit and must be cleared each time a corresponding bit that causes this field to be set is cleared by software. (R/W1C)

Continued on the next page...
```