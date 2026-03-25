

```markdown
Register 2.93. tcontrol (0x7A5)

| 31 | 8 | 7 | 6 | 1 | 0 |
|-----|----|----|----|----|----|
|     |    | mpte | (reserved) | rite | Reset |
| 0x000000 | O | 0x00 | O |

mpte Configures whether to enable the machine mode previous trigger.
When CPU is taking a machine mode trap, the value of mte is automatically pushed into this.
When CPU is executing MRET, its value is popped back into mte, so this becomes 0.
(R/W)

mte Configures whether to enable the machine mode trigger.
When CPU is taking a machine mode trap, its value is automatically pushed into mpte, so this becomes 0 and triggers with action=0 are disabled globally.
When CPU is executing MRET, the value of mpte is automatically popped back into this.
(R/W)

Register 2.94. MCONTEXT (0x7A8)

| 31 | 6 | 5 | 0 |
|-----|----|----|----|
|     |    | context | Reset |
| 0x0 | O | 0x0 |

Reserved Read as 0. (RO)
context Writable in M mode and Debug Mode. Machine mode software can write a context number to this register, which can be used to set triggers that only fire in that specific context. (R/W)
```