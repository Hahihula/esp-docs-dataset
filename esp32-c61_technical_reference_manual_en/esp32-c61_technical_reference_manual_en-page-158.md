

```markdown
| AHB_DMA_PERI_IN_SEL_CHn | Peripheral |
|--------------------------|------------|
|                          |            |
| 0                        | Dummy-0    |
| 1                        | GP-SPI     |
| 2                        | Dummy-2    |
| 3                        | I2S        |
| 4 ~ 6                    | Dummy-4 ~ 6|
| 7                        | SHA        |
| 8                        | ADC        |
| 9 ~ 15                   | Dummy-9 ~ 15|
| 16 ~ 63                  | Invalid    |

## 3.4.3 Memory-to-Memory Data Transfer

The GDMA controller also allows memory-to-memory data transfer. Such data transfer can be enabled by setting `AHB_DMA_MEM_TRANS_EN_CHn`, which connects the output of transmit channel n to the input of receive channel n. Note that a transmit channel is only connected to the receive channel with the same number (n), and `AHB_DMA_PERI_IN_SEL_CHn` and `AHB_DMA_PERI_OUT_SEL_CHn` should be configured to the same value corresponding to “Dummy”.

## 3.4.4 Enabling GDMA

The software uses the GDMA controller through linked lists. When the GDMA controller receives data, software loads an inlink, configures the `AHB_DMA_INLINK_ADDR_CHn` field with the address of the first receive descriptor, and sets the `AHB_DMA_INLINK_START_CHn` bit to enable GDMA. When the GDMA controller transmits data, software loads an outlink, prepares data to be transmitted, configures the `AHB_DMA_OUTLINK_ADDR_CHn` field with the address of the first transmit descriptor, and sets the `AHB_DMA_OUTLINK_START_CHn` bit to enable GDMA. The `AHB_DMA_INLINK_START_CHn` bit and `AHB_DMA_OUTLINK_START_CHn` bit are cleared automatically by hardware.

In some cases, you may want to append more descriptors to a DMA transfer that is already started. Naively, it would seem to be possible to do this by clearing the EOF bit of the final descriptor in the existing list and setting its next descriptor address pointer field (DW2) to the first descriptor of the to-be-added list. However, this strategy fails if the existing DMA transfer is almost or entirely finished. Instead, the GDMA controller has specialized logic to make sure a DMA transfer can be continued or restarted: if the transfer is ongoing, the controller will make sure to take the appended descriptors into account; if the transfer has already finished, the controller will restart with the new descriptors. This is implemented by the Restart function.

When using the Restart function, software needs to rewrite the address of the first descriptor in the new list to DW2 of the last descriptor in the loaded list, and set `AHB_DMA_INLINK_RESTART_CHn` bit or `AHB_DMA_OUTLINK_RESTART_CHn` bit (these two bits are cleared automatically by hardware). As shown in Figure 3.4-2, by doing so hardware can obtain the address of the first descriptor in the new list when reading the last descriptor in the loaded list, and then read the new list.
```