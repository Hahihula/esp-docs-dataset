

```markdown
Register 19.2. HP_SYSTEM_SEC_DPA_CONF_REG (0x0008)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 3   | 2   | 1   | 0    |
|     |                                                   | Reset |
| 0   | 0   | 0   | ...  | 0x0  |

HP_SYSTEM_SEC_DPA_LEVEL Configures whether to enable anti-DPA attack. Valid only when HP_SYSTEM_SEC_DPA_CFG_SEL is O.
- O: Disable
- 1-3: Enable. The larger the number, the higher the security level, which represents the ability to resist DPA attacks, with increased computational overhead of the hardware crypto-accelerators at the same time.
(R/W)

HP_SYSTEM_SEC_DPA_CFG_SEL Configures whether to select HP_SYSTEM_SEC_DPA_LEVEL or EFUSE_SEC_DPA_LEVEL (from eFuse) to control DPA level.
- O: Select EFUSE_SEC_DPA_LEVEL
- 1: Select HP_SYSTEM_SEC_DPA_LEVEL
(R/W)
```