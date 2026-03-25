

```markdown
Chapter 29 SPI Controller (SPI)

Set the CS hold time by specifying `SPI_CS_HOLD` in `SPI_USER_REG` and `SPI_CS_HOLD_TIME` in `SPI_USER1_REG`:

- If `SPI_CS_HOLD` is cleared, the SPI CS hold time is 0.5 x T_SPI_CLK;
- If `SPI_CS_HOLD` is set, the SPI CS hold time is (`SPI_CS_HOLD_TIME + 1.5`) x T_SPI_CLK.

Figure 29.6-1 and Figure 29.6-2 show the recommended CS timing and register configuration to access external RAM and flash.

Register Configurations:

```
SPI_CS_SETUP = 1; SPI_CS_SETUP_TIME = 0;
SPI_CS_HOLD = 1; SPI_CS_HOLD_TIME = 1.
```

Figure 29.6-1. Recommended CS Timing and Settings When Accessing External RAM

Register Configurations:

```
SPI_CS_SETUP = 1; SPI_CS_SETUP_TIME = 0;
SPI_CS_HOLD = 1; SPI_CS_HOLD_TIME = 0.
```

Figure 29.6-2. Recommended CS Timing and Settings When Accessing Flash

## 29.7 GP-SPI2 Clock Control

GP-SPI2 has the following clocks:
```