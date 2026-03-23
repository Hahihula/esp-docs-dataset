

# 18.8 Registers

The addresses in this section are relative to the AES accelerator base address provided in Table 3.3-3 in Chapter 3 System and Memory.

## Register 18.1. AES_KEY_n_REG (n: 0-7) (0x0000+4*n)

```
AES_KEY_n_REG (n: 0-7)
31
0x00000000
Reset
```

**AES_KEY_n_REG (n: 0-7)** Stores AES key data. (R/W)

## Register 18.2. AES_TEXT_IN_m_REG (m: 0-3) (0x0020+4*m)

```
AES_TEXT_IN_m_REG (m: 0-3)
31
0x00000000
Reset
```

**AES_TEXT_IN_m_REG (m: 0-3)** Stores the source text data when the AES Accelerator operates in the Typical AES working mode. (R/W)

## Register 18.3. AES_TEXT_OUT_m_REG (m: 0-3) (0x0030+4*m)

```
AES_TEXT_OUT_m_REG (m: 0-3)
31
0x00000000
Reset
```

**AES_TEXT_OUT_m_REG (m: 0-3)** Stores the result text data when the AES Accelerator operates in the Typical AES working mode. (RO)