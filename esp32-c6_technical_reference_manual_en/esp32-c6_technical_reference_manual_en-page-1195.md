

```markdown
- No synchronization input signal selected

• Configure the source of the PWM timer’s synchronization output to one of the four sources below:
    - Synchronization input signal
    - Event generated when the value of the PWM timer is equal to zero
    - Event generated when the value of the PWM timer is equal to the period
    - Event generated when writing toggle value to `MCPWM_TIMERx_SYNC_SW` bit

• Configure the method of period updating.

### 36.3.1.3 Operator Module

Figure 36.3-3. Operator Module

The configuration parameters of the operator module are shown in Table 36.3-1.

Table 36.3-1. Configuration Parameters of the Operator Submodule

| Submodule           | Configuration Parameter/Option for PWMxA and/or PWMxB output. |
|---------------------|----------------------------------------------------------------|
| PWM Generator       | • Configure at which time the timing events occur.<br>• Configure what action should be taken on timing events:<ul><li>Switch high or low of PWMxA and/or PWMxB outputs</li><li>Toggle PWMxA and/or PWMxB outputs</li><li>Take no action on outputs</li></ul><ul><li>Use direct s/w control to force the state of PWM outputs</li><li>Add a dead time to raising edge and/or failing edge on PWM outputs.</li><li>Configure update method for this submodule.</li></ul> |
```