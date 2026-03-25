

```markdown
| Enable Field                     | Valid Task Received                  | Response Operation                                                                 |
|----------------------------------|---------------------------------------|-------------------------------------------------------------------------------------|
| MCPWM_TASK_CMPRx_A_UP_EN         | MCPWM_TASK_CMPRx_A_UP                 | Timer stamp A of the PWM operator x is updated to the value of the shadow register MCPWM_GENx_A |
```

## 36.3.6 Interrupts

*   `MCPWM_TIMERx_STOP_INT`: triggered when timerx stops. Only could be triggered when the `MCPWM_TIMERx_STOP_INT_ENA` field in the `MCPMW_INT_ENA_REG` register is set.
*   `MCPWM_TIMERx_TEZ_INT`: triggered by the TEZ event of PWM timerx. Only could be triggered when the `MCPWM_TIMERx_TEZ_INT_ENA` field in the `MCPMW_INT_ENA_REG` register is set.
*   `MCPWM_TIMERx_TEP_INT`: triggered by the TEP event of PWM timerx. Only could be triggered when the `MCPWM_TIMERx_TEP_INT_ENA` field in the `MCPMW_INT_ENA_REG` register is set.
*   `MCPWM_FAULTx_INT`: triggered when fault_eventx starts. Only could be triggered when the `MCPWM_FAULTx_INT_ENA` field in the `MCPMW_INT_ENA_REG` register is set.
*   `MCPWM_FAULTx_CLR_INT`: triggered after fault_eventx ends. Only could be triggered when the `MCPWM_FAULTx_CLR_INT_ENA` field in the `MCPMW_INT_ENA_REG` register is set.
*   `MCPWM_CMPRx_TEA_INT`: triggered by the TEA event of PWM operatorx. Only could be triggered when the `MCPWM_CMPRx_TEA_INT_ENA` field in the `MCPMW_INT_ENA_REG` register is set.
*   `MCPWM_CMPRx_TEB_INT`: triggered by the TEB event of PWM operatorx. Only could be triggered when the `MCPWM_CMPRx_TEB_INT_ENA` field in the `MCPMW_INT_ENA_REG` register is set.
*   `MCPWM_TZx_CBC_INT`: triggered by the CBC action of PWMx. Only could be triggered when the `MCPWM_TZx_CBC_INT_ENA` field in the `MCPMW_INT_ENA_REG` register is set.
*   `MCPWM_TZx_OST_INT`: triggered by the OST action of PWMx. Only could be triggered when the `MCPWM_TZx_OST_INT_ENA` field in the `MCPMW_INT_ENA_REG` register is set.
*   `MCPWM_CAPx_INT`: triggered by the capture event on channelx. Only could be triggered when the `MCPWM_CAPx_INT_ENA` field in the `MCPMW_INT_ENA_REG` register is set.
```