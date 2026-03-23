

# 22.6 Registers

The addresses in this section are relative to Digital Signature base address provided in Table 3.3-3 in Chapter 3 System and Memory.

## Register 22.1. DS_IV_m_REG (m: 0-3) (0x0630+4*m)

DS_IV_m_REG (m: 0-3)

```
31
+---------------------------------------------------------------+
| 0 | 0x00000000 | Reset |
+---------------------------------------------------------------+
```

**DS_IV_m_REG (m: 0-3)** IV block data. (WO)

## Register 22.2. DS_SET_START_REG (0x0E00)

```
31
+---------------------------------------------+
| (reserved)                                 | DS_SET_START |
|                                          1   0         | Reset      |
+---------------------------------------------+
```

**DS_SET_START** Write 1 to this register to activate the DS peripheral. (WO)

## Register 22.3. DS_SET_ME_REG (0x0E04)

```
31
+---------------------------------------------+
| (reserved)                                 | DS_SET_ME   |
|                                          1   0         | Reset      |
+---------------------------------------------+
```

**DS_SET_ME** Write 1 to this register to start DS operation. (WO)