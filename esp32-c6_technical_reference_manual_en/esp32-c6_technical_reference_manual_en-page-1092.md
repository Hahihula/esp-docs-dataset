

```markdown
| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| 4   | TWAI_RESET_MODE Configures the Operation mode of the TWAI Controller. <br> O: Operation mode <br> 1: Reset mode <br> (R/W) |
| 3   | TWAI_LISTEN_ONLY_MODE Configures whether to enter the Listen-only mode. <br> O: No effect <br> 1: Listen-only mode. In this mode, the nodes will only receive messages from the bus, without generating the acknowledge signal or updating the RX error counter. <br> (R/W) |
| 2   | TWAI_SELF_TEST_MODE Configures whether to enter the Self-test mode. <br> O: No effect <br> 1: Enter the Self-test mode. In this mode, the TX nodes can perform a successful transmission without receiving the acknowledge signal. This mode is often used to test a single node with the self-reception request command. <br> (R/W) |
| 1   | TWAI_RX_FILTER_MODE Configures the filter mode. <br> O: Dual-filter mode <br> 1: Single-filter mode <br> (R/W) |
| 0   | Reset |
```