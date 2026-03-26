

# 30.6 Registers

The addresses in this section are relative to the RSA Digital Signature Peripheral (RSA_DS) base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 30.1. DSA_IV_m_REG (m: 0-3) (0x0630+4*m)

```
DSA_IV_m_REG (m: 0-3)
Writes IV block data. (WO)
```

## Register 30.2. DSA_SET_START_REG (0x0E00)

```
DSA_SET_START Configures whether to activate the RSA_DS peripheral.
0: No effect
1: Activate the RSA_DS peripheral
(WO)
```

## Register 30.3. DSA_SET_ME_REG (0x0E04)

```
DSA_SET_ME Configures whether to start the RSA_DS operation.
0: No effect
1: Start the RSA_DS operation
(WO)
```