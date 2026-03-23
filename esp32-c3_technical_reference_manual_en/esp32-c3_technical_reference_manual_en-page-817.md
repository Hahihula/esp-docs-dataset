

```markdown
Chapter 31 Two-wire Automotive Interface (TWAI)

Register 31.7. TWAI_DATA_2_REG (0x0048)
```

```text
(reserved)          TWAI_TX_BYTE_2 | TWAI_ACCEPTANCE_CODE_2
31                   8               7                    0

0x0                 Reset
```

TWAI_TX_BYTE_2 Stored the 2nd byte information of the data to be transmitted in operation mode. (WO)

TWAI_ACCEPTANCE_CODE_2 Stored the 2nd byte of the filter code in reset mode. (R/W)

Register 31.8. TWAI_DATA_3_REG (0x004C)
```

```text
(reserved)          TWAI_TX_BYTE_3 | TWAI_ACCEPTANCE_CODE_3
31                   8               7                    0

0x0                 Reset
```

TWAI_TX_BYTE_3 Stored the 3rd byte information of the data to be transmitted in operation mode. (WO)

TWAI_ACCEPTANCE_CODE_3 Stored the 3rd byte of the filter code in reset mode. (R/W)
```