

```markdown
## 5.10.2 Power Supply Management

Each ESP32-C3 pin is connected to one of the two different power domains.

* VDD3P3_RTC: the input power supply for both RTC and CPU
* VDD3P3_CPU: the input power supply for CPU

## 5.11 Peripheral Signal List

Table 5.11-1 shows the peripheral input/output signals via GPIO matrix.

Please pay attention to the configuration of the bit `GPIO_FUNCn_OEN_SEL`:

* `GPIO_FUNCn_OEN_SEL = 1`: the output enable is controlled by the corresponding bit `n` of `GPIO_ENABLE_REG`:
    - `GPIO_ENABLE_REG = 0`: output is disabled;
    - `GPIO_ENABLE_REG = 1`: output is enabled;

* `GPIO_FUNCn_OEN_SEL = 0`: use the output enable signal from peripheral, for example SPIQ_oe in the column "Output enable signal when GPIO_FUNCn_OEN_SEL = 0" of Table 5.11-1. Note that the signals such as SPIQ_oe can be 1 ('1d1') or 0 ('1d0'), depending on the configuration of corresponding peripherals. If it's 1'd1 in the "Output enable signal when GPIO_FUNCn_OEN_SEL = 0", it indicates that once the register `GPIO_FUNCn_OEN_SEL` is cleared, the output signal is always enabled by default.

**Note:**
Signals are numbered consecutively, but not all signals are valid.
* Only the signals with a name assigned in the column "Input signal" in Table 5.11-1 are valid input signals.
* Only the signals with a name assigned in the column "Output signal" in Table 5.11-1 are valid output signals.
```