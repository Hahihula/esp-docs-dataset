**Chapter Title:**
Chapter 21 HMAC Accelerator (HMAC)

**Body Text with Steps and Instructions for HMAC Algorithm**

- **Step Description:** If Block_n is the last block of the padded message and the user has applied SHA padding in software, write 1 to register HMAC_SET_MESSAGE_PAD_REG, and then jump to step 5.
  - *If the bit length of the message is not a multiple of 512 bits, there are three possible options as follows. Note that in this case, the user should apply SHA padding to the message, after which the padded message length should be a multiple of 512 bits.*
    - If Block_n is the only message block, n = 1, and Block_1 has included all padding bits, write 1 to register HMAC_ONE_BLOCK_REG, and then jump to step 6.
    - If Block_n is the second to last padded block, write 1 to register HMAC_SET_MESSAGE_PAD_REG, and then jump to step 5.
    - If Block_n is neither the last nor the second to last message block, write 1 to register HMAC_SET_MESSAGE_ING_REG and define n = n + 1, and then jump to step 4.(b).

- **Step Description:** Apply SHA padding to message
  - (a) After applying SHA padding to the last message block as described in Section [21.3.1](#), write this block to register HMAC_WDATAO~15_REG, and then write 1 to register HMAC_SET_MESSAGE_ONE_REG. Then the HMAC module will calculate this message block.
  - (b) Jump to step 6.

- **Step Description:** Read hash result in upstream mode
  - (a) Poll Status register HMAC_QUERY_BUSY_REG. When the value of this register is 0, go to the next step.
  - (b) Read hash result from register HMAC_RDATAO~7_REG.
  - (c) Write 1 to register HMAC_SET_RESULT_FINISH_REG to finish calculation.
  - (d) Upstream mode operation is completed.

**Note:**
The SHA accelerator can be called directly, or used internally by the DS module and the HMAC module. However, they cannot share the hardware resources simultaneously. Therefore, SHA module can not be called by the CPU nor DS module when the HMAC module is in use.

**Subsection Title:** 21.3 HMAC Algorithm Details

**Subsection Subtitle:**
21.3.1 Padding Bits

**Body Text with Explanation and Figure Reference for Padding Steps**

The HMAC module uses SHA-256 as hash algorithm. If the input message is not a multiple of 512 bits, a SHA-256 padding algorithm must be applied in software. The SHA-256 padding algorithm is the same as described in Section [Padding the Message of FIPS PUB 180-4](#).

As shown in Figure **[21.3-1](#)**, suppose the length of the unpadded message is m bits. Padding steps are as follows:
1. Append one bit of value "1" to the end of the unpadded message;

**Footer:**
Espressif Systems
Page 887 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback