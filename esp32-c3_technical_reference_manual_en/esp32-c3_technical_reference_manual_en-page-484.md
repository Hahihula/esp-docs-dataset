

```markdown
## Register 18.8. AES_INC_SEL_REG (0x009C)

AES_INC_SEL Defines the Standard Incrementing Function for CTR block operation. Set this bit to 0 or 1 to choose INC₃₂ or INC₁₂₈. (R/W)


## Register 18.9. AES_TRIGGER_REG (0x0048)

AES_TRIGGER Set this bit to 1 to start AES operation. (WO)


## Register 18.10. AES_STATE_REG (0x004C)

AES_STATE Stores the working status of the AES Accelerator. For details, see Table 18.4-1 for Typical AES working mode and Table 18.5-2 for DMA AES working mode. (RO)


## Register 18.11. AES_DMA_EXIT_REG (0x00B8)

AES_DMA_EXIT Set this bit to 1 to exit AES operation. This register is only effective for DMA-AES operation. (WO)
```