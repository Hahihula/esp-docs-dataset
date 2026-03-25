

```markdown
Register 7.11. PCR_UHCI_CONF_REG (0x0030)

PCR_UHCI_CLK_EN Configures whether or not to enable UHCI clock.
O: Not enable
1: Enable
(R/W)

PCR_UHCI_RST_EN Configures whether or not to reset UHCI.
O: Not reset
1: Reset
(R/W)

PCR_UHCI_READY Represents whether or not UCHI is released from reset.
O: Not released
1: Released
(RO)
```

```markdown
Register 7.12. PCR_RMT_CONF_REG (0x0034)

PCR_RMT_CLK_EN Configures whether or not to enable APB_CLK for RMT.
O: Enable
1: Not enable
(R/W)

PCR_RMT_RST_EN Configures whether or not to reset RMT.
O: Not reset
1: Reset
(R/W)

PCR_RMT_READY Represents whether or not RMT is released from reset.
O: Not released
1: Released
(RO)
```