

```markdown
Chapter 24 HMAC Accelerator (HMAC)

GoBack

i. Write to register HMAC_SET_MESSAGE_PAD_REG, and continue message transmission (jump back to step(c)).
• If Block_n is neither the last nor the second last message block:
    i. Write the 512-bit Block_n to register HMAC_WR_MESSAGE_n_REG (n: 0-15). Write 1 to register HMAC_SET_MESSAGE_ONE_REG, to trigger the processing of this message block.
    ii. Poll Status register HMAC_QUERY_BUSY_REG until it reads 0.
    iii. Write 1 to register HMAC_SET_MESSAGE_ING_REG, and continue message transmission (jump back to step(c)).

2. Read hash result in upstream mode:
(a) Poll Status register HMAC_QUERY_BUSY_REG until it reads 0.
(b) Read hash result from register HMAC_RD_RESULT_n_REG (n: 0-7).
(c) Write 1 to register HMAC_SET_RESULT_FINISH_REG to finish calculation. The result will be cleared at the same time.
(d) Upstream mode operation is completed.

Note:
The SHA accelerator can be called directly, or used internally by the DSA module and the HMAC module. However, they can not share the hardware resources simultaneously. Therefore, the SHA module must not be called neither by the CPU nor by the DSA module when the HMAC module is in use.

24.6 HMAC Algorithm Details

24.6.1 Padding Bits

The HMAC module uses SHA-256 as hash algorithm. If the input message is not a multiple of 512 bits, the user must apply a SHA-256 padding algorithm in software. The SHA-256 padding algorithm is the same as described in Section Padding the Message of FIPS PUB 180-4. In downstream mode, users do not need to input any message or apply padding. The HMAC module uses a default 32-byte pattern of 0x00 for re-enabling JTAG and a 32-byte pattern of 0xff for deriving the AES key for the DSA module.

For the convenience of reading, here we will briefly describe the process of message padding. As shown in Figure 24.6-1, suppose the length of the unpadded message is m bits. Padding steps are as follows:

1. Append one bit of value “1” to the end of the unpadded message.
2. Append k bits of value “0”, where k is the smallest non-negative number which satisfies m + 1 + k ≡ 448 (mod512).
3. Append a 64-bit integer value as a binary block. This block consists of the length of the unpadded message as a big-endian binary integer value m.

In upstream mode, if the length of the unpadded message is a multiple of 512 bits, users can configure hardware to apply SHA padding by writing 1 to HMAC_SET_MESSAGE_END_REG or do padding work themselves by writing 1 to HMAC_SET_MESSAGE_PAD_REG. If the length is not a multiple of 512 bits, SHA
```