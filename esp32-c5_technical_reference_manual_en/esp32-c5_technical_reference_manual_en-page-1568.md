

```markdown
Register 41.7. MCPWM_OPERATOR_TIMERSSEL_REG (0x0038)

31 ────────────────────────────────────────────────────────────────────────────── Reset
      6   5   4   3   2   1   0
      +---+---+---+---+---+---+
      |reserved| MCPWM_OPERATOR2_TIMERSSEL |
      |       | MCPWM_OPERATOR1_TIMERSSEL |
      |       | MCPWM_OPERATOR0_TIMERSSEL |
      +---+---+---+---+---+---+

MCPWM_OPERATORn_TIMERSSEL Configures which PWM timer will be the timing reference for PWM operatorn.
O: timer0
1: timer1
2: timer2
3: Invalid, will select timer2
(R/W)
```