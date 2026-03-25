

# 24.6 Registers

The addresses in this section are relative to Digital Signature Algorithm base address provided in Table 4.3-2 in Chapter 4 System and Memory.

## Register 24.1. DS_IV_m_REG (m: 0-3) (0x0630+4*m)

```
DS_IV_m_REG (m: 0-3)
```

| Bit 31 | ... | Bit 0 |
|--------|-----|-------|
|   0     | ... | Reset |

`DS_IV_m_REG (m: 0-3)` Writes IV block data. (WO)

## Register 24.2. DS_SET_START_REG (0x0E00)

```
(reserved)
DS_SET_START
```

| Bit 31 | ... | Bit 0 |
|--------|-----|-------|
|   1     | ... | Reset |

`DS_SET_START` Configures whether to activate the DSA peripheral.

- O: No effect
- 1: Activate the DSA peripheral (WO)

## Register 24.3. DS_SET_ME_REG (0x0E04)

```
(reserved)
DS_SET_ME
```

| Bit 31 | ... | Bit 0 |
|--------|-----|-------|
|   1     | ... | Reset |

`DS_SET_ME` Configures whether to start the DSA operation.

- O: No effect
- 1: Start the DSA operation (WO)