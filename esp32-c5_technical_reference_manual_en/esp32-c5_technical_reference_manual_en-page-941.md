

```markdown
Chapter 27 Digital Signature Algorithm (DSA)
GoBack

## 27.6 Registers

The addresses in this section are relative to Digital Signature Algorithm base address provided in Table 6.3-2 in Chapter 6 System and Memory.

Register 27.1. DS_SET_START_REG (0xOEOO)

DS_SET_START Configures whether or not to activate the DSA peripheral.
0: Invalid
1: Activate the DSA peripheral
(WT)

Register 27.2. DS_SET_CONTINUE_REG (0xOE04)

DS_SET_CONTINUE Configures whether or not to continue the DSA operation.
0: No effect
1: Continue the DSA operation
(WT)

Register 27.3. DS_SET_FINISH_REG (0xOE08)

DS_SET_FINISH Configures whether or not to end the DSA operation.
0: No effect
1: End the DSA operation
(WT)
```