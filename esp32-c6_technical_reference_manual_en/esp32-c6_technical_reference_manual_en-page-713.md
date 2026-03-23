

# 24.6 Registers

The addresses in this section are relative to Digital Signature base address provided in Table 5.3-2 in Chapter 5 System and Memory.

## Register 24.1. DS_IV_m_REG (m: 0-3) (0x0630+4*n)

```
DS_IV_m_REG (m: 0-3)
```

| Bit 31 | Value |
|--------|-------|
|   0     | Reset |
| 0x00000000 |       |

**DS_IV_m_REG** Writes IV block data. (WO)

## Register 24.2. DS_SET_START_REG (0x0E00)

```
(reserved)
DS_SET_START
```

| Bit 31 | Value |
|--------|-------|
|   1     | Reset |
| 0x00000000 |       |

**DS_SET_START** Configures whether or not to activate the DS peripheral.  
0: Invalid  
1: Activate the DS peripheral (WO)

## Register 24.3. DS_SET_ME_REG (0x0E04)

```
(reserved)
DS_SET_ME
```

| Bit 31 | Value |
|--------|-------|
|   1     | Reset |
| 0x00000000 |       |

**DS_SET_ME** Configures whether or not to start DS operation.  
0: Invalid  
1: Start DS operation (WO)