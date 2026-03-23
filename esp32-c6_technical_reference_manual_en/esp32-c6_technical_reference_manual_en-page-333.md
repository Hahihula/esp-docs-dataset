

```markdown
Register 8.22. PCR_TWAIO_CONF_REG (0x005C)

PCR_TWAIO_CLK_EN   Configures whether or not to enable TWAIO APB clock.
    O: Not enable
    1: Enable
      (R/W)

PCR_TWAIO_RST_EN   Configures whether or not to reset TWAIO module.
    O: Not reset
    1: Reset
      (R/W)
```

```markdown
Register 8.23. PCR_TWAIO_FUNC_CLK_CONF_REG (0x0060)

PCR_TWAIO_FUNC_CLK_SEL   Configures to select clock source.
    O (default): Select XTAL_CLK
    1: Select RC_FAST_CLK
      (R/W)

PCR_TWAIO_FUNC_CLK_EN   Configures whether or not to enable TWAIO function clock.
    O: Not enable
    1: Enable
      (R/W)
```