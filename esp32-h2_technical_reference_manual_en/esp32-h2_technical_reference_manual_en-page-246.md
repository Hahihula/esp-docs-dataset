

```markdown
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

Register 6.7. GPIO_STRAP_REG (0x0038)


GPIO_STRAPPING Represents the values of GPIO Strapping pins.

- bit0: GPIO2 (GPIO2 should be reserved as a Strapping pin only when using SPI Download Boot mode.)
- bit1: GPIO3 (GPIO3 should be reserved as a Strapping pin only when using SPI Download Boot mode.)
- bit2: GPIO8 (this value will also be affected by EFUSE_DIS_FORCE_DOWNLOAD and LP_AON_FORCE_DOWNLOAD_BOOT.)
- bit3: GPIO9 (this value will also be affected by EFUSE_DIS_FORCE_DOWNLOAD and LP_AON_FORCE_DOWNLOAD_BOOT.)
- bit4: GPIO25
- bit5 ~ bit15: invalid

For more details about GPIO Strapping pins, please refer to the Chapter 8 Chip Boot Control. (RO)


Register 6.8. GPIO_IN_REG (0x003C)


GPIO_IN_DATA_NEXT Represents the input value of GPIO0 ~ GPIO27. Each bit represents a pin input value:
O: Low level
1: High level
bit0 ~ bit27 are corresponding to GPIO0 ~ GPIO27. Bit28 ~ bit31 are invalid.
(RO)
```