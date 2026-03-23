

```markdown
* if read 0, read the trace packets from `TRACE_MEM_START_ADDR_REG`
* if read 1, and the loop mode is enabled, then the old trace packets are overwritten. In this case, read the `TRACE_MEM_CURRENT_ADDR_REG` to know the last writing address, and use this address as the first address to decode

• Use the decoder to decode data packets
    - The decoder reads all data packets starting from the first address, and reconstructs the data stream with the binary file
    - As mentioned in 2.6, the encoder writes 14 zero bytes to the memory partition boundary every time when 128 packets are transmitted. Given this fact, the first non-zero byte after 14 zero bytes should be the header of a new packet
```