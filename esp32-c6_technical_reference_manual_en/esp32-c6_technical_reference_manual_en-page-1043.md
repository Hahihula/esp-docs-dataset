

```markdown
|Bit|15|14|13|12|11|10|9|8|7|6|5|4|3|2|1|0|
|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
|Value|(reserved)|USB_SERIAL_JTAG_USB_PAD_ENABLE|USB_SERIAL_JTAG_USB_PAD_PULLUP_VALUE|USB_SERIAL_JTAG_DM_PULLDOWN|USB_SERIAL_JTAG_DP_PULLDOWN|USB_SERIAL_JTAG_PAD_PULLUP|USB_SERIAL_JTAG_VREFH|USB_SERIAL_JTAG_VREFL|USB_SERIAL_JTAG_EXCHG_PINS_OVERRIDE|USB_SERIAL_JTAG_PINS_OVERRIDE|USB_SERIAL_JTAG_PHY_SEL||
```

**USB_SERIAL_JTAG_PHY_SEL** Configures whether to select internal or external PHY.

0: Internal PHY
1: External PHY
(R/W)

**USB_SERIAL_JTAG_EXCHG_PINS_OVERRIDE** Configures whether to enable software control USB D+ D- exchange.

0: Disable
1: Enable
(R/W)

**USB_SERIAL_JTAG_EXCHG_PINS** Configures whether to enable USB D+ D- exchange.

0: Disable
1: Enable
(R/W)

**USB_SERIAL_JTAG_VREFH** Configures single-end input high threshold.

0: 1.76 V
1: 1.84 V
2: 1.92 V
3: 2.00 V
(R/W)

**USB_SERIAL_JTAG_VREFL** Configures single-end input low threshold.

0: 0.80 V
1: 0.88 V
2: 0.96 V
3: 1.04 V
(R/W)

**USB_SERIAL_JTAG_VREF_OVERRIDE** Configures whether to enable software control input threshold.
```