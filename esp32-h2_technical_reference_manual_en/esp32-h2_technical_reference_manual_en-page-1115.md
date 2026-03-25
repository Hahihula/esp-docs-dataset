

```markdown
|Bit Name                                 |Mask         |Access|Default|
|-----------------------------------------|-------------|-------|--------|
|MCPWM_DTO_CLK_SEL                       |0x8000       |R/W    |0       |
|MCPWM_DTO_A_OUTBYPASS                   |0x4000       |R/W    |0       |
|MCPWM_DTO_B_OUTBYPASS                   |0x2000       |R/W    |0       |
|MCPWM_DTO_FED_OUTINVERT                 |0x1000       |R/W    |0       |
|MCPWM_DTO_RED_OUTINVERT                 |0x800        |R/W    |0       |
|MCPWM_DTO_FED_RED_INSEL                 |0x400        |R/W    |0       |
|MCPWM_DTO_RED_INSEL                     |0x200        |R/W    |0       |
|MCPWM_DTO_A_OUTSWAP                     |0x100        |R/W    |0       |
|MCPWM_DTO_B_OUTSWAP                     |0x80         |R/W    |0       |
|MCPWM_DTO_DEB_MODE                      |0x40         |R/W    |0       |
|MCPWM_DTO_RED_UPMETHOD                  |0x20         |R/W    |0       |
|MCPWM_DTO_FED_UPMETHOD                  |0x10         |R/W    |0       |
|(reserved)                              |             |       |        |
|31                                       |18            |17     |16      |
||15            |14     |13      |
||12            |11     |10      |
||9             |8      |7       |
||6             |5      |4       |
||3             |2      |1       |
|Reset                                    ||||||||
```

MCPWM_DTO_FED_UPMETHOD Configures update method for FED active register.

O: Immediate

When bit0 is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: sync
When bit3 is set to 1: disable the update (R/W)

MCPWM_DTO_RED_UPMETHOD Update method for RED active register. See details in MCPWM_DTO_FED_UPMETHOD. (R/W)

MCPWM_DTO_DEB_MODE Configures the S8 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DTO_A_OUTSWAP Configures the S6 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DTO_B_OUTSWAP Configures the S7 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DTO_RED_INSEL Configures the S4 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DTO_FED_INSEL Configures the S5 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DTO_RED_OUTINVERT Configures the S2 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DTO_FED_OUTINVERT Configures the S3 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DTO_A_OUTBYPASS Configures the S1 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DTO_B_OUTBYPASS Configures the SO switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DTO_CLK_SEL Configures dead time generator O clock selection.

O: PWM_CLK
1: PT_CLK
(R/W)
```