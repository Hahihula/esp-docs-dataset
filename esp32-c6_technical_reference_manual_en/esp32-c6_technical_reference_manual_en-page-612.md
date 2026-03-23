

```markdown
Chapter 18 Debug Assistant (ASSIST_DEBUG)
GoBack

In loop mode, data looping several times in the storage memory may cause residual data, which can interfere with packet parsing. For example, the lower 32 bits of a HP CPU packet are overwritten, thus making its higher 32 bits residual data. Therefore, users need to filter out the possible residual data in order to determine the starting position of the first valid packet with `MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG`. Once the starting position of the packet is identified, check the anchored bit value of the packet. If it is 1, the data will be retained. If it is 2, it will be dumped.

The process of packet parsing is described below:

- Determine whether there is a data overflow with `MEM_MONITOR_LOG_MEM_FULL_FLAG`. If no, the address space to read is `MEM_MONITOR_LOG_MEM_START_REG ~ MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG - 4`. If yes and the loop mode is enabled, the address space is `MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG ~ MEM_MONITOR_LOG_MEM_END_REG` and `MEM_MONITOR_LOG_MEM_START_REG ~ MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG - 4`. If yes and loop mode is not enabled, the address space is `MEM_MONITOR_LOG_MEM_START_REG ~ MEM_MONITOR_LOG_MEM_END_REG`.

- Read and parse data from the starting address. Read 32 bits each time.

After packet parsing is completed, clear the `MEM_MONITOR_LOG_MEM_FULL_FLAG` flag bit by setting `MEM_MONITOR_CLR_LOG_MEM_FULL_FLAG`.
```