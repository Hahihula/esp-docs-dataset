

```markdown
Register 11.94. PAU_REGDMA_CLK_CONF_REG (0x0004)

PAU_CLK_EN Configures whether or not to enable clock for the PAU module.
O: Disable
1: Enable
(R/W)
```

```markdown
Register 11.95. PAU_REGDMA_ETM_CTRL_REG (0x0008)

PAU_ETM_BUSY_CAUSE Records the ETM busy cause for debug purpose. (RO)
PAU_ETM_LINK_SEL_0 Configures to select a link for ETM operation 0. (R/W)
PAU_ETM_LINK_SEL_1 Configures to select a link for ETM operation 1. (R/W)
PAU_ETM_LINK_SEL_2 Configures to select a link for ETM operation 2. (R/W)
PAU_ETM_LINK_SEL_3 Configures to select a link for ETM operation 3. (R/W)
PAU_ETM_START_0 Write 1 to start ETM operation 0. (WT)
PAU_ETM_START_1 Write 1 to start ETM operation 1. (WT)
PAU_ETM_START_2 Write 1 to start ETM operation 2. (WT)
PAU_ETM_START_3 Write 1 to start ETM operation 3. (WT)
```