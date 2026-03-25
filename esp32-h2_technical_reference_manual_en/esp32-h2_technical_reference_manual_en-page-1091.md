

```markdown
| Enable Field                     | Generation Condition                                                                                      | Event Generated                  |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------|
| MCPWM_EVT_Fx_EN                  | Fault event fault_eventx is generated                                                                     | MCPWM_EVT_Fx                     |
| MCPWM_EVT_OPx_TEB_EN             | The count value of the timer that PWM operator x selects is equal to the value of timer stamp B¹         | MCPWM_EVT_OPx_TEB                 |
| MCPWM_EVT_OPx_TEA_EN             | The count value of the timer that PWM operator x selects is equal to the value of timer stamp A¹        | MCPWM_EVT_OPx_TEA                 |
| MCPWM_EVT_TIMERx_TEP_EN          | The count value of timer x is equal to the period value MCPWM_TIMERx_PERIOD                              | MCPWM_EVT_TIMERx_TEP              |
| MCPWM_EVT_TIMERx_TEZ_EN          | The count value of timer x is equal to 0                                                                  | MCPWM_EVT_TIMERx_TEZ              |
| MCPWM_EVT_TIMERx_STOP_EN         | Timer x stops counting                                                                                   | MCPWM_EVT_OPx_TEA                 |

¹ See Section 36.3.3.1 for a detailed description of timer stamp A and B.

### 36.3.5.3   MCPWM-Related ETM Tasks

When setting the enable field to 1, after inputting valid tasks, the corresponding response operation would be generated. For details, please refer to Table 36.3-8 below:

Table 36.3-8. MCPWM-Related ETM Tasks

| Enable Field                     | Valid Task Received                          | Response Operation                                                                 |
|----------------------------------|----------------------------------------------|-------------------------------------------------------------------------------------|
| MCPWM_TASK_CAPx_EN               | MCPWM_TASK_CAPx                              | CAPx channel performs a capture operation                                         |
| MCPWM_TASK_CLRx_OST_EN           | MCPWM_TASK_CLRx_OST                          | PWM operator x clears the One-Shot Trip operation                                  |
| MCPWM_TASK_TZx_OST_EN            | MCPWM_TASK_TZx_OST                           | PWM operator x performs a One-Shot Trip (OST) operation                            |
| MCPWM_TASK_TIMERx_PERIOD_UP_EN   | MCPWM_TASK_TIMERx_PERIOD_UP                  | The period of timer x is updated to the value configured in the period register    |
|                                      |                                              | MCPWM_TIMERx_PERIOD               |
| MCPWM_TASK_TIMERx_SYNC_EN        | MCPWM_TASK_TIMERx_SYNC                       | Timer x performs a sync operation                                                  |
| MCPWM_TASK_GEN_STOP_EN           | MCPWM_TASK_GEN_STOP                          | All the timers stop counting and the PWM signals output by all PWM operators remain unchanged |
| MCPWM_TASK_CMPRx_B_UP_EN         | MCPWM_TASK_CMPRx_B_UP                        | Timer stamp B of the PWM operator x is updated to the value of the shadow register |
|                                      |                                              | MCPWM_GENx_B                       |
```