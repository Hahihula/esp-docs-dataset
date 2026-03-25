

```markdown
Register 11.93. PAU_REGDMA_CONF_REG (0x0000)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 12  | PAU_SEL_MAC                                                                |
| 11  | PAU_TO_MEM_MAC                                                             |
| 10  | PAU_START_MAC                                                              |
| 9   | PAU_LINK_SEL                                                               |
| 8   | PAU_FLOW_ERR                                                               |
| 7-4 | 0x0                                                                        |
| 3   | 0x0                                                                        |
| 2   | 0x0                                                                        |
| 1   | Reset                                                                      |
```

**PAU_FLOW_ERR** Represents the backup error type.
*   0: Received software triggered interrupt clear signal
*   1: Peripheral AHB bus timeout
*   2: Memory AHB bus timeout
*   3: Address link list wait timer timeout
*   4: Address mapping error (RO)

**PAU_START** Write 1 to initiate the backup start signal. (WT)

**PAU_TO_MEM** Configures the backup direction.
*   0: register to memory
*   1: memory to register
(R/W)

**PAU_LINK_SEL** Configures to select the link.
*   0: PAU_REGDMA_LINK_0_ADDR_REG
*   1: PAU_REGDMA_LINK_1_ADDR_REG
*   2: PAU_REGDMA_LINK_2_ADDR_REG
*   3: PAU_REGDMA_LINK_3_ADDR_REG
(R/W)

**PAU_START_MAC** Write 1 to initiate the MAC software backup start signal. (WT)

**PAU_TO_MEM_MAC** Configures the MAC software backup direction.
*   0: register to memory
*   1: memory to register
(R/W)

**PAU_SEL_MAC** Configures the MAC hardware/software selection.
*   0: select the hardware path
*   1: select the software path
(R/W)
```