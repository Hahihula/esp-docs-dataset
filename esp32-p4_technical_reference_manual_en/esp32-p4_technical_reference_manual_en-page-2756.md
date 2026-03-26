

```markdown
Register 54.15. SDHOST_HCON_REG (0x0070)

| Bit | 31 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 18 | 17 | 16 | 15 | 10 | 9 | 7 | 6 | 5 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | (reserved) | SDHOST_NUM_CLK_DIV_REG | SDHOST_HOLD_REG | SDHOST_RAM_INDISE_REG | SDHOST_DMA_WIDTH_REG | (reserved) | SDHOST_ADDR_WIDTH_REG | SDHOST_DATA_WIDTH_REG | SDHOST_BUS_TYPE_REG | SDHOST_CARD_NUM_REG | SDHOST_CARD_TYPE_REG |
| Value | 0x0 | 0x0 | 0x3 | 0x1 | 0x1 | 0x0 | 0x1 | 0x0 | 0x13 | 0x1 | Reset |

SDHOST_NUM_CLK_DIV_REG Represents 4 clk divider in design. (RO)

SDHOST_HOLD_REG Represents a hold register in data path. (RO)

SDHOST_RAM_INDISE_REG Represents that the SDMMC module contains RAM. (RO)

SDHOST_DMA_WIDTH_REG Represents that the DMA data width is 32. (RO)

SDHOST_ADDR_WIDTH_REG Represents that the register address width is 32. (RO)

SDHOST_DATA_WIDTH_REG Represents that the register data width is 32. (RO)

SDHOST_BUS_TYPE_REG Represents that the register is configured for the APB bus. (RO)

SDHOST_CARD_NUM_REG Represents that the number of supported cards is 2. (RO)

SDHOST_CARD_TYPE_REG Represents that the hardware supports SDIO and MMC. (RO)
```

```markdown
Register 54.16. SDHOST_UHS_REG (0x0074)

| Bit | 31 | 18 | 17 | 16 | 15 | ... | 2 | 1 | 0 |
|-----|----|----|----|----|----|-----|---|---|---|
|     |    | (reserved) | SDHOST_DDR_REG | (reserved) | SDHOST_VOLT_REG | Reset |
| Value | 0x0 | ... | 0x0 | ... | 0x0 |

SDHOST_VOLT_REG Configures High Voltage mode per card. Bit[0] corresponds to card[0]. For every card bit:
- 0: 3.3 V VDD
- 1: 1.8 V VDD
(R/W)

SDHOST_DDR_REG Configures DDR (double data rate) mode selection per card. Bit[0] corresponds to card[0]. For every card bit:
- 0: Non-DDR mode
- 1: DDR mode
(R/W)
```