

```markdown
the DMA linked list descriptor is set to 1, the SDIO slave considers the valid data of the current packet complete. At this point, the DMA writes back the current descriptor and generates the SLCO/1_RX_EOF_INT interrupt. After the SDIO slave determines that the valid data is complete, the remaining bits of the current data packet are padded with invalid data (0x0) and are not read from the buffer via DMA. The slave restarts reading data from the buffer via DMA when the next CMD53 command is sent by the host.

**Note:** When the host receives either incremental-address or fixed-address data packets from the slave, the `eof` bit of the DMA linked list descriptor is always used to determine the end of data, rather than the address 0x1F800. Therefore, when the host sends multiple CMD53 commands to obtain multiple data packets, as long as the DMA does not encounter the `eof` bit set to 1 in the descriptors, the slave obtains the data from buffers in sequence according to the linked list and transmits it to the host. When the DMA encounters the `eof` bit set to 1, the data is fetched from the corresponding buffer, and then invalid data is padded to complete the current CMD53 command. The next CMD53 command will fetch data from the buffer pointed to by the next descriptor.

### 39.5.6 SDIO Bus Timing

The SDIO bus operates at high speed, and PCB trace length can affect signal integrity by introducing latency. To ensure proper timing characteristics, the SDIO slave module supports configuration of the input sampling clock edge and output driving clock edge.

When incoming data changes near the rising edge of the clock, the slave samples on the falling edge, and vice versa, as shown in Figure 39.5-8.



![Figure 39.5-8. Sampling Timing Diagram](image-placeholder)

By default, the voltage level of the GPIO25 strapping pin determines the slave pin's sampling edge. You can also configure the sampling edge using the `SLCHOST_CONF_REG` register, with the following priority (from high to low): (1) Set `SLCHOST_FRC_POS_SAMP` to sample the corresponding signal at the rising edge; (2) Set `SLCHOST_FRC_NEG_SAMP` to sample at the falling edge.

The `SLCHOST_FRC_POS_SAMP` and `SLCHOST_FRC_NEG_SAMP` fields are five bits wide, corresponding to the CMD line and four DATA lines (0–3). Setting a bit causes the corresponding line to be sampled at the rising or falling clock edge.

The slave can also select which edge to drive the output lines, to compensate for any latency caused by the physical signal path. The output timing is shown in Figure 39.5-9.
```