**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Body Text:**

- VDD3P3_RTC: the input power supply for both RTC and CPU

- VDD3P3_CPU: the input power supply for CPU

- VDD_SPI: configurable input/output power supply

VDD_SPI can be configured to use an internal LDO. The LDO input and output both are 1.8 V. If the LDO is not enabled, VDD_SPI is connected directly to the same power supply as VDD3P3_RTC.

The VDD_SPI configuration is determined by the value of strapping pin GPIO45, or can be overridden by eFuse and/or register settings. See ESP32-S3 Datasheet sections Power Scheme and Strapping Pins for more details.

Note that GPIO33 ~ GPIO37 and GPIO47 ~ GPIO48 can be powered either by VDD_SPI or VDD3P3_CPU.

**Subtitle:**
6.11 Peripheral Signals via GPIO Matrix

**Table Description (Table 6.11-1):**

| GPIO_FUNCn_OEN_SEL = n | GPIO_FUNCn_OEN_SEL |
|--------------------------|--------------------|
| GPIO_ENABLE_REG         | Output enable signal from peripheral, for example SPIQ_oe in the column "Output enable signal when GPIO_FUNCn_OEN_SEL = 0" of Table 6.11-1. Note that the signals such as SPIQ_oe can be 1 (t'd1) or 0 (t'd0), depending on the configuration of corresponding peripherals. If it's t'd1 in the "Output enable signal when GPIO_FUNCn_OEN_SEL = 0", it indicates that once the register GPIO FUNCn OEN SEL is cleared, the output signal is always enabled by default. |

**Note:**
Signals are numbered consecutively, but not all signals are valid.
- Only the signals with a name assigned in the column "Input signal" in Table 6.11-1 are valid input signals.

- Only the signals with a name assigned in the column "Output signal" in Table 6.11-1 are valid output signals.

**Footer:**
Espressif Systems
482 ESP32-S3 TRM (Version 1.7)