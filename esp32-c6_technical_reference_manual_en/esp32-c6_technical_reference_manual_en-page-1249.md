

```markdown
Register 36.23. MCPWM_DTO_CFG_REG (0x0058)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 31  | Reset                               |                                                                             |
| 18  | MCPWM_DTO_CLK_SEL                   | Configures dead time generator 0 clock selection.                           |
|     |                                    | O: PWM_CLK                                                                   |
|     |                                    | 1: PT_CLK                                                                    |
| (R/W)|                                      |                                                                             |
| 17  | MCPWM_DTO_A_OUTBYPASS               | S1 in table 36.3-5. (R/W)                                                   |
| 16  | MCPWM_DTO_B_OUTBYPASS               | SO in table 36.3-5. (R/W)                                                   |
| 15  | MCPWM_DTO_A_OUTSWAP                 | S6 in table 36.3-5. (R/W)                                                   |
| 14  | MCPWM_DTO_B_OUTSWAP                 | S7 in table 36.3-5. (R/W)                                                   |
| 13  | MCPWM_DTO_RED_INSEL                 | S4 in table 36.3-5. (R/W)                                                   |
| 12  | MCPWM_DTO_FED_INSEL                 | S5 in table 36.3-5. (R/W)                                                   |
| 11  | MCPWM_DTO_RED_OUTINVERT             | S2 in table 36.3-5. (R/W)                                                   |
| 10  | MCPWM_DTO_FED_OUTINVERT             | S3 in table 36.3-5. (R/W)                                                   |
| 9   | MCPWM_DTO_DEB_MODE                  | S8 in table 36.3-5, dual-edge B mode.                                     |
|     |                                    | O: FED/RED take effect on different path separately                         |
|     |                                    | 1: FED/RED take effect on B path, A out is in bypass or dulpB mode (R/W)    |
| 8   | MCPWM_DTO_RED_UPMETHOD              | Update method for RED active register. See details in MCPWM_DTO_FED_UPMETHOD. (R/W) |
| 7   | MCPWM_DTO_FED_UPMETHOD              | Configures update method for FED active register.                           |
|     |                                    | O: Immediate                                                                 |
|     |                                    | When bit0 is set to 1: TEZ                                                  |
|     |                                    | When bit1 is set to 1: TEP                                                  |
|     |                                    | When bit2 is set to 1: sync                                                  |
|     |                                    | When bit3 is set to 1: disable the update (R/W)                             |
```