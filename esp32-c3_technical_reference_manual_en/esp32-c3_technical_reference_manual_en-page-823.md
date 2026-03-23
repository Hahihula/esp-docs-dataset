

```markdown
Register 31.21. TWAI_ARB_LOST_CAP_REG (0x002C)

TWAI_ARB_LOST_CAP This register contains information about the bit position of lost arbitration.
(RO)
```

```markdown
Register 31.22. TWAI_ERR_CODE_CAP_REG (0x0030)

TWAI_ECC_SEGMENT This register contains information about the location of errors, see Table 31.4-11 for details. (RO)

TWAI_ECC_DIRECTION This register contains information about transmission direction of the node when error occurs. 1: Error occurs when receiving a message; 0: Error occurs when transmitting a message (RO)

TWAI_ECC_TYPE This register contains information about error types: 00: bit error; 01: form error; 10: stuff error; 11: other type of error (RO)
```

```markdown
Register 31.23. TWAI_RX_ERR_CNT_REG (0x0038)

TWAI_RX_ERR_CNT The RX error counter register, reflects value changes in reception status. (RO | R/W)
```