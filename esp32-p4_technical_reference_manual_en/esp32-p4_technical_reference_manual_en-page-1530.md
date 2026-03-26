

```markdown
Register 31.3. ECDSA_CLK_REG (0x0008)

ECDSA_CLK_GATE_FORCE_ON   Configures whether to force on ECC memory clock gate.
    0: No effect
    1: Force on
    (R/W)
```

```markdown
Register 31.4. ECDSA_INT_RAW_REG (0x000C)

ECDSA_PREP_DONE_INT_RAW   The raw interrupt status of the ECDSA_PREP_DONE_INT interrupt.
    (R/SS/WTC)

ECDSA_PROC_DONE_INT_RAW   The raw interrupt status of the ECDSA_PROC_DONE_INT interrupt.
    (R/SS/WTC)

ECDSA_POST_DONE_INT_RAW   The raw interrupt status of the ECDSA_POST_DONE_INT interrupt.
    (R/SS/WTC)

ECDSA_SHA_RELEASE_INT_RAW  The raw interrupt status of the ECDSA_SHA_RELEASE_INT interrupt.
    (R/SS/WTC)
```