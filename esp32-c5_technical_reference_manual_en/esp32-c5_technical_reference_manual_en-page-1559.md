

```markdown
| Enable Field                  | Generation Condition                                                                                      | Event Generated                     |
|-------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------|
| MCPWM_EVT_Fn_EN               | Fault event fault_eventn is generated                                                                     | MCPWMO_EVT_Fn                        |
| MCPWM_EVT_OPn_TEB_EN          | The count value of the timer that PWM operator n selects is equal to the value of timer stamp B¹           | MCPWMO_EVT_OPn_TEB                   |
| MCPWM_EVT_OPn_TEA_EN          | The count value of the timer that PWM operator n selects is equal to the value of timer stamp A¹           | MCPWMO_EVT_OPn_TEA                   |
| MCPWM_EVT_OPn_TEE1_EN         | The count value of the timer that PWM operator n selects is equal to the value of register MCPWM_OPn_TSTMP_E1_REG | MCPWMO_EVT_OPn_TEE1                  |
| MCPWM_EVT_OPn_TEE2_EN         | The count value of the timer that PWM operator n selects is equal to the value of register MCPWM_OPn_TSTMP_E2_REG | MCPWMO_EVT_OPn_TEE2                  |
| MCPWM_EVT_TIMERn_TEP_EN       | The count value of timer n is equal to the period value MCPWM_TIMERn_PERIOD                                 | MCPWMO_EVT_TIMERn_TEP                |
| MCPWM_EVT_TIMERn_TEZ_EN       | The count value of timer n is equal to 0                                                                    | MCPWMO_EVT_TIMERn_TEZ                |
| MCPWM_EVT_TIMERn_STOP_EN      | Timer n’s count stops                                                                                      | MCPWMO_EVT_TIMERn_STOP               |

¹ See Section 41.3.3.1 for a detailed description of timer stamp A and B.

## 41.3.5.3 MCPWM-Related ETM Tasks

When setting the enable field to 1, after inputting valid tasks, the corresponding response operation would be generated. For details, please refer to Table 41.3-8 below:

Table 41.3-8. ETM Related Tasks
| Enable Field                  | Valid Task Input                                      | Response Operation                                                                 |
|-------------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------------|
| MCPWM_TASK_CAPn_EN            | MCPWMO_TASK_CAPn                                       | CAPn channel performs a capture operation                                         |
| MCPWM_TASK_CLRn_OST_EN        | MCPWMO_TASK_CLRn_OST                                   | PWM operator n clears the One-Shot Trip operation                                 |
| MCPWM_TASK_TZn_OST_EN         | MCPWMO_TASK_TZn_OST                                    | PWM operator n performs a One-Shot Trip (OST) operation                           |
| MCPWM_TASK_TIMERn_PERIOD_UP_EN| MCPWMO_TASK_TIMERn_PERIOD_UP                          | The period of timer n is updated to the value configured in the period register MCPWM_TIMERn_PERIOD |
| MCPWM_TASK_TIMERn_SYNC_EN     | MCPWMO_TASK_TIMERn_SYN                                 | Timer n performs a sync operation                                                  |
| MCPWM_TASK_GEN_STOP_EN        | MCPWMO_TASK_GEN_STOP                                   | All the timers stop counting and the PWM signals output by all PWM operators remain unchanged |
```