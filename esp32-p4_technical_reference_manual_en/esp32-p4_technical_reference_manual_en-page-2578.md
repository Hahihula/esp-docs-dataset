

```markdown
|Bit|31|30|29|28|27|26|25|24|23|22|21|20|19|18|17|16|
|:----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||0|0|0|0|0|0|0|0|0|0|0|1|0|0|0|1|
|||(reserved)|USB_SERIAL_JTAG_USB_PAD_PULLUP_VALUE|USB_SERIAL_JTAG_USB_PAD_PULLDOWN|USB_SERIAL_JTAG_DM_PULLUP|USB_SERIAL_JTAG_DP_PULLUP|USB_SERIAL_JTAG_VREFH_OVERRIDE|USB_SERIAL_JTAG_VREFL_OVERRIDE|USB_SERIAL_JTAG_EXCHG_PINS_OVERRIDE|USB_SERIAL_JTAG_PHY_SEL|
```

**Register 51.3. USB_SERIAL_JTAG_CONFO_REG (0x0018)**

`USB_SERIAL_JTAG_PHY_SEL` Configures whether to select internal or external PHY.
- O: Internal PHY
- 1: External PHY
(R/W)

`USB_SERIAL_JTAG_EXCHG_PINS_OVERRIDE` Configures whether to enable software control USB D+ D- exchange.
- O: Disable
- 1: Enable
(R/W)

`USB_SERIAL_JTAG_EXCHG_PINS` Configures whether to enable USB D+ D- exchange.
- O: Disable
- 1: Enable
(R/W)

`USB_SERIAL_JTAG_VREFH` Configures single-end input high threshold.
- 0: 1.76 V
- 1: 1.84 V
- 2: 1.92 V
- 3: 2.00 V
(R/W)

`USB_SERIAL_JTAG_VREFL` Configures single-end input low threshold.
- 0: 0.80 V
- 1: 0.88 V
- 2: 0.96 V
- 3: 1.04 V
(R/W)

`USB_SERIAL_JTAG_VREF_OVERRIDE` Configures whether to enable software control input threshold.
- O: Disable
- 1: Enable
(R/W)
```