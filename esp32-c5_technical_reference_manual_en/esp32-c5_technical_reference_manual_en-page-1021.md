

```markdown
Register 31.19. KEYMNG_START_REG (0x0024)

KEYMNG_START Write 1 to start Key Manager operation at IDLE phase.
(WT)

KEYMNG_CONTINUE Write 1 to continue the operation of Key Manager at LOAD/GAIN phase.
(WT)

Register 31.20. KEYMNG_STATE_REG (0x0028)

KEYMNG_STATE Represents the state of Key Manager.

O: IDLE
1: LOAD
2: GAIN
3: BUSY
(RO)

Register 31.21. KEYMNG_RESULT_REG (0x002C)

KEYMNG_PROC_RESULT Represents the procedure result of Key Manager, valid only when Key
Manager procedure is done.

O: Key Manager procedure failed.
1: Key Manager procedure succeeded.
(RO/SS)
```