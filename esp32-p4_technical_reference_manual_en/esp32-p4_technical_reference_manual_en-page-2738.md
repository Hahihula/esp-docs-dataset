

```markdown
| Bits | Name         | Description                                                                 |
|------|--------------|-----------------------------------------------------------------------------|
| 12:0 | BS (Buffer Size) | These bits indicate the size of the data buffer byte size, which must be a multiple of four. When the buffer size is not a multiple of four, the resulting behavior is undefined. This field must not be zero. |

The DES2 field contains the address pointer to the data buffer.

Table 54.8-3. DES2 Descriptor Field

| Bits | Name                  | Description                                                                 |
|------|-----------------------|-----------------------------------------------------------------------------|
| 31:0 | Buffer Address Pointer | These bits indicate the address of the data buffer. The buffer address must be word-aligned. |

The DES3 field contains the address pointer to the next descriptor if the present descriptor is not the last one in a linked list structure.

Table 54.8-4. DES3 Descriptor Field

| Bits | Name                  | Description                                                                 |
|------|-----------------------|-----------------------------------------------------------------------------|
| 31:0 | Next Descriptor Address | If CH (DESO[4]) is set to 1, these bits contain the pointer to the next descriptor. If this is not the last descriptor in a linked list structure, bits 1 and 0 must be zero, i.e., DES3[1:0] = 0. |

## 54.9 Programming Procedures

### 54.9.1 Initializing Registers

To initialize registers, perform the following steps:

1. Write to the control register SDHOST_CTRL_REG, the raw interrupt register SDHOST_RINTSTS_REG, and SDIO interrupt mask register SDHOST_INTMASK_REG to clear pending interrupts and configure controlling and interrupt parameters.

2. Write clock divider configuration register SDHOST_CLKDIV_REG, clock source selection register SDHOST_CLKSRC_REG, and clock enable register SDHOST_CLKKENA_REG to configure the card clock.

3. Write other configuration registers based on card parameters. For example, configure

* card bus width (SDHOST_CTYPE_REG)
* user ID (SDHOST_USRID_REG)
* UHS mode voltage and DDR (SDHOST_UHS_REG)
* EMMC mode start bit (SDHOST_EMMCDDR_REG)
* SDIO mode (SDHOST_CLK_EDGE_SEL_REG)
* timeout value (SDHOST_TIMEOUT_REG)
```