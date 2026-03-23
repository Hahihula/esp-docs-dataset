

```markdown
Register 17.2. HP_SYSTEM_SEC_DPA_CONF_REG (0x0008)

| Bit | Description |
|-----|-------------|
| 3   | HP_SYSTEM_SEC_DPA_CFG_SEL |
| 2   | HP_SYSTEM_SEC_DPA_LEVEL |
| 1-0 | reserved    |

HP_SYSTEM_SEC_DPA_LEVEL Configures whether or not to enable anti-DPA attack. Valid only when HP_SYSTEM_SEC_DPA_CFG_SEL is 0.
O: Disable
1-3: Enable. The larger the number, the higher the security level, which represents the ability to resist DPA attacks, with increased computational overhead of the hardware crypto-accelerators at the same time.
(R/W)

HP_SYSTEM_SEC_DPA_CFG_SEL Configures whether to select HP_SYSTEM_SEC_DPA_LEVEL or EFUSE_SEC_DPA_LEVEL (from eFuse) to control DPA level.
O: Select EFUSE_SEC_DPA_LEVEL
1: Select HP_SYSTEM_SEC_DPA_LEVEL
(R/W)

Register 17.3. HP_SYSTEM_CORE_DEBUG_RUNSTALL_CONF_REG (0x0040)

| Bit | Description |
|-----|-------------|
| 1   | HP_SYSTEM_CORE_DEBUG_RUNSTALL_ENABLE |
| 0-0 | reserved    |

HP_SYSTEM_CORE_DEBUG_RUNSTALL_ENABLE Configures whether or not to enable debug Run-Stall functionality between HP CPU and LP CPU.
O: Disable
1: Enable
(R/W)
```