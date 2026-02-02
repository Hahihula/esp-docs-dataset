Title: Peripheral Signal List

Subtitle: Table 6.9-1 shows the peripheral input/output signals via GPIO matrix.

Body Text:
Please pay attention to the configuration of the bit GPIO_FUNCn_OEN_SEL:

- GPIO_FUNCn_OEN_SEL = 1; the output enable is controlled by the corresponding bit n of GPIO_ENABLE_REG;
  - GPIO_ENABLE_REG = 0: output is disabled.
  - GPIO_ENABLE_REG = 1: output is enabled.

- GPIO_FUNCn_OEN_SEL = 0: use the output enable signal from peripheral, for example SPIQ_oe in the column “Output Enable of Output Signals” of Table 6.9-1. Note that the signals such as SPIQ_oe can be 1 (‘d1’) or 0 (‘d0’), depending on the configuration of corresponding peripherals. If it’s ‘d1’ in column “Output Enable of Output Signals”, it indicates that once GPIO_FUNCn_OEN_SEL is cleared, the output signal is always enabled by default.

Note:
Signals are numbered consecutively, but not all signals are valid.
- Only the signals with a name assigned in the column “Input signal” in Table 6.9-1 are valid input signals.
- Only the signals with a name assigned in the column “Output signal” in Table 6.9-1 are valid output signals.

Table Title: Table 6.9-1. GPIO_Matrix

Table:
| Signal | No. Input Signals | Same Input Signal from IO_MUX Core Value If Unassigned* | Output Signals |
|--------|------------------|----------------------------------------------------------|---------------|
|        |                  |                                                          |               |
| 0      | SPICLK_in        | O                                                        | SPICLK_out   |
| 1      | SPIQ_in          | O                                                        | SPIQ_out     |
| 2      | SPID_in          | O                                                        | SPID_out     |
| 3      | SPIHD_in         | O                                                        | SPIHD_out    |
| 4      | SPIWP_in         | O                                                        | SPIWP_out    |
| 5      | SPICS0_in        | O                                                        | SPICS0_out   |

*Unassigned indicates that the signal is not assigned to any specific input or output in this context.