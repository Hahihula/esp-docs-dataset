

```markdown
Register 15.4. WCL_Core_O_STATUSTABLEn_REG(n: 0-31) (0x0x0040+4*n)

WCL_CORE_O_FROM_WORLD_n Stores the world info before CPU entering entry n. (R/W)
WCL_CORE_O_FROM_ENTRY_n Stores the previous entry info before CPU entering entry n.(R/W)
WCL_CORE_O_CURRENT_n Represents if the interrupt is at entry n. (R/W)

Register 15.5. WCL_Core_O_STATUSTABLE_CURRENT_REG (0x00EO)

WCL_CORE_O_STATUSTABLE_CURRENT Represents the entry where the interrupt is currently at.
(R/W)

Register 15.6. WCL_Core_O_World_TRIGGER_ADDR_REG (0x0140)

WCL_CORE_O_WORLD_TRIGGER_ADDR Configures the entry address at which CPU switches from Secure World to Non-secure World. (RW)
```