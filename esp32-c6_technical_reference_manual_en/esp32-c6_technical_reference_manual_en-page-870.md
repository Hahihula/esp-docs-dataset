

```markdown
Register 28.6. SPI_CTRL_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 1  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |
```

**SPI_DUMMY_OUT** Configures whether or not to output the FSPI bus signals in DUMMY state. (R/W)

*   0: Not output
*   1: Output

Can be configured in CONF state.

**SPI_FADDR_DUAL** Configures whether or not to enable 2-bit mode during address (ADDR) state. (R/W)

*   0: Disable
*   1: Enable

Can be configured in CONF state.

**SPI_FADDR_QUAD** Configures whether or not to enable 4-bit mode during address (ADDR) state. (R/W)

*   0: Disable
*   1: Enable

Can be configured in CONF state.

**SPI_FCMD_DUAL** Configures whether or not to enable 2-bit mode during command (CMD) state. (R/W)

*   0: Disable
*   1: Enable

Can be configured in CONF state. (R/W)

**SPI_FCMD_QUAD** Configures whether or not to enable 4-bit mode during command (CMD) state. (R/W)

*   0: Disable
*   1: Enable

Can be configured in CONF state. (R/W)

Continued on the next page...
```