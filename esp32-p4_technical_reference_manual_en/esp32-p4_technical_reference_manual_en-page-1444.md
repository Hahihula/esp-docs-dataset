

```markdown
Register 25.9. AES_AAD_BLOCK_NUM_REG (0x00A0)

31                                 0
+-----------------------------------------------+
|       0x00000000        |Reset|
+-----------------------------------------------+

AES_AAD_BLOCK_NUM Stores the ADD block number for the GCM operation. For details, see Section 25.7.4. (R/W)


Register 25.10. AES_REMAINDER_BIT_NUM_REG (0x00A4)

31                                 7   6        0
+-----------------------------------------------+
|       0x00000000        |Reset|
+-----------------------------------------------+

AES_REMAINDER_BIT_NUM Stores the Remainder Bit Number for the GCM operation. For details, see Section 25.7.5. (R/W)


Register 25.11. AES_TRIGGER_REG (0x0048)

31                                 1   0
+-----------------------------------------------+
|       0x00000000        |Reset|
+-----------------------------------------------+

AES_TRIGGER Configures whether to start AES operation.
O: No effect
1: Start
(WT)
```