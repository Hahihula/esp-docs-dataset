

```markdown
Register 19.11. AES_DMA_EXIT_REG (0x00B8)

AES_DMA_EXIT   Configures whether to exit AES operation.
               O: No effect
               1: Exit
               Only valid for DMA-AES operation. (WO)


Register 19.12. AES_PSEUDO_REG (0x00D0)

AES_PSEUDO_EN   Configures whether to enable the pseudo-round function of AES.
                O: Disabled
                1: Enabled
                (R/W)

AES_PSEUDO_BASE  Configures the basic number of pseudo-rounds. (R/W)

AES_PSEUDO_INC   Configures the random incremental number of pseudo-rounds. (R/W)

AES_PSEUDO_RNG_CNT Configures the frequency of pseudo-key updates in the pseudo-round function. (R/W)


Register 19.13. AES_INT_CLR_REG (0x00AC)

AES_INT_CLR     Configures whether to clear AES interrupt.
                O: No effect
                1: Clear
                (WT)
```