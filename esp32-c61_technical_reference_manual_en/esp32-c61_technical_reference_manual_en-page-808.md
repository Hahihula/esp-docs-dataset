

```markdown
Chapter 22 Elliptic Curve Digital Signature Algorithm (ECDSA) GoBack


Register 22.2. ECDSA_START_REG (0x001C)

(reserved)
3   2   1   0
-------------------------------------------------
|     |     |     |
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 Reset

ECDSA_START Configures whether to start the ECDSA operation. This bit will be self-cleared after configuration.
O: No effect
1: Start the ECDSA operation
(WT)

ECDSA_LOAD_DONE Write 1 to generate a signal indicating the ECDSA accelerator's LOAD operation is done. This bit will be self-cleared after configuration. (WT)

ECDSA_GET_DONE Write 1 to generate a signal indicating the ECDSA accelerator's GAIN operation is done. This bit will be self-cleared after configuration. (WT)


Register 22.3. ECDSA_CLK_REG (0x0008)

(reserved)
3   2   1   0
-------------------------------------------------
|     |     |     |
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 Reset

ECDSA_CLK_GATE_FORCE_ON Configures whether to force on ECDSA memory clock gate.
O: No effect
1: Force on
(R/W)
```