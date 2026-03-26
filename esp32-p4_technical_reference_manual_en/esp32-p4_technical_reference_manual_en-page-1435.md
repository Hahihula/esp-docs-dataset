

```markdown
5. Check if DMA completes data transmission from AES to memory. At this time, DMA had already written the result data in memory, which can be accessed directly. For details on DMA, please refer to Chapter 4 GDMA Controller (GDMA-AHB, GDMA-AXI).

6. Clear interrupt by writing 1 to the `AES_INT_CLR_REG` register, if any AES interrupt occurred during the computation.

7. Release the AES accelerator by writing 1 to the `AES_DMA_EXIT_REG` register. After this, the content of the `AES_STATE_REG` register becomes 0. Note that, you can release DMA earlier, but only after Step 4 is completed.
```

## 25.6.7 GCM Operation Process

```markdown
1. Configure DMA chain and start DMA. For details on DMA, please refer to Chapter 4 GDMA Controller (GDMA-AHB, GDMA-AXI).

2. Initialize the AES accelerator-related registers:

   - Write 1 to the `AES_DMA_ENABLE_REG` register.
   - Configure the `AES_INT_ENA_REG` register to enable or disable the interrupt function.
   - Initialize registers `AES_MODE_REG` and `AES_KEY_n_REG`.
   - Write 6 to the `AES_BLOCK_MODE_REG` register.
   - Initialize the `AES_BLOCK_NUM_REG` register. Details about this register are described in Section 25.6.4 Block Number.
   - Initialize the `AES_AAD_BLOCK_NUM_REG` register. Details about this register are described in Section 25.7.4 AAD Block Number.
   - Initialize the `AES_REMAINDER_BIT_NUM_REG` register. Details about this register is described in Section 25.7.5 Number of Effective Bits of Incomplete Blocks.

3. Start operation by writing 1 to the `AES_TRIGGER_REG` register.

4. Wait for the completion of computation, which happens when the content of `AES_STATE_REG` becomes 2. For details on the working status of AES Accelerator, please refer to Table 25.6-2 Working Status under DMA-AES Working mode. At this step, no interrupt occurs.

5. Obtain the H value from the `AES_H_MEM` memory.

6. Generate J₀ and write it to the `AES_JO_MEM` memory.

7. Continue operating by writing 1 to the `AES_CONTINUE_OP_REG` register.

8. Wait for the completion of computation, which happens when the content of `AES_STATE_REG` becomes 2 or the AES interrupt occurs. For details on the working status of AES Accelerator, please refer to Table 25.6-2 Working Status under DMA-AES Working mode.

9. Obtain T₀ by reading `AES_TO_MEM`.

10. Check if DMA completes data transmission from AES to memory. At this time, DMA had already written the result data in memory, which can be accessed directly. For details on DMA, please refer to Chapter 4 GDMA Controller (GDMA-AHB, GDMA-AXI).
```