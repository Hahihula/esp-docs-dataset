

```markdown
| Internal Interrupt Source                     | Trigger Condition                                                                                      | Interrupt Signal |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------|------------------|
| TOUCH_APPROACH_LOOP_DONE_INT                 | Completion of proximity mode cumulative sampling                                                      |                  |
| TOUCH_TIMEOUT_INT                            | Timeout for the TOUCH_OUT signal sampling                                                              | LP_TOUCH_INTR   |
| TOUCH_INACTIVE_INT                           | Touch release detected                                                                                |                  |
| TOUCH_ACTIVE_INT                             | Touch detected                                                                                        |                  |
| TOUCH_DONE_INT                               | Completion of sampling an individual touch pin at a certain frequency mode for comparison             |                  |
| TOUCH_SCAN_DONE_INT                          | Completion of sampling selected touch pins for comparison at all frequency modes                    |                  |
| TOUCH_BENCHMARK_UPDATE_INT                   | Completion of software benchmark data update                                                          |                  |

**Note:**
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.
```

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 60.6 Register Summary.