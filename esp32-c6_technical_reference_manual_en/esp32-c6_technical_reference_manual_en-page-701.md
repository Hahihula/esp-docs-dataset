

```markdown
| Name              | Description                  | Address   | Access |
|-------------------|------------------------------|-----------|--------|
| Version Register  |                              |           |        |
| SHA_DATE_REG      | Version control register     | 0x002C    | R/W    |

## 23.6 Registers

The addresses in this section are relative to the SHA accelerator base address provided in Table 5.3-2 in Chapter 5 System and Memory.

### Register 23.1. SHA_START_REG (0x0010)

```
31                                 1                                 0
+-----------------------------------------------+
| (reserved)                                     | SHA_START |
+-----------------------------------------------+
| 0 0 ... 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset     |
+-----------------------------------------------+

SHA_START Write 1 to start Typical SHA calculation. (WO)
```

### Register 23.2. SHA_CONTINUE_REG (0x0014)

```
31                                 1                                 0
+-----------------------------------------------+
| (reserved)                                     | SHA_CONTINUE |
+-----------------------------------------------+
| 0 0 ... 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset     |
+-----------------------------------------------+

SHA_CONTINUE Write 1 to continue Typical SHA calculation. (WO)
```

### Register 23.3. SHA_BUSY_REG (0x0018)

```
31                                 1                                 0
+-----------------------------------------------+
| (reserved)                                     | SHA_BUSY_STATE |
+-----------------------------------------------+
| 0 0 ... 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset     |
+-----------------------------------------------+

SHA_BUSY_STATE Represents the states of SHA accelerator.
0: idle
1: busy
(RO)
```
```