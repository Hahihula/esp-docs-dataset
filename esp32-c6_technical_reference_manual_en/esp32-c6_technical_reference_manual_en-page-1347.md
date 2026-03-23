

```markdown
Register 38.1. PARL_IO_RX_CFG0_REG (0x0000)

Continued from the previous page...

PARL_IO_RX_LEVEL_SUBMODE_SEL Configures whether to sample data at high or low level of the external enable signal.
O: At high level
1: At low level
(R/W)

PARL_IO_RX_SMP_MODE_SEL Configures RX data sampling mode.
O: External Level Enable mode
1: External Pulse Enable mode
2: Internal Software Enable mode
(R/W)

PARL_IO_RX_CLK_EDGE_SEL Configures whether to invert the RX input clock.
O: Not invert
1: Invert
(R/W)

PARL_IO_RX_BIT_PACK_ORDER Configures the packing order to pack bits into 1 byte when data bus width is 4/2/1 bit.
O: Pack from MSB
1: Pack from LSB
(R/W)

PARL_IO_RX_BUS_WID_SEL Configures RX data bus width.
O: 16 bit
1: 8 bit
2: 4 bit
3: 2 bit
4: 1 bit
(R/W)

PARL_IO_RX_FIFO_SRST Configures whether to enable soft reset of async FIFO in the RX unit.
O: Disable
1: Enable
(R/W)
```