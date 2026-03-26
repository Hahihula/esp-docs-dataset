

```markdown
Register 20.53. HP_SYSTEM_HP_ECC_PD_CTRL_REG (0x01D4)
```

| Bit | Description |
|-----|-------------|
| 3   | HP_SYSTEM_ECC_MEM_PD<br>Configures whether or not to power down ECC internal memory.<br>O: No effect<br>1: Power down<br>(R/W) |
| 2   | HP_SYSTEM_ECC_MEM_FORCE_PU<br>Configures whether or not to force power up ECC internal memory.<br>O: No effect<br>1: Power up<br>(R/W) |
| 1   | HP_SYSTEM_ECC_MEM_FORCE_PD<br>Configures whether or not to force power down ECC internal memory. This setting has a lower priority than HP_SYSTEM_ECC_MEM_FORCE_PU.<br>O: No effect<br>1: Power down<br>(R/W) |
| 0   | Reset |

```markdown
HP_SYSTEM_ECC_MEM_FORCE_PD Configures whether or not to force power down ECC internal memory. This setting has a lower priority than HP_SYSTEM_ECC_MEM_FORCE_PU.
```

```markdown
O: No effect
1: Power down
(R/W)
```

```markdown
HP_SYSTEM_ECC_MEM_FORCE_PU Configures whether or not to force power up ECC internal memory.
```

```markdown
O: No effect
1: Power up
(R/W)
```

```markdown
HP_SYSTEM_ECC_MEM_PD Configures whether or not to power down ECC internal memory.
```

```markdown
O: No effect
1: Power down
(R/W)
```
```