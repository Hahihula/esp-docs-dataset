

```markdown
CPU loads available buffers on linked list

CPU notifies DMA of refreshed linked list

CPU refreshes available buffers
```

Figure 34.7-3. Loading Receiving Buffer

The CPU first needs to append new buffer segments at the end of the linked list that is being used by DMA and is available for receiving data.

The CPU then needs to notify the DMA that the linked list has been updated. This can be done by setting `SDIO_SLCO_TXLINK_RESTART` or `SDIO_SLC1_TXLINK_RESTART`. Please note that when the CPU initiates DMA to receive packets for the first time, `SDIO_SLCO_TXLINK_START` or `SDIO_SLC1_TXLINK_START` should be set to 1.

**Notes:** Use the `_RESTART` field to restart DMA only in the two scenarios:

*   DMA is suspended by configuration of the `_STOP` field.
*   DMA is suspended as a result of insufficient linked list descriptors. Users can restart it after descriptors are added.

Lastly, the CPU refreshes any available buffer information by writing to the `SDIO_SLCOTOKEN1_REG` or `SDIO_SLC1TOKEN1_REG` register.
```