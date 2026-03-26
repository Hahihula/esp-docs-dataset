

```markdown
Chapter 4 GDMA Controller (GDMA-AHB, GDMA-AXI) GoBack


| GDMA-AXI Channels                     | Modules       |
|----------------------------------------|---------------|
| GDMA-AXI Rx channel 0                  | LCD or CAM    |
| GDMA-AXI Tx channel 0                  | SPI2          |
| GDMA-AXI Rx channel 1                  | SPI3          |
| GDMA-AXI Tx channel 1                  | PARLIO        |
| GDMA-AXI Rx channel 2                  | AES           |
| GDMA-AXI Tx channel 2                  | SHA           |

Figure 4.1-2. Modules that Share GDMA-AXI Channels


## 4.2 Features

GDMA-AHB and GDMA-AXI have the following features:

*   Architecture:
    -   GDMA-AHB: AHB bus architecture
    -   GDMA-AXI: AXI bus architecture, which gives the possibility to complete up to 8 transactions out of order and up to 8 outstanding transactions

*   Programmable length of data to be transferred in bytes

*   Access via any address and size

*   Alignment:

    -   GDMA-AHB:
        *   Descriptor address: 1-word aligned
        *   Data address and length:
            -   Internal memory and non-encrypted external memory address space: no requirements
            -   Encrypted external memory address space: 16-byte aligned

    -   GDMA-AXI:
        *   Descriptor address: 2-word aligned
        *   Data address and length:
            -   Internal memory and non-encrypted external memory address space: no requirements
            -   Encrypted external memory address space: 16-byte aligned

*   Linked list of descriptors

*   When accessing memory, GDMA-AHB supports INCR4, INCR8, or INCR16 burst transfer, and GDMA-AXI supports INCR burst transfer

*   Three transmit channels and three receive channels for each controller
```