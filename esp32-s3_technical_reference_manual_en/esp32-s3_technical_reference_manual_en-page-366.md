**Chapter Title:**
Chapter 3 GDMA Controller (DMA)

**Body Text:**

All peripherals with GDMA feature (i.e., SPI2, SPI3, UHCI0, I2S0, I2S1, LCD/CAM, AES, SHA, ADC, and RMT) do not have access permissions for Area 0 and Area 3, but their permissions for Area 1 and Area 2 can be independently managed. The permission control module contains registers to manage such access permissions for Area 1 and Area 2. For example, the PMS_EDMA_PMS_SPI2 ATTR1 field configures SPI2’s permissions to read and write Area 1. Specifically, when bit 0 of this field is 1, SPI2 is granted read permission; when bit 1 of this field is 1, SPI2 is granted write permission. Likewise, the PMS_EDMA_PMS_SPI2 ATTR2 field configures SPI2’s permissions to read and write Area 2.

Access violations are logged and can trigger the GDMA_ETXMEM_REJECT_INT interrupt. You can check the address where the access violation occurs; the peripheral involved, channel number and read or write attribute via GDMA_ETXMEM_REJECT_ADDR, GDMA_ETXMEM_REJECT_PERI_NUM, GDMA_ETXMENREJECT_CHANNEL_NUM, and GDMA_ETXMEM_REJECT ATTR respectively.

**Subsection Title:**
3.4.11 Seamless Access to Internal and External RAM

In some application scenarios, a data frame or packet contains data from both internal RAM and external RAM.
To ensure real-time data processing, GDMA is designed in such a way that some descriptors in the linked list can be used to access internal RAM, while the other descriptors in the same linked list can be used to access external RAM. This design allows seamless access to internal and external RAM.

**Subsection Title:**
3.4.12 Arbitration

To ensure timely response to peripherals running at a high speed with low latency (such as SPI, LCD/CAM), the GDMA controller implements a fixed-priority channel arbitration scheme. That is to say, each channel can be assigned a priority from 0 ~ 9. The larger the number, the higher the priority, and the more timely the response. When several channels are assigned the same priority, the GDMA controller adopts a round-robin arbitration scheme.

Please note that the overall throughput of peripherals with GDMA feature cannot exceed the maximum bandwidth of the GDMA, so that requests from low-priority peripherals can be responded to.

**Subsection Title:**
3.5 GDMA Interrupts

- GDMA_OUT_TOTAL_EOF_CHn_INT: Triggered when all data corresponding to a linked list (including multiple descriptors) have been sent via transmit channel n.
- GDMA_IN_DSCR_EMPTY_CHn_INT: Triggered when the size of the buffer pointed by receive descriptors is smaller than the length of data to be received via receive channel n.
- GDMA_OUT_DSCR_ERR_CHn_INT: Triggered when an error is detected in a transmit descriptor on transmit channel n.
- GDMA_IN_DSCR_ERR_CHn_INT: Triggered when an error is detected in a receive descriptor on receive channel n.
- GDMA_OUT_EOF_CHn_INT: Triggered when EOF in a transmit descriptor 1 and data corresponding to this descriptor have been sent via transmit channel n. If GDMA_OUT_EOF_MODE_CHn is 0, this interrupt will be triggered when the last byte of data corresponding to this descriptor enters GDMA’s transmit channel; if GDMA_OUT_EOF MODE CHn is 1, this interrupt is triggered when the last byte of data is taken from GDMA’s transmit channel.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version Information:**
366 ESP32-S3 TRM (Version 1.7)