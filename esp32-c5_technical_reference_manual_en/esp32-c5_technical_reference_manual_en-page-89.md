

```markdown
Register 2.64. clicintip[i] (0x20801000 + 4*i)

IP[i] Represents the pending state for ith CLIC machine mode interrupt.
O: ith interrupt is not pending
1: ith interrupt is pending

- When the ith interrupt is configured as level type using clicintattr[i].TRIG, this bit is read-only,
and to clear it the interrupt must be cleared from source.

- When the ith interrupt is configured as edge triggered using clicintattr[i].TRIG, this bit is R/W,
and thus it is to be cleared by writing 0 to this register.
(R/W)

Register 2.65. clicintie[i] (0x20801001 + 4*i)

IE[i] Configures whether to enable the ith CLIC machine mode interrupt.
O: Disable
1: Enabled
(R/W)
```