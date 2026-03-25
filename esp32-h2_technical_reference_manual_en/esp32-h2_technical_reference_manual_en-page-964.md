

```markdown
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)
Register 33.3. USB_SERIAL_JTAG_CONFO_REG (0x0018)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
|     |    |    |    |    |    |    |    |    |    |    |    | Reset |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |
```

USB_SERIAL_JTAG_PHY_SEL Configures whether to select internal or external PHY.
0: Internal PHY
1: External PHY
(R/W)

USB_SERIAL_JTAG_EXCH_PINS_OVERRIDE Configures whether to enable software control USB D+ and D- exchange.
0: Disable
1: Enable
(R/W)

USB_SERIAL_JTAG_EXCH_PINS Configures whether to enable USB D+ and D- exchange.
0: Disable
1: Enable
(R/W)

USB_SERIAL_JTAG_VREFH Configures single-end input high threshold.
0: 1.76 V
1: 1.84 V
2: 1.92 V
3: 2.00 V
(R/W)

USB_SERIAL_JTAG_VREFL Configures single-end input low threshold.
0: 0.80 V
1: 0.88 V
2: 0.96 V
3: 1.04 V
(R/W)

USB_SERIAL_JTAG_VREF_OVERRIDE Configures whether to enable software control input threshold.
0: Disable
1: Enable
(R/W)
```