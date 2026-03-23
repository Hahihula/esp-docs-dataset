

```markdown
Chapter 21 HMAC Accelerator (HMAC)

GoBack

21.3.1 Padding Bits

The HMAC module uses SHA-256 as hash algorithm. If the input message is not a multiple of 512 bits, the user must apply a SHA-256 padding algorithm in software. The SHA-256 padding algorithm is the same as described in Section Padding the Message of FIPS PUB 180-4. In downstream mode, users do not need to input any message or apply padding. The HMAC module uses a default 32-byte pattern of 0x00 for re-enabling JTAG and a 32-byte pattern of 0xff for deriving the AES key for the DS module.

As shown in Figure 21.3-1, suppose the length of the unpadded message is m bits. Padding steps are as follows:

1. Append one bit of value “1” to the end of the unpadded message.
2. Append k bits of value “0”, where k is the smallest non-negative number which satisfies
   m + 1 + k ≡ 448 (mod 512).
3. Append a 64-bit integer value as a binary block. This block consists of the length of the unpadded message as a big-endian binary integer m.

![Figure 21.3-1. HMAC SHA-256 Padding Diagram](image)

In upstream mode, if the length of the unpadded message is a multiple of 512 bits, users can configure hardware to apply SHA padding by writing 1 to HMAC_SET_MSGGAE_END_REG or do padding work themselves by writing 1 to HMAC_SET_MESSAGE_PAD_REG. If the length is not a multiple of 512 bits, SHA padding must be manually applied by the user. After the user prepared the padding data, they should complete the subsequent configuration according to the Section 21.2.5.

21.3.2 HMAC Algorithm Structure

The structure of the implemented algorithm in the HMAC module is shown in Figure 21.3-2. This is the standard HMAC algorithm as described in RFC 2104.
```