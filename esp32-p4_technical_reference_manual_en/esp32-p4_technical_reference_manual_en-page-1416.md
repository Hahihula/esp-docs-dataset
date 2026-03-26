

```markdown
## 23.8 Registers

The addresses in this section are relative to Brown-out Detector base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 23.1. LP_ANA_BOD_MODEO_CNTL_REG (0x0000)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | O                                                                         |
| 30  | O                                                                         |
| 29  | O                                                                         |
| 28  | O                                                                         |
| 27  | O                                                                         |
|     | LP_ANA_BOD_MODEO_RESET_ENA                                                 |
|     | LP_ANA_BOD_MODEO_RESET_SEL                                                |
|     | LP_ANA_BOD_MODEO_INTR_ENA                                                 |
|     | LP_ANA_BOD_MODEO_CNTL_CLR                                                  |
|     | LP_ANA_BOD_MODEO_RESET_WAIT                                               |
| 16  | LP_ANA_BOD_MODEO_CLOSE_FLASH_ENA                                          |
| 17  | LP_ANA_BOD_MODEO_INTR_WAIT                                                |
| 8   | LP_ANA_BOD_MODEO_RESET_WAIT                                              |
| 7   | (reserved)                                                                |
| 6   | (reserved)                                                                |
| 5   | (reserved)                                                                |
| 0   | Reset                                                                     |

LP_ANA_BOD_MODEO_CLOSE_FLASH_ENA Configure to close the flash functionality when under-voltage happens in Mode O.
- O: Disable
- 1: Enable
(R/W)

LP_ANA_BOD_MODEO_INTR_WAIT Configure the counter threshold that triggers interrupts in Mode O. (R/W)

LP_ANA_BOD_MODEO_RESET_WAIT Configure the counter threshold that triggers reset in Mode O. (R/W)

LP_ANA_BOD_MODEO_CNTL_CLR Clear counter value in Mode O. (R/W)

LP_ANA_BOD_MODEO_INTR_ENA Configure to enable the counter and interrupts in Mode O.
- O: Disable
- 1: Enable
(R/W)

LP_ANA_BOD_MODEO_RESET_SEL Configure the reset way when under-voltage happens in Mode O.
- O: Reset the chip
- 1: Reset the system
(R/W)

LP_ANA_BOD_MODEO_RESET_ENA Configure to enable reset in Mode O.
- O: Disable
- 1: Enable
(R/W)
```