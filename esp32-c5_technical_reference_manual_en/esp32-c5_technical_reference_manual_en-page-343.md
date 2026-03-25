

```markdown
Register 8.15. GPIO_PINn_REG (n: 0-28) (0x00C4+0x4*n)

Continued from the previous page...

GPIO_PINn_INT_ENA Configures whether or not to enable CPU interrupt or GPIO_SDIO_INT interrupt.
- Bit[13]: Configures whether or not to enable CPU interrupt:
    O: Disable
    1: Enable
- Bit[14]: Invalid
- Bit[15]: Configures whether or not to enable GPIO_SDIO_INT interrupt:
    O: Disable
    1: Enable
- Bit[16]~bit[17]: Invalid
(R/W)
```