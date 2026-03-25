

```markdown
| PMU_n1_DIG_ICG_FUNC_EN Bit | Clock                  |
|-----------------------------|------------------------|
| bit 0                       | GDMA_CLK               |
| bit 1                       | SPI2_CLK               |
| bit 2                       | I2S_RX_CLK             |
| bit 3                       | UARTO_CLK              |
| bit 4                       | UART1_CLK              |
| bit 5                       | UHCI_CLK               |
| bit 6                       | USB_CLK                |
| bit 7                       | I2S_TX_CLK             |
| bit 8                       | N/A                    |
| bit 9                       | N/A                    |
| bit 10                      | N/A                    |
| bit 11                      | N/A                    |
| bit 12                      | N/A                    |
| bit 13                      | TG1_CLK                |
| bit 14                      | TGO_CLK                |
| bit 15                      | N/A                    |
| bit 16                      | SOC_ETM_CLK            |
| bit 17                      | N/A                    |
| bit 18                      | SYSTIMER_CLK           |
| bit 19                      | N/A                    |
| bit 20                      | SARADC_CLK             |
| bit 21                      | RMT_CLK                |
| bit 22                      | MCPWM_CLK              |
| bit 23                      | N/A                    |
| bit 24                      | PARLIO_TX_CLK          |
| bit 25                      | PARLIO_RX_CLK          |
| bit 26                      | N/A                    |
| bit 27                      | LEDC_CLK               |
| bit 28                      | IOMUX_CLK              |
| bit 29                      | I2C_CLK                |
| bit 30                      | N/A                    |
| bit 31                      | TWAIO_CLK              |

- Configure PMU_n1_DIG_ICG_APB_EN to power up/down the APB clock in the target PMU state. For detailed configuration please see Table 11.4-3.

Table 11.4-3. HP System Peripherals' APB Clocks

| PMU_n1_DIG_ICG_APB_EN Bit | Clock                  |
|---------------------------|------------------------|
| bit 0                     | SEC_APB_CLK            |
| bit 1                     | GDMA_APB_CLK           |
| bit 2                     | API2_APB_CLK           |
```