

```markdown
- L2_MEM_MONITOR_LOG_MEM_START_REG and L2_MEM_MONITOR_LOG_MEM_END_REG specify the storage space for recorded data. The storage space must be in the range of 0x4080_0000 ~ 0x4087_FFFF.
- Set L2_MEM_MONITOR_LOG_MEM_ADDR_UPDATE_REG to update the value in L2_MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG to L2_MEM_MONITOR_LOG_MEM_START_REG.

- Configure the permission for the L2MEM Monitor function of Debug Assistant module to access the HP L2MEM. Only when the access permission is enabled can the Debug Assistant module access the HP L2MEM. For more information, please refer to TEE_DMA_L2MEM_MON_PMS_W_REG and other relevant registers in Chapter 19 Permission Control (PMS).

5. Configure the writing mode for the recorded data: loop mode or non-loop mode.

- In loop mode, writing to the specified address space is performed in loops. When writing reaches the end address, it will return to the starting address and continue, overwriting the previously recorded data. Set L2_MEM_MONITOR_LOG_MEM_LOOP_ENABLE to enable loop mode. For example, there are 10 write operations (1 ~ 10) to address space 0 ~ 4 during bus access. After the 5th operation writes to address 4, the 6th operation will start writing from address 0. The 6th to 10th operations will overwrite the previous data written by the 1st to 5th operations.

- In non-loop mode, when writing reaches the end address, it will stop at the end address and dump the remaining data, not overwriting the previously recorded data. Clear L2_MEM_MONITOR_LOG_MEM_LOOP_ENABLE to use non-loop mode. For example, there are 10 write operations (1 ~ 10) to address space 0 ~ 4 during bus access. After the 5th operation writes to address 4, the 6th to 10th write operations will stop at address 4 and will not be performed any more. Therefore, the address 0 ~ 4 stores the values written by the 1 ~ 5 operations and the values of the 6 ~ 10 operations are dumped.

- See the example in 21.5.3.1 > step 5.

6. Configure bus enable registers.

- Enable DMA_2 and DMA_3 channel groups bus access logging with L2_MEM_MONITOR_LOG_DMA_2_ENA and L2_MEM_MONITOR_LOG_DMA_3_ENA respectively. They can be enabled at the same time.
```