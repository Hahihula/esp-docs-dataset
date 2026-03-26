

```markdown
Register 40.16. CSI_HOST_INT_MSK_PKT_FATAL_REG (0x00F4)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             |                                                                             |
|     |                                             | Reset                                                                       |
| 2   | CS1_HOST_MASK_SHORTER_PAYLOAD              | Configures whether to mask CSI_HOST_ST_SHORTER_PAYLOAD.                    |
|     |                                             | 0: Mask the error interrupt<br>1: Enable the error interrupt (R/W)          |
| 1   | CS1_HOST_MASK_ERR_ECC_DOUBLE               | Configures whether to mask CSI_HOST_ST_ERR_ECC_DOUBLE.                     |
|     |                                             | 0: Mask the error interrupt<br>1: Enable the error interrupt (R/W)          |
```