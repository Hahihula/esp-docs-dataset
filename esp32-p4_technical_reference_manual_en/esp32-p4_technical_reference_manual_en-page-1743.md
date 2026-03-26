

```markdown
Register 36.149. CSI_BRIG_DMABLK_SIZE_REG (0x0030)

[Diagram: Register layout for CSI_BRIG_DMABLK_SIZE_REG]
- Bitfield labeled "CSI_BRIG_DMABLK_SIZE" from bit 12 to 0.
- Bits 31..13 are marked "(reserved)".
- Reset value is 0x1fff.

CSI_BRIG_DMABLK_SIZE Configures the number of VDMA bursts in a VDMA block transfer. (R/W)

Register 36.150. CSI_BRIG_DATA_TYPE_CFG_REG (0x0010)

[Diagram: Register layout for CSI_BRIG_DATA_TYPE_CFG_REG]
- Bitfield labeled "CSI_BRIG_DATA_TYPE_MAX" from bit 7 to 5.
- Bitfield labeled "CSI_BRIG_DATA_TYPE_MIN" from bit 4 to 0.
- Bits 31..14 and bits 8..6 are marked "(reserved)".
- Reset value is 0x2f for the upper portion (bits 14 down) and lower part appears as two fields with values implied by layout.

CSI_BRIG_DATA_TYPE_MIN Configures the minimum value of DATA_TYPE for valid pixels. (R/W)
CSI_BRIG_DATA_TYPE_MAX Configures the maximum value of DATA_TYPE for valid pixels. (R/W)
```