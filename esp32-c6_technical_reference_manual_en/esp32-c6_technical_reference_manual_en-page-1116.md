

```markdown
34.5.5.3 Data Padding and Discarding

In order to transfer data in blocks, both the host and the slave need to pad the data sent on the SDIO bus into entire blocks. The slave will automatically pad data when sending the packet, and automatically discard the padded data after receiving packets.

- When the host sends a data packet to the slave through CMD53 and the amount of data reaches the length of the data packet, the SDIO slave considers that the valid data of the current data packet is over. At this time, DMA will write back the current linked list descriptor, set the eof bit of the current descriptor to 1, and generate SLCO/1_TX_SUC_EOF_INT interrupt. After it determines that the valid data is over, the remaining data of the current packet will be considered as invalid data, and will not be received into the buffer by DMA. The slave will not restart receiving data into the next buffer until the next CMD53.

  - For incremental-address packets, the slave determines valid data based on the address. The data with the address greater than or equal to 0x1F800 is considered as invalid data and will be discarded. Therefore, the host should set the CMD53 start address field to 0x1F800 – Packet_length (unit: byte). The data flow of incremental-address packets on SDIO bus is shown in Figure 34.5-7.

![Figure 34.5-7. Data Flow of Sending Incremental-address Packets From Host to Slave](image)

- For fixed-address packets, the slave considers the first 3 bytes of the data packet as the packet length (including the first 3 bytes, which will also be stored in the buffer specified by the linked list). After the length of the received data reaches the packet length, the subsequent data will be considered as invalid and discarded.

- When the host receives data packets (including incremental-address packets and fixed-address packets) from the slave through CMD53 and DMA reads the last byte of a buffer and the eof bit of the DMA linked list descriptor is 1, the SDIO slave will consider the valid data of the current packet is over. At this time, DMA will write back the current descriptor and generate SLCO/1_RX_EOF_INT interrupt. After it is determined that the valid data is over, the remaining bits of the current data packet will be padded with invalid data 0x0, and will not be read from the buffer via DMA. The slave will restart to read data from the buffer via DMA until the next CMD53.

Note: When the host receives either incremental-address or fixed-address data packets from the slave, the eof bit of the DMA linked list descriptor is always considered as the basis for determining the end of data, rather than the address 0x1F800. Therefore, when the host sends multiple CMD53s to obtain multiple data packets, as long as the DMA does not encounter the eof bit is 1 in the descriptors, the slave will obtain the data from buffers in sequence according to the linked list and then transmit them to the host; when the DMA encounters the eof bit is 1, the data will be fetched from the corresponding buffer, and then invalid data will be added to complete the current CMD53 command, and the next CMD53 command will take data from the buffer pointed to by the next descriptor.
```