

```markdown
## Register 9.16. PCR_RMT_PD_CTRL_REG (0x0044)

PCR_RMT_MEM_FORCE_PU Configures whether or not to force power up RMT memory.
- O: Not force power up
- 1: Force power up
(R/W)

PCR_RMT_MEM_FORCE_PD Configures whether or not to force power down RMT memory.
- O: Not force power down
- 1: Force power down
(R/W)


## Register 9.17. PCR_LEDC_CONF_REG (0x0048)

PCR_LEDC_CLK_EN Configures whether or not to enable APB_CLK for LEDC.
- O: Not enable
- 1: Enable
(R/W)

PCR_LEDC_RST_EN Configures whether or not to reset LEDC.
- O: Not reset
- 1: Reset
(R/W)

PCR_LEDC_READY Represents whether or not LEDC is released from reset.
- O: Not released
- 1: Released
(RO)
```