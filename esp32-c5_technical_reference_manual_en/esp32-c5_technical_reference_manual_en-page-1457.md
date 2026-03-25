

```markdown
Chapter 39 SDIO Slave Controller (SDIO)  GoBack


CPU loads available buffers on linked list

CPU notifies DMA of refreshed linked list

CPU refreshes available buffers

Figure 39.7-3. Loading Receiving Buffer


The CPU should append new buffer segments at the end of the linked list used by DMA and available for receiving data.

The CPU must then notify the DMA that the linked list has been updated. This can be done by setting SDIO_SLCO_TXLINK_RESTART or SDIO_SLC1_TXLINK_RESTART. When the CPU initiates DMA to receive packets for the first time, SDIO_SLCO_TXLINK_START or SDIO_SLC1_TXLINK_START should be set to 1.

Notes: Use the * _RESTART field to restart DMA only in the two scenarios:

• DMA is suspended by configuration of the * _STOP field. You can restart it after configuring the * _RESTART field.
• DMA is suspended due to insufficient linked list descriptors. You can restart it by adding descriptors and configuring the * _RESTART field.

Finally, the CPU refreshes available buffer information by writing to the SDIO_SLCTOKEN1_REG or SDIO_SLC1TOKEN1_REG register.
```