

```markdown
Register 1.24. tdata2 (0x7A2)

tdata2 Abstract tdata2 content. (R/W)
This will always be interpreted as maddress since only match type (0x2) triggers are supported.

Register 1.25. tcontrol (0x7A5)

mpte Machine mode previous trigger enable bit. (R/W)
- When CPU is taking a machine mode trap, the value of mte is automatically pushed into this.
- When CPU is executing MRET, its value is popped back into mte, so this becomes 0.

mte Machine mode trigger enable bit. (R/W)
- When CPU is taking a machine mode trap, its value is automatically pushed into mpte, so this becomes 0 and triggers with action=0 are disabled globally.
- When CPU is executing MRET, the value of mpte is automatically popped back into this.
```