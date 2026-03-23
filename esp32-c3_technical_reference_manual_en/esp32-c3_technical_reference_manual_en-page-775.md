

```markdown
|Bit|15|14|13|12|11|10|9|8|7|6|5|4|3|2|1|0|
|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
|USB_SERIAL_JTAG_PHY_SEL|Select internal/external PHY. 1'b0: internal PHY, 1'b1: external PHY.|(R/W)|
|USB_SERIAL_JTAG_EXCHG_PINS_OVERRIDE|Enable software control USB D+ D- exchange.|(R/W)|
|USB_SERIAL_JTAG_EXCHG_PINS|USB D+ D- exchange|(R/W)|
|USB_SERIAL_JTAG_VREFL|Control single-end input high threshold. 1.76 V to 2 V, step 80 mV.|(R/W)|
|USB_SERIAL_JTAG_VREFH|Control single-end input low threshold. 0.8 V to 1.04 V, step 80 mV.|(R/W)|
|USB_SERIAL_JTAG_VREF_OVERRIDE|Enable software control input threshold.|(R/W)|
|USB_SERIAL_JTAG_PAD_PULL_OVERRIDE|Enable software control USB D+ D- pull-up pull-down.|(R/W)|
|USB_SERIAL_JTAG_DP_PULLUP|Control USB D+ pull-up.|(R/W)|
|USB_SERIAL_JTAG_DP_PULLDOWN|Control USB D+ pull-down.|(R/W)|
|USB_SERIAL_JTAG_DM_PULLUP|Control USB D- pull-up.|(R/W)|
|USB_SERIAL_JTAG_DM_PULLDOWN|Control USB D- pull-down.|(R/W)|
|USB_SERIAL_JTAG_PULLUP_VALUE|Control pull-up value. 0: 2.2 K; 1: 1.1 K.|(R/W)|
|USB_SERIAL_JTAG_USB_PAD_ENABLE|Enable USB pad function.|(R/W)|
```