

# 32.8 Registers

The addresses in this section are relative to the External Memory Encryption and Decryption base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 32.1. XTS_AES_PLAIN_n_REG (n: 0-15) (0x0300+4*n)

XTS_AES_PLAIN_n Configures the nth 32-bit piece of plain text. (R/W)

## Register 32.2. XTS_AES_LINESIZE_REG (0x0340)

XTS_AES_LINESIZE Configures the data size of one encryption operation.

```
reserved
0: 16 bytes
1: 32 bytes
2: 64 bytes
3: Invalid
(R/W)
```