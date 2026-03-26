

```markdown
Register 54.19. SDHOST_PLDMND_REG (0x0084)

SDHOST_PLDMND_PD   Configures the DMA FSM to resume normal descriptor fetch operation. If the OWNER bit of a descriptor is not set, the FSM goes to the Suspend state, software needs to write any value into this field for the FSM to resume normal descriptor fetch operation. (WO)


Register 54.20. SDHOST_DBADDR_REG (0x0088)

SDHOST_DBADDR_REG   Configures the base address of the linked list (First Descriptor). Bit[1:0] are ignored and taken as all-zero by the DMA internally. (R/W)
```