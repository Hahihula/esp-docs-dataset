

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| PMS_CORE1_MM_HP_PERI_PMS_REG3_REG         | Permission control register3 for HP<br>CPU1 in machine mode                 | 0x0034  | R/W    |
| PMS_CORE1_UM_HP_PERI_PMS_REG0_REG          | Permission control register0 for HP<br>CPU1 in user mode                    | 0x0038  | R/W    |
| PMS_CORE1_UM_HP_PERI_PMS_REG1_REG          | Permission control register1 for HP<br>CPU1 in user mode                    | 0x003C  | R/W    |
| PMS_CORE1_UM_HP_PERI_PMS_REG2_REG          | Permission control register2 for HP<br>CPU1 in user mode                    | 0x0040  | R/W    |
| PMS_CORE1_UM_HP_PERI_PMS_REG3_REG          | Permission control register3 for HP<br>CPU1 in user mode                    | 0x0044  | R/W    |

### 19.6.3 LP2HP_PERI_PMS_REG

The addresses in this section are relative to the LP2HP_PERI_PMS base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| Version Control Registers                 |                                                                             |         |        |
| PMS_LP2HP_PERI_PMS_DATE_REG               | Version control register                                                    | 0x0000  | R/W    |
| Clock Gating Registers                    |                                                                             |         |        |
| PMS_LP2HP_PERI_PMS_CLK_EN_REG             | Clock gating register                                                      | 0x0004  | R/W    |
| LP CPU Permission Control Registers       |                                                                             |         |        |
| PMS_LP_MM_PMS_REG0_REG                    | Permission control register0 for the LP CPU<br>in machine mode              | 0x0008  | R/W    |
| PMS_LP_MM_PMS_REG1_REG                    | Permission control register1 for the LP CPU in<br>machine mode              | 0x0030  | R/W    |
| PMS_LP_MM_PMS_REG2_REG                    | Permission control register2 for the LP CPU<br>in machine mode              | 0x00A4  | R/W    |
| PMS_LP_MM_PMS_REG3_REG                    | Permission control register3 for the LP CPU<br>in machine mode              | 0x011C  | R/W    |

### 19.6.4 LP_PERI_PMS_REG

The addresses in this section are relative to the LP_PERI_PMS base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| Version Control Registers                 |                                                                             |         |        |
```