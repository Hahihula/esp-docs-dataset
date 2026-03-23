

```markdown
Chapter 21 HMAC Accelerator (HMAC) GoBack

(c) Poll Status register `HMAC_QUERY_BUSY_REG` until it reads 0.  
(d) Different message blocks will be generated, depending on whether the size of the to-be-processed message is a multiple of 512 bits.

• If the bit length of the message is a multiple of 512 bits, there are three possible options:  
  i. If `Block_n+1` exists, write 1 to register `HMAC_SET_MESSAGE_ING_REG` to make $n = n + 1$, and then jump to step 4.(b).  
  ii. If `Block_n` is the last block of the message and users expects to apply SHA padding in hardware, write 1 to register `HMAC_SET_MESSAGE_END_REG`, and then jump to step 6.  
  iii. If `Block_n` is the last block of the padded message and SHA padding has been applied by users, write 1 to register `HMAC_SET_MESSAGE_PAD_REG`, and then jump to step 5.  

• If the bit length of the message is not a multiple of 512 bits, there are three possible options as follows. Note that in this case, the user is required to apply SHA padding to the message, after which the padded message length should be a multiple of 512 bits.  
  i. If there is only one message block in total which has included all padding bits, write 1 to register `HMAC_ONE_BLOCK_REG`, and then jump to step 6.  
  ii. If `Block_n` is the second last padded block, write 1 to register `HMAC_SET_MESSAGE_PAD_REG`, and then jump to step 5.  
  iii. If `Block_n` is neither the last nor the second last message block, write 1 to register `HMAC_SET_MESSAGE_ING_REG` and define $n = n + 1$, and then jump to step 4.(b).  

5. Apply SHA padding to message:  
   (a) Users apply SHA padding to the last message block as described in Section 21.3.1, write this block to register `HMAC_WDATA0~15_REG`, and then write 1 to register `HMAC_SET_MESSAGE_ONE_REG`. Then the HMAC module will process this message block.  
   (b) Jump to step 6.  

6. Read hash result in upstream mode:  
   (a) Poll Status register `HMAC_QUERY_BUSY_REG` until it reads 0.  
   (b) Read hash result from register `HMAC_RDATA0~7_REG`.  
   (c) Write 1 to register `HMAC_SET_RESULT_FINISH_REG` to finish calculation. The result will be cleared at the same time.  
   (d) Upstream mode operation is completed.  

Note:  
The SHA accelerator can be called directly, or used internally by the DS module and the HMAC module. However, they can not share the hardware resources simultaneously. Therefore, the SHA module must not be called neither by the CPU nor by the DS module when the HMAC module is in use.  

## 21.3 HMAC Algorithm Details
```