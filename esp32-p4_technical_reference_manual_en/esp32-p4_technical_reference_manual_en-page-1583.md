

```markdown
Register 34.10. HUK_DATE_REG (0x00FC)

HUK_DATE Version control register.
(R/W)
```

## 34.12.2 Key Manager Registers

The addresses in this section are relative to Key Manager base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section IX .

Register 34.11. KEYMNG_CLK_REG (0x0004)

KEYMNG_REG_CG_FORCE_ON Configures whether or not to force on register clock gate.
```
0: Not force on
1: Force on
(R/W)
```

KEYMNG_MEM_CG_FORCE_ON Configures whether or not to force on memory clock gate.
```
0: Not force on
1: Force on
(R/W)
```