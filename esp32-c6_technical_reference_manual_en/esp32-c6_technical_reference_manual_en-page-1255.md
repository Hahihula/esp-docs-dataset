

```markdown
| (reserved) | MCPWM_GEN1_B_SHDW_FULL | MCPWM_GEN1_A_SHDW_FULL | MCPWM_GEN1_B_UPMETHOD | MCPWM_GEN1_A_UPMETHOD |
|:------------|:-----------------------|:------------------------|:----------------------|:----------------------|
| 31          | 10                     | 9                      | 8                     | 7                     |
|             |                        |                       | 4                     | 3                     |
|             |                        |                       |                      | 0                     |
|             |                        |                       |                      | Reset                 |

MCPWM_GEN1_A_UPMETHOD Configures update method for PWM generator 1 time stamp A's active register.
When all bits are set to 0: immediately. When bit0 is set to 1: TEZ.
When bit1 is set to 1: TEP
When bit2 is set to 1: sync
When bit3 is set to 1: disable the update (R/W)

MCPWM_GEN1_B_UPMETHOD Configures update method for PWM generator 1 time stamp B's active register. See details in MCPWM_GEN1_A_UPMETHOD. (R/W)

MCPWM_GEN1_A_SHDW_FULL Set and reset by hardware.
0: A's active reg has been updated with shadow register latest value.
1: PWM generator 1 time stamp A's shadow reg is filled and waiting to be transferred to A's active reg.
(R/SC/WTC)

MCPWM_GEN1_B_SHDW_FULL Set and reset by hardware.
0: B's active reg has been updated with shadow register latest value.
1: PWM generator 1 time stamp B's shadow reg is filled and waiting to be transferred to B's active reg.
(R/SC/WTC)
```

```markdown
| (reserved) | MCPWM_GEN1_A |
|:------------|:--------------|
| 31          | 16            |
|             | 15            |
|             |              |
|             | Reset         |

MCPWM_GEN1_A Shadow register for PWM generator 1 time stamp A. (R/W)
```