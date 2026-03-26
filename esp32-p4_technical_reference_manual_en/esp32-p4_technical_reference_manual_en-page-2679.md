

```markdown
Register 52.58. EMACTGTIMENS_REG (0x0720)

TTSLO Configures the signed target time.
Measurement unit: nanosecond.
When the system time matches or exceeds the target time, an interrupt is generated (if enabled).
(R/W)
```

```markdown
Register 52.59. EMACSYSTIMHIGHWORD2ND_REG (0x0724)

TSHWR Configures the most significant 16-bits of the timestamp seconds value.
The register is directly written to initialize the value.
This register is incremented when there is an overflow from the 32 bits of the System Time
Seconds register. (R/W/SU)
```