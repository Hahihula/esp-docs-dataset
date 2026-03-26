

```markdown
|Complete macroblock|
|--------------------|
|Incomplete macroblock|
|The part of hardware padding|

Figure 6.4-2. Padding Illustration (Overall)

1 | 2 | 3 | 3 | 3 | 3 | 3 |
4 | 5 | 6 | 6 | 6 | 6 | 6 |
7 | 8 | 9 | 9 | 9 | 9 | 9 |
7 | 8 | 9 | 9 | 9 | 9 | 9 |
7 | 8 | 9 | 9 | 9 | 9 | 9 |
7 | 8 | 9 | 9 | 9 | 9 | 9 |
7 | 8 | 9 | 9 | 9 | 9 | 9 |

Figure 6.4-3. Padding Illustration (Detail)

## 6.4.4 Peripheral-to-Memory and Memory-to-Peripheral Data Transfer

When `DMA2D_MEM_TRAN_EN_CHn` is 0, the 2D-DMA controller enters peripheral transfer mode. The transmit channel reads data from the memory and transmits it to peripherals, while the receive channel receives data from peripherals and stores it into the memory.

The transmit direction refers to data transfer from memory to peripheral, and the receive direction refers data transfer from peripheral to memory. A transmit channel transfers data in the specified memory location to a peripheral's transmitter via an outlinkn, whereas a receive channel transfers data received by a peripheral to the specified memory location via an inlinkn.

Every transmit and receive channel can be connected to any peripheral that supports 2D-DMA. Table 6.4-2 and Table 6.4-3 illustrate how to select the peripheral to be connected via registers. "Dummy-n" corresponds to register values for memory-to-memory data transfer. When a channel is connected to a peripheral, the rest
```