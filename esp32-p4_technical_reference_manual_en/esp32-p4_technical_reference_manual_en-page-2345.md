

```markdown
Register 43.93. LP_SPI_DIN_NUM_REG (0x0028)

LP_SPI_DINO_NUM   Configures the delays to input signal LP_SPI_D based on the setting of LP_SPI_DINO_MODE.
    0: Delayed by 1 clock cycle
    1: Delayed by 2 clock cycles
    2: Delayed by 3 clock cycles
    3: Delayed by 4 clock cycles
    (R/W)

LP_SPI_DIN1_NUM   Configures the delays to input signal LP_SPI_Q based on the setting of LP_SPI_DIN1_MODE.
    0: Delayed by 1 clock cycle
    1: Delayed by 2 clock cycles
    2: Delayed by 3 clock cycles
    3: Delayed by 4 clock cycles
    (R/W)

Register 43.94. LP_SPI_DOUT_MODE_REG (0x002C)

LP_SPI_DOUTO_MODE   Configures the output mode for LP_SPI_D signal.
    0: Output without delay
    1: Output with a delay of an LP-SPI module clock cycle at its falling edge
    (R/W)

LP_SPI_DOUT1_MODE   Configures the output mode for LP_SPI_Q signal.
    0: Output without delay
    1: Output with a delay of an LP-SPI module clock cycle at its falling edge
    (R/W)
```