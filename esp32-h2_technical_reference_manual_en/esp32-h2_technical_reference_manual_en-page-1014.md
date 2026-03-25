

```markdown
## 34.6 Registers

'|' here means a separate line. The left describes the access in Operation mode. The right belongs to Reset mode with red color. The addresses in this section are relative to Two-wire Automotive Interface base address (each TWAI 0 and TWAI 1 has an individual base address) provided in Table 4.3-2 in Chapter 4 System and Memory.

Register 34.1. TWAI_MODE_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| 3   | TWAI_RX_FILTER_MODE |
| 2   | TWAI_SELF_TEST_MODE |
| 1   | TWAI_LISTEN_ONLY_MODE |
| 0   | TWAI_RESET_MODE |

TWAI_RESET_MODE Configures the Operation mode of the TWAI Controller.
- O: Operation mode
- 1: Reset mode
(R/W)

TWAI_LISTEN_ONLY_MODE Configures whether to enter the Listen-Only mode.
- O: No effect
- 1: Listen-Only mode. In this mode, the nodes will only receive messages from the bus, without generating the acknowledge signal or updating the RX error counter.
(R/W)

TWAI_SELF_TEST_MODE Configures whether to enter the Self-Test mode.
- O: No effect
- 1: Enter the Self-Test mode. In this mode, the TX nodes can perform a successful transmission without receiving the acknowledge signal. This mode is often used to test a single node with the self-reception request command.
(R/W)

TWAI_RX_FILTER_MODE Configures the filter mode.
- O: Dual Filter mode
- 1: Single Filter mode
(R/W)
```