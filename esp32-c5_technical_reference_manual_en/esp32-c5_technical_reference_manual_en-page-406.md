

```markdown
## Register 9.9. PCR_TWAIO_CONF_REG (0x0028)

PCR_TWAIO_CLK_EN Configures whether or not to enable TWAIO APB_CLK.
- O: Not enable
- 1: Enable
(R/W)

PCR_TWAIO_RST_EN Configures whether or not to reset TWAIO.
- O: Not reset
- 1: Reset
(R/W)

PCR_TWAIO_READY Represents whether or not TWAIO is released from reset.
- O: Not released
- 1: Released
(RO)
```

```markdown
## Register 9.10. PCR_TWAIO_FUNC_CLK_CONF_REG (0x002C)

PCR_TWAIO_FUNC_CLK_SEL Configures the clock source of TWAIO.
- O (default): XTAL_CLK
- 1: RC_FAST_CLK
(R/W)

PCR_TWAIO_FUNC_CLK_EN Configures whether or not to enable TWAIO functional clock.
- O: Not enable
- 1: Enable
(R/W)
```