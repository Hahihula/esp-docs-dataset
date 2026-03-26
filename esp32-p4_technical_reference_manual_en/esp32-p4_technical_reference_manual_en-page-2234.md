

```markdown
8. Set `AXI_DMA_IN_SUC_EOF_ChN_INT_ENA` and wait for the interrupt `AXI_DMA_IN_SUC_EOF_ChN_INT`.

## 43.6 CS Setup Time and Hold Time Control

SPI bus CS (SPI_CS) setup time and hold time are very important to meet the timing requirements of various SPI devices (e.g., flash or PSRAM).

CS setup time is the time between the CS falling edge and the first latch edge of SPI bus CLK (SPI_CLK). The first latch edge for mode 0 and mode 3 is rising edge, and falling edge for mode 1 and mode 2.

CS hold time is the time between the last latch edge of SPI_CLK and the CS rising edge.

When operating as slave, the CS setup time and hold time should be longer than `0.5 x T_SPI_CLK`, otherwise the SPI transfer may be incorrect. `T_SPI_CLK` is one cycle of SPI_CLK.

When operating as master, set the CS setup time by specifying `SPI_CS_SETUP` in register `SPI_USER_REG` and `SPI_CS_SETUP_TIME` in register `SPI_USER1_REG`.

* If `SPI_CS_SETUP` is cleared, the SPI CS setup time is `0.5 x T_SPI_CLK`.
* If `SPI_CS_SETUP` is set, the SPI CS setup time is `(SPI_CS_SETUP_TIME + 1.5) x T_SPI_CLK`.

Set the CS hold time by specifying `SPI_CS_HOLD` in register `SPI_USER_REG` and `SPI_CS_HOLD_TIME` in register `SPI_USER1_REG`.

* If `SPI_CS_HOLD` is cleared, the SPI CS hold time is `0.5 x T_SPI_CLK`.
* If `SPI_CS_HOLD` is set, the SPI CS hold time is `(SPI_CS_HOLD_TIME + 1.5) x T_SPI_CLK`.

Figure 43.6-1 and Figure 43.6-2 show the recommended CS timing and register configuration to access external RAM and flash.

![Recommended CS Timing Diagram](#)

Register Configurations:

```
SPI_CS_SETUP = 1; SPI_CS_SETUP_TIME = 0;
SPI_CS_HOLD = 1; SPI_CS_HOLD_TIME = 1.
```

Figure 43.6-1. Recommended CS Timing and Settings When Accessing External RAM
```