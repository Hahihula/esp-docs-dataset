

```markdown
Chapter 29 I2C Controller (I2C) GoBack

29.4.5 Synchronization

I2C registers are configured in APB_CLK domain, whereas the I2C controller is configured in asynchronous I2C_SCLK domain. Therefore, before being used by the I2C controller, register values should be synchronized by first writing configuration registers and then writing 1 to `I2C_CONF_UPGATE`. Registers that need synchronization are listed in Table 29.4-1.
```