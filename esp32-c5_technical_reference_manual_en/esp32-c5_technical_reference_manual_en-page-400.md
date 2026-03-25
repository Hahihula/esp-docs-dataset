

# 9.5 Registers

## 9.5.1 PCR Registers

The addresses in this section are relative to the Power/Clock/Reset (PCR) Register base address provided in Table 6.3-2 in Chapter 6 System and Memory.

Register 9.1. PCR_UARTO_CONF_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 3   | PCR_UARTO_READY |
| 2   | PCR_UARTO_RST_EN |
| 1   | PCR_UARTO_CLK_EN |
| 0   | Reset |

PCR_UARTO_CLK_EN Configures whether or not to enable APB_CLK for UARTO.
- O: Not enable
- 1: Enable (R/W)

PCR_UARTO_RST_EN Configures whether or not to reset UARTO.
- O: Not reset
- 1: Reset (R/W)

PCR_UARTO_READY Represents whether or not UARTO is released from reset.
- O: Not released
- 1: Released (RO)