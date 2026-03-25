

```markdown
Register 1.41. tdata2 (0x7A2)

tdata2 Configures the abstract tdata2 content. This will always be interpreted as maddress since only match type (0x2) triggers are supported. (R/W)


Register 1.42. tcontrol (0x7A5)

mpte Configures whether to enable the machine mode previous trigger.
When CPU is taking a machine mode trap, the value of mte is automatically pushed into this.
When CPU is executing MRET, its value is popped back into mte, so this becomes 0.
(R/W)

mte Configures whether to enable the machine mode trigger.
When CPU is taking a machine mode trap, its value is automatically pushed into mpte, so this becomes 0 and triggers with action=0 are disabled globally.
When CPU is executing MRET, the value of mpte is automatically popped back into this.
(R/W)
```