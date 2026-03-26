

```markdown
Register 20.52. HP_SYSTEM_HP_RSA_PD_CTRL_REG (0x01DO)
```

| Bit | Description |
|-----|-------------|
| 3   | HP_SYSTEM_RSA_MEM_PD<br>Configures whether or not to power down RSA internal memory.<br>O: No effect<br>1: Power down (R/W) |
| 2   | HP_SYSTEM_RSA_MEM_FORCE_PD<br>This setting has a lower priority than HP_SYSTEM_RSA_MEM_FORCE_PU.<br>O: No effect<br>1: Power down (R/W) |
| 1   | HP_SYSTEM_RSA_MEM_FORCE_PU<br>Configures whether or not to force power up RSA internal memory.<br>O: No effect<br>1: Power up (R/W) |
| 0   | HP_SYSTEM_RSA_MEM_PD<br>Configures whether or not to power down RSA internal memory.<br>O: No effect<br>1: Power down (R/W) |

```markdown
Espressif Systems
```

```markdown
Submit Documentation Feedback
```
```markdown
ESP32-P4 TRM
PRELIMINARY
```