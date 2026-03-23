

```markdown
Register 15.7. WCL_Core_0_World_PREPARE_REG (0x0144)

WCL_CORE_0_WORLD_PREPARE Configures the world to switch to.
- 0x1: reserved
- 0x2: Non-secure World
(R/W)
```

```markdown
Register 15.8. WCL_Core_0_World_UPDATE_REG (0x0148)

WCL_CORE_0_UPDATE Write any value to this field to indicate the completion of CPU configuration for switching from Secure World to Non-Secure World. (WO)
```

```markdown
Register 15.9. WCL_Core_0_World_Cancel_REG (0x014C)

WCL_CORE_0_WORLD_CANCEL Write any value to this filed to cancel the CPU configuration for switching from Secure World to Non-Secure World. (WO)
```