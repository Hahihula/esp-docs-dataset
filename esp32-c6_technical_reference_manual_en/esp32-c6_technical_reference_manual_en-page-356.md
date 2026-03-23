

```markdown
Register 8.61. PCR_MODEM_APB_CONF_REG (0x0108)

PCR_MODEM_APB_CLK_EN   Configures whether or not to enable MODEM_APB clock.
    0: Disable
    1: Enable
    (R/W)

PCR_MODEM_RST_EN      Configures whether or not to reset modem subsystem.
    0: Not reset
    1: Reset
    (R/W)
```

```markdown
Register 8.62. PCR_TIMEOUT_CONF_REG (0x010C)

PCR_CPU_TIMEOUT_RST_EN   Configures whether or not to reset CPU_PERI TIMEOUT module.
    0: Not reset
    1: Reset
    (R/W)

PCR_HP_TIMEOUT_RST_EN    Configures whether or not to reset HP_PERI TIMEOUT module and
                         HP_MODEM TIMEOUT module.
    0: Not reset
    1: Reset
    (R/W)
```