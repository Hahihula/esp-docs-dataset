

```markdown
Register 54.3. SDHOST_CLKSRC_REG (0x0000C)

SDHOST_CLKSRC_REG Configures clock divider source for two SD cards. Each card has two bits assigned to it. For example, bit[1:0] are assigned to card 0, and bit[3:2] are assigned to card 1. Card 1/0 maps and internally routes clock divider[0:3] outputs to cclk_out[1:0] pins, depending on bit value. For every card’s clock divider source:

- 0x0: Clock divider 0
- 0x1: Clock divider 1
- 0x2: Clock divider 2
- 0x3: Clock divider 3

(R/W)

Register 54.4. SDHOST_CLKENA_REG (0x0010)

SDHOST_CCLK_ENABLE Configures whether to enable two SD card clocks or one MMC card clock. One bit per card. For every card’s bit:

- 0: Clock disabled
- 1: Clock enabled

(R/W)

SDHOST_LP_ENABLE Configures whether to disable the clock when the card is in an IDLE state. One bit per card. For every card’s bit:

- 0: Clock disabled
- 1: Clock enabled

(R/W)
```