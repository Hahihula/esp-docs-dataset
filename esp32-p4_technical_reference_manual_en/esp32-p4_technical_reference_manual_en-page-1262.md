

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.13. HP_SYSTEM_HP_CORE_TIMEOUT_INT_ENA_REG (0x01BO)
```

```plaintext
31          6   5   4   3   2   1   0
-------------------------------------------------
0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 | Reset
```

```markdown
HP_SYSTEM_CORE0_AHB_TIMEOUT_INT_ENA Write 1 to enable HP_CORE0_AHB_TIMEOUT_INT interrupt. (R/W)

HP_SYSTEM_CORE1_AHB_TIMEOUT_INT_ENA Write 1 to enable HP_CORE1_AHB_TIMEOUT_INT interrupt. (R/W)

HP_SYSTEM_CORE0_IBUS_TIMEOUT_INT_ENA Write 1 to enable HP_CORE0_IBUS_TIMEOUT_INT interrupt. (R/W)

HP_SYSTEM_CORE1_IBUS_TIMEOUT_INT_ENA Write 1 to enable HP_CORE1_IBUS_TIMEOUT_INT interrupt. (R/W)

HP_SYSTEM_CORE0_DBUS_TIMEOUT_INT_ENA Write 1 to enable HP_CORE0_DBUS_TIMEOUT_INT interrupt. (R/W)

HP_SYSTEM_CORE1_DBUS_TIMEOUT_INT_ENA Write 1 to enable HP_CORE1_DBUS_TIMEOUT_INT interrupt. (R/W)
```