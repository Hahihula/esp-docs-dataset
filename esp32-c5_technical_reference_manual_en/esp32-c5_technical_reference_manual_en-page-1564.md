

```markdown
## 41.6 Registers

The addresses in this section are relative to Motor Control PWM base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 41.1. MCPWM_CLK_CFG_REG (0x0000)

```text
31                                 8                 7                  0
+------------------------------------------------------------------------------+
| xxxxxxxx | xxxxxxxx | xxxxxxxx | MCPWM_CLK_PRESCALE |
+------------------------------------------------------------------------------+
```

**MCPWM_CLK_PRESCALE** Configures the prescaler value of the clock, so that the period of  
PWM_clk = 6.25 ns * (PWM_CLK_PRESCALE + 1). (R/W)

### Register 41.2. MCPWM_TIMERn_CFGO_REG (n: 0-2) (0x0004+0x10*n)

```text
31                                 8                 7                  0
+------------------------------------------------------------------------------+
| xxxxxxxx | MCPWM_TIMERn_PERIOD_UPMETHOD | MCPWM_TIMERn_PERIOD | MCPWM_TIMERn_PRESCALE |
+------------------------------------------------------------------------------+
```

**MCPWM_TIMERn_PRESCALE** Configures the prescaler value of timer n, so that the period of  
PTO_clk = Period of PWM_clk * (PWM_TIMERn_PRESCALE + 1). (R/W)

**MCPWM_TIMERn_PERIOD** Configures the period shadow of PWM timer n.  
(R/W)

**MCPWM_TIMERn_PERIOD_UPMETHOD** Configures the update method for active register of PWM  
timer n period.  
0: Immediate  
1: TEZ  
2: Sync  
3: TEZ or sync  
TEZ here and below means timer equals zero event.  
(R/W)
```