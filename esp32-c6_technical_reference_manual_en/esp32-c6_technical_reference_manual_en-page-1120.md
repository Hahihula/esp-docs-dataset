

```markdown
SDIO_SLCO_LEN_CONF_REG.

3. The slave CPU starts DMA by writing the 32-bit address of the first descriptor in linked list to SDIO_SLCORX_LINK_ADDR_REG or SDIO_SLC1RX_LINK_ADDR_REG and then configuring SDIO_SLCO_RXLINK_START or SDIO_SLC1_RXLINK_START to start DMA. For more information on DMA, please refer to Section 34.5.5.

4. The slave DMA sends an interrupt to the host.

5. After the host received the interrupt, it reads from SLCHOST_SLCOHOST_INT_ST_REG, SLCHOST_SLC1HOST_INT_ST_REG, and SLCHOST_PKT_LEN_REG the following information:

*   SLCHOST_SLCO/1HOST_INT_ST_REG: Interrupt status register. If the SLCHOST_SLCO/1_RX_NEW_PACKET_INT_ST bit is 1, this indicates that the slave has packets to send.
*   SLCHOST_PKT_LEN_REG: Packet length accumulator register. The current value minus the value of last time equals the packet length sent this time.

6. The host clears the interrupt through CMD52.

7. The host fetches packets from the slave through CMD53. During the transmission, when the slave determines that the valid data of the current packet is over, the subsequent bits will be padded with invalid data 0x0. For how to determine the end of valid data, please refer to Section 34.5.5.3.

8. After the packets is transmitted, the slave DMA sends an interrupt to the CPU, and the CPU can recycle the buffer at this time.
```

**Notes:**

*   It is not recommended to set all of the eof bits to 0 in the linked list. Otherwise, the DMA may send the data of the next packet to the current command, which may cause errors. In cases where all of the eof bits is set to 0, the slave software should align the length of each packet to the size of the data block by padding data, to prevent the DMA from sending the data of the next packet to the current command. When the host sends CMD53 to read data, it should accurately control the number of data blocks in each packet, do not read more or less data blocks. Besides, the host should be able to identify the padded data.
*   It is recommended that a CMD53 command only should transmit one data packet and each data packet should use only one linked list so as to avoid unknown exceptions caused by complex transmission.
*   It is not recommended to send multiple packets through one linked list because it may be difficult for the host and software to split between the data packets. In cases where this has to be done, the software should set the eof bit when creating the linled list to divide the data packets so that the DMA can pad data packets accordingly (it is recommended that the length of each data packet should be aligned to the size of the data block to avoid data padding by DMA), and the host should be able to identify the padded data.

## 34.7.2 Receiving Packets from SDIO Host

Transmission of packets from the host to slave is initiated by the host. The slave receives data via DMA and stores it in RAM. After transmission is completed, the CPU will be interrupted to process the data. The whole procedure is demonstrated in Figure 34.7-2.
```