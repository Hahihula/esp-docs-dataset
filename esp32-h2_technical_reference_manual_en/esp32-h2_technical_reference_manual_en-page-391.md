

```markdown\n- LP_SWITCH: The intermediate state for the LP system transitioning between HP_SLEEP and LP_SLEEP. The hardware will complete the control switching of various controllers in this state.\n```
![Figure 11.4-2. PMU Workflow](image_path)  // Note: Actual image not included here, but described as a block diagram showing states and transitions.\n\nThe following sections describe the main parts of PMU.\n\n### 11.4.2.1 PMU Main State Machine\nThe PMU main state machine can receive sleep and wake-up signals, change the state of power and clock through the power controllers, thereby switching PMU states, and achieving a balance between performance and power consumption of the chip.
```