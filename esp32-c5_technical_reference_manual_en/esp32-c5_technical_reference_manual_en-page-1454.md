

```markdown
Chapter 39 SDIO Slave Controller (SDIO)

GoBack

Figure 39.7-1. Procedure of Slave Sending Packets to Host

1. The slave CPU creates the linked list for the data packets to be sent to the host. For details, see Section 39.5.5.1.
2. The slave CPU updates the length of data to be sent using the register SDIO_SLC0_LEN_CONF_REG.
3. The slave CPU starts DMA by writing the 32-bit address of the first descriptor in linked list to SDIO_SLCORX_LINK_ADDR_REG or SDIO_SLC1RX_LINK_ADDR_REG and then configuring SDIO_SLCO_RXLINK_START or SDIO_SLC1_RXLINK_START to start DMA. For more information on DMA, please refer to Section 39.5.5.
4. The slave DMA sends an interrupt to the host.

Espressif Systems    1454
Submit Documentation Feedback    ESP32-C5 TRM (Version 1.0)
```