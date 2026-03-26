

```markdown
## Register 14.67. PMU_EXT_WAKEUP_SEL_REG (0x01EC)

PMU_EXT_WAKEUP_SEL Configures whether to enable EXT wake-up.
- O: Disable
- 1: Enable
(R/W)
```

```markdown
## Register 14.68. PMU_EXT_WAKEUP_ST_REG (0x01F0)

PMU_EXT_WAKEUP_STATUS Gets the GPIO number for wake-up. 0 corresponds to GPIO0, 1 corresponds to GPIO1, and so on. (RO)
```

```markdown
## Register 14.69. PMU_EXT_WAKEUP_CNTL_REG (0x01F4)

| Bit | Description                  |
|-----|------------------------------|
| 31  | reserved                     |
| 30  | PMU_EXT_WAKEUP_STATUS_CLR    |
| 29  | PMU_EXT_WAKEUP_FILTER        |

PMU_EXT_WAKEUP_STATUS_CLR Clears the wake-up records. (R/W)

PMU_EXT_WAKEUP_FILTER Configures whether to enable the wake-up filter.
- O: Disable
- 1: Enable
(R/W)
```