

```markdown
Register 10.54. HP_SYS_CLKRST_HPWTDCORE1_RST_CTRL0_REG (0x00D8)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-29     | (reserved)                                 |                                                                             |
| 28        | Reset                                      |                                                                             |
| 27-24     | HP_SYS_CLKRST_HPCORE1_STALL_EN             | Configures the behavior when MWDT triggers HP CPU1 reset.                   |
|           |                                             | 0: Immediately reset HP CPU1                                                 |
|           |                                             | 1: Stall HP CPU1 first (R/W)                                                |
| 23-16     | HP_SYS_CLKRST_HPCORE1_STALL_WAIT_NUM       | Configures the duration of HP CPU1 stall when MWDT triggers HP CPU1 reset and HP_SYS_CLKRST_HPCORE1_STALL_EN is set to 1. Measurement unit: Clock cycles. (R/W) |
| 15-8      | HP_SYS_CLKRST_WDT_HPCORE1_RST_LEN          | Configures the duration of the reset when MWDT triggers HP CPU1 reset.       |
|           |                                             | Measurement unit: Clock cycles. (R/W)                                       |

Register 10.55. HP_SYS_CLKRST_CPU_SRC_FREQ_REG (0x00DC)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-29     | (reserved)                                 |                                                                             |
| 28        | Reset                                      |                                                                             |
| 27-0      | HP_SYS_CLKRST_CPU_SRC_FREQ                 | Represents the CPU source clock frequency.                                  |
|           |                                             | 80: RC_FAST_CLK                                                               |
|           |                                             | 160: XTAL_CLK                                                                |
|           |                                             | 1600: CPLL_CLK                                                               |
|           |                                             | (RO)                                                                        |
```