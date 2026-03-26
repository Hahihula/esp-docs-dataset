

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.18. HP_SYSTEM_L2_ROM_PWR_CTRL0_REG (0x0040)
```

![Register bitfield diagram for HP_SYSTEM_L2_ROM_CLK_FORCE_ON](diagram description: A horizontal bitfield labeled from bit 31 to bit 0, with the rightmost bits showing "HP_SYSTEM_L2_ROM_CLK_FORCE_ON" and a single '1' at position indicating force on. The field is mostly marked as "(reserved)" except for this specific bit.)

```markdown
HP_SYSTEM_L2_ROM_CLK_FORCE_ON Configures whether or not to force on L2ROM clock.

O: No effect
1: Force on
(R/W)
```

Register 20.19. HP_SYSTEM_HP_SYSTEM_L2_MEM_RAM_PWR_CTRL0_REG (0x0060)

![Register bitfield diagram for HP_SYSTEM_L2_MEM_CLK_FORCE_ON](diagram description: A horizontal bitfield labeled from bit 31 to bit 0, with the rightmost bits showing "HP_SYSTEM_L2_MEM_CLK_FORCE_ON" and a single '1' at position indicating force on. The field is mostly marked as "(reserved)" except for this specific bit.)

```markdown
HP_SYSTEM_L2_MEM_CLK_FORCE_ON Configures whether or not to force on L2MEM clock.

O: No effect
1: Force on
(R/W)
```

Espressif Systems

Submit Documentation Feedback

ESP32-P4 TRM
PRELIMINARY
```