

```markdown
| Hash Algorithm | Length of Message Digest (in bits) | Storage¹ |
|----------------|------------------------------------|----------|
| SHA-1          | 160                                | SHA_H_O_REG ~ SHA_H_4_REG |
| SHA-224        | 224                                | SHA_H_O_REG ~ SHA_H_6_REG |
| SHA-256        | 256                                | SHA_H_O_REG ~ SHA_H_7_REG |

¹ The message digest is stored in registers from most significant bits to the least significant bits, with the first word stored in register SHA_H_O_REG and the second word stored in register SHA_H_1_REG... For details, please see subsection 21.4.1.2.
```

## 21.4.4 Interrupt

SHA accelerator supports interrupt on the completion of message digest calculation when working in the DMA-SHA mode. To enable this function, write 1 to register `SHA_INT_ENA_REG`. Note that the interrupt should be cleared by software after use via setting the `SHA_INT_CLEAR_REG` register to 1.

## 21.5 Register Summary

The addresses in this section are relative to the SHA accelerator base address provided in Table 3.3-3 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Control/Status registers** | | | |
| SHA_CONTINUE_REG | Continues SHA operation (only effective in Typical SHA mode) | 0x0014 | WO |
| SHA_BUSY_REG | Indicates if SHA Accelerator is busy or not | 0x0018 | RO |
| SHA_DMA_START_REG | Starts the SHA accelerator for DMA-SHA operation | 0x001C | WO |
| SHA_START_REG | Starts the SHA accelerator for Typical SHA operation | 0x0010 | WO |
| SHA_DMA_CONTINUE_REG | Continues SHA operation (only effective in DMA-SHA mode) | 0x0020 | WO |
| SHA_INT_CLEAR_REG | DMA-SHA interrupt clear register | 0x0024 | WO |
| SHA_INT_ENA_REG | DMA-SHA interrupt enable register | 0x0028 | R/W |
| **Version Register** | | | |
| SHA_DATE_REG | Version control register | 0x002C | R/W |
| **Configuration Registers** | | | |
| SHA_MODE_REG | Defines the algorithm of SHA accelerator | 0x0000 | R/W |
| **Data Registers** | | | |
| SHA_DMA_BLOCK_NUM_REG | Block number register (only effective for DMA-SHA) | 0x000C | R/W |
| SHA_H_O_REG | Hash value | 0x0040 | R/W |
| SHA_H_1_REG | Hash value | 0x0044 | R/W |
```