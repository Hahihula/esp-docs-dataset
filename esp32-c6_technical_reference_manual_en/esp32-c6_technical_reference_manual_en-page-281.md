

```markdown
Register 7.17. GPIO_CLOCK_GATE_REG (0x062C)

GPIO_CLK_EN Configures whether or not to enable clock gate.
O: Not enable
1: Enable, the clock is free running.
(R/W)
```

```markdown
Register 7.18. GPIO_DATE_REG (0x06FC)

GPIO_DATE Version control register.
(R/W)
```

## 7.16.2 IO MUX Registers

The addresses in this section are relative to the IO MUX base address provided in Table 5.3-2 in Chapter 5 System and Memory.

```markdown
Register 7.19. IO_MUX_PIN_CTRL_REG (0x0000)

IO_MUX_CLK_OUTx (x: 1 - 3) Configures the output clock for I2S.
0x0: Select CLK_OUT_outx for I2S output clock.
CLK_OUT_outx can be found in Table 7.11-1.
(R/W)
```
```