

```markdown
| TWAI_RESET_MODE | Configures the Operation mode of the TWAI Controller. |
|-----------------|------------------------------------------------------|
| 0: Operation mode                                       |
| 1: Reset mode                                         |
| (R/W)                                                  |

| TWAI_LISTEN_ONLY_MODE | Configures whether to enter the Listen-only mode. |
|-----------------------|--------------------------------------------------|
| 0: No effect                                 |
| 1: Listen-only mode. In this mode, the nodes will only receive messages from the bus, without generating the acknowledge signal or updating the RX error counter. (R/W) |

| TWAI_SELF_TEST_MODE | Configures whether to enter the Self-test mode. |
|---------------------|-----------------------------------------------|
| 0: No effect                                 |
| 1: Enter the Self-test mode. In this mode, the TX nodes can perform a successful transmission without receiving the acknowledge signal. This mode is often used to test a single node with the self-reception request command. (R/W) |

| TWAI_ACCEPTANCE_FILTER_MODE | Configures the filter mode. |
|----------------------------|-----------------------------|
| 0: Dual-filter mode                                 |
| 1: Single-filter mode                               |
| (R/W)                                             |
```