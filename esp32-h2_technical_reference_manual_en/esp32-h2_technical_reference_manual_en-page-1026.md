

```markdown
Register 34.25. TWAI_ARB_LOST_CAP_REG (0x002C)

TWAI_ARB_LOST_CAP Represents the bit position of lost arbitration. (RO)


Register 34.26. TWAI_ERR_CODE_CAP_REG (0x0030)

TWAI_ECC_SEGMENT Represents the location of errors, see Table 34.4-11 for details. (RO)

TWAI_ECC_DIRECTION Represents transmission direction of the node when error occurs.
    0: Error occurs when transmitting a message
    1: Error occurs when receiving a message
    (RO)

TWAI_ECC_TYPE Represents error types.
    0: Bit error
    1: Form error
    2: Stuff error
    3: Others
    (RO)


Register 34.27. TWAI_RX_ERR_CNT_REG (0x0038)

TWAI_RX_ERR_CNT The RX error counter register, reflects value changes in reception status. (RO | R/W)
```