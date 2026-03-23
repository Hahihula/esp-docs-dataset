

```markdown
Register 5.18. GPIO_CLOCK_GATE_REG (0x062C)

GPIO_CLK_EN Clock gating enable bit. If set to 1, the clock is free running. (R/W)


Register 5.19. GPIO_DATE_REG (0x06FC)

GPIO_DATE_REG Version control register (R/W)


5.15.2 IO MUX Registers

The addresses in this section are relative to the IO MUX base address provided in Table 3.3-3 in Chapter 3 System and Memory.

Register 5.20. IO_MUX_PIN_CTRL_REG (0x0000)

IO_MUX_CLK_OUTx If you want to output clock for I2S to CLK_OUT_outx, set IO_MUX_CLK_OUTx to 0x0. CLK_OUT_outx can be found in Table 5.11-1. (R/W)
```