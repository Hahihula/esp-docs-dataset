

```markdown
| PMU_n1_DIG_ICG_FUNC_EN Bit | Clock                     |
|----------------------------|---------------------------|
| bit 19                     | N/A                       |
| bit 20                     | SARADC_CLK                |
| bit 21                     | RMT_CLK                   |
| bit 22                     | MCPWM_CLK                 |
| bit 23                     | N/A                       |
| bit 24                     | PARLIO_TX_CLK             |
| bit 25                     | PARLIO_RX_CLK             |
| bit 26                     | N/A                       |
| bit 27                     | LEDC_CLK                  |
| bit 28                     | IOMUX_CLK                 |
| bit 29                     | I2C_CLK                   |
| bit 30                     | TWAI1_CLK                 |
| bit 31                     | TWAIO_CLK                 |

- Configure PMU_n1_DIG_ICG_APB_EN to power up/down the APB clock in the target PMU state. For detailed configuration please see Table 12.4-3.

Table 12.4-3. HP System Peripherals’ APB Clocks

| PMU_n1_DIG_ICG_APB_EN Bit | Clock                     |
|---------------------------|---------------------------|
| bit 0                     | SEC_APB_CLK               |
| bit 1                     | GMDA_APB_CLK              |
| bit 2                     | API2_APB_CLK              |
| bit 3                     | INTMTX_APB_CLK            |
| bit 4                     | I2S_APB_CLK               |
| bit 5                     | MSPI_APB_CLK              |
| bit 6                     | UARTO_APB_CLK             |
| bit 7                     | UART1_APB_TX_CLK          |
| bit 8                     | UHCI_APB_CLK              |
| bit 9                     | SARADC_APB_CLK            |
| bit 10                    | N/A                       |
| bit 11                    | TimerGroup0_APB_CLK       |
| bit 12                    | TimerGroup1_APB_CLK       |
| bit 13                    | I2C_APB_CLK               |
| bit 14                    | LEDC_APB_CLK              |
| bit 15                    | RMT_APB_CLK               |
| bit 16                    | SYSTIMER_APB_CLK          |
| bit 17                    | USB_DEVICE_APB_CLK        |
| bit 18                    | TWAIO_APB_CLK             |
| bit 19                    | TWAI1_APB_CLK             |
| bit 20                    | PCNT_APB_CLK              |
| bit 21                    | PWM_APB_CLK               |
| bit 22                    | SOC_ETM_CLK               |
| bit 23                    | PARLIO_APB_CLK            |
```