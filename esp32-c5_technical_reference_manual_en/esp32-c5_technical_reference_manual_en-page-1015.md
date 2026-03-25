

```markdown
Register 31.11. KEYMNG_CLK_REG (0x0004)

KEYMNG_REG_CG_FORCE_ON   Configures whether or not to force on register clock gate.
    0: Not force on
    1: Force on
    (R/W)

KEYMNG_MEM_CG_FORCE_ON   Configures whether or not to force on memory clock gate.
    0: Not force on
    1: Force on
    (R/W)
```

```markdown
Register 31.12. KEYMNG_INT_RAW_REG (0x0008)

KEYMNG_PREP_DONE_INT_RAW   The raw interrupt status of KEYMNG_PREP_DONE_INT interrupt.
    (RO/WTC/SS)

KEYMNG_PROC_DONE_INT_RAW   The raw interrupt status of KEYMNG_PROC_DONE_INT interrupt.
    (RO/WTC/SS)

KEYMNG_POST_DONE_INT_RAW   The raw interrupt status of KEYMNG_POST_DONE_INT interrupt.
    (RO/WTC/SS)
```