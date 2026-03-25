

```markdown
- If this eFuse is 1, LP_AON_FORCE_DOWNLOAD_BOOT is disabled, and GPIO_STRAPPING can not be overwritten.

*   **EFUSE_DIS_DOWNLOAD_MODE**
    If this eFuse is 1, Joint Download Boot mode is disabled, and `GPIO_STRAPPING` will not be overwritten by `LP_AON_FORCE_DOWNLOAD_BOOT`.

*   **EFUSE_ENABLE_SECURITY_DOWNLOAD**
    If this eFuse is 1, Joint Download Boot mode only allows reading, writing, and erasing plaintext flash and does not support any SRAM or register operations. Ignore this eFuse if Joint Download Boot mode is disabled.

*   **EFUSE_DIS_DIRECT_BOOT**
    If this eFuse is 1, Direct Boot mode is disabled.
```

USB Serial/JTAG Controller can also force switch the chip to Joint Download Boot mode from SPI Boot mode, and vice versa. For detailed information, please refer to Chapter 29 USB Serial/JTAG Controller.

## 8.2.3 SDIO Sampling and Driving Clock Edge Control

The strapping pin MTMS and MTDI can be used to decide on which clock edge to sample signals and drive output lines. See Table 8.2-3 SDIO Input Sampling Edge/Output Driving Edge Control.

Table 8.2-3. SDIO Input Sampling Edge/Output Driving Edge Control

| Edge behavior                                                                 | MTMS¹   | MTDI¹ |
|-------------------------------------------------------------------------------|---------|-------|
| Falling edge sampling, falling edge output                                   | 0       | 0     |
| Falling edge sampling, rising edge output                                    | 0       | 1     |
| Rising edge sampling, falling edge output                                    | 1       | 0     |
| Rising edge sampling, rising edge output                                     | 1       | 1     |

¹ MTMS and MTDI are floating by default, so above are not default configurations.

## 8.2.4 ROM Messages Printing Control

During the ROM boot stage of SPI Boot mode, GPIO8, LP_AON_STORE4_REG[0], and `EFUSE_UART_PRINT_CONTROL` jointly control the printing of ROM messages.
```