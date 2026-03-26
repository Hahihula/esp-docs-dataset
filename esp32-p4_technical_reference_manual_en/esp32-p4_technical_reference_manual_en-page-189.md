

```markdown
## 2.8.6 Decode Data Packets

- Find the first address to decode  
  - Read the `TRACE_MEM_FULL_INTR_RAW` bit of the `TRACE_INTR_RAW_REG` register to know if the trace memory is full  
    * if read 0, read the trace packets from `TRACE_MEM_START_ADDR_REG`  
    * if read 1, and the loop mode is enabled, then the old trace packets are overwritten. In this case, read the `TRACE_MEM_CURRENT_ADDR_REG` to know the last writing address, and use this address as the first address to decode

- Use the decoder to decode data packets  
  - The decoder reads all data packets starting from the first address, and reconstructs the data stream with the binary file  
  - As mentioned in 2.6, the encoder writes 14 zero bytes to the memory partition boundary every time when 128 packets are transmitted. Given this fact, the first non-zero byte after 14 zero bytes should be the header of a new packet

## 2.8.7 AHB Configuration

ESP32-P4 encoder supports the AHB bus. There are some optional configurations to control the transmission bandwidth of the encoder.

If there are many DMA masters, users can increase the bandwidth of Trace by setting AHB burst `TRACE_AHB_CONFIG_REG`.

- The `TRACE_HBURST` supports the following configurations:  
  - `0x0`: SINGLE  
  - `0x1`: INCR (length not defined)  
  - `0x2`: INCR4  
  - `0x4`: INCR8  
  - Others: reserved

Burst transfer means that once arbitration is successful, multiple words can be transferred continuously. For SINGLE, the length is 1; for INCR, the length is undefined; for INCR4, the length is 4; for INCR8, the length is 8. The longer the burst length, the better the bandwidth.

- When configured as INCR transfer, since INCR is a burst of indeterminate length, in order to avoid Trace occupying the bus for a long time, it will end the INCR transfer after the transfer length up to `TRACE_MAX_INCR`, and restart bus arbitration.

This is the configuration used to adjust the bandwidth. When the bandwidth is sufficient, it’s not required to do the configuration, and users can use the default configuration.
```