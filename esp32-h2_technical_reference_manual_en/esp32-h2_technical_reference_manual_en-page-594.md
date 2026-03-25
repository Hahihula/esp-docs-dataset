

# 19.10 Registers

The addresses in this section are relative to the AES accelerator base address provided in Table 4.3-2 in Chapter 4 System and Memory.

## Register 19.1. AES_KEY_n_REG (n: 0-7) (0x0000+4*n)

```
AES_KEY_n_REG (n: 0-7)
31                                 0
+---------------------------------------+
|               0x00000000              |
+---------------------------------------+
Reset
```

**AES_KEY_n_REG (n: 0-7)** Represents AES key data. (R/W)

## Register 19.2. AES_TEXT_IN_m_REG (m: 0-3) (0x0020+4*m)

```
AES_TEXT_IN_m_REG (m: 0-3)
31                                 0
+---------------------------------------+
|               0x00000000              |
+---------------------------------------+
Reset
```

**AES_TEXT_IN_m_REG (m: 0-3)** Represents the source text data when the AES accelerator operates in the Typical AES working mode. (R/W)

## Register 19.3. AES_TEXT_OUT_m_REG (m: 0-3) (0x0030+4*m)

```
AES_TEXT_OUT_m_REG (m: 0-3)
31                                 0
+---------------------------------------+
|               0x00000000              |
+---------------------------------------+
Reset
```

**AES_TEXT_OUT_m_REG (m: 0-3)** Represents the result text data when the AES accelerator operates in the Typical AES working mode. (RO)