

```markdown
Register 1.20. ucause (0x042)

Interrupt ID This field is automatically updated with the unique ID of the most recent user mode interrupt due to which CPU entered trap. (R/W)

Interrupt Flag This flag would always be set because CPU can only enter trap due to user mode interrupts as exception delegation is unsupported. (R/W)
```

```markdown
Register 1.21. uip (0x044)

USIP Configures the pending status of the user software interrupt.
O: Not pending
1: Pending
(R/W)

UTIP Configures the pending status of the user timer interrupt.
O: Not pending
1: Pending
(R/W)

UXIP Configures the pending status of the 28 external interrupts delegated to user mode.
O: Not pending
1: Pending
(R/W)
```