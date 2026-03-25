

```markdown
# Chapter 11

## Low-Power Management

### 11.1 Overview

ESP32-H2 features an advanced low-power management system that can optimize the chip's power consumption while maintaining its high performance.

The low-power management system employs various power-saving techniques such as sleep modes, dynamic voltage and frequency scaling, and peripheral power gating to minimize the chip's power consumption.

The power management unit (PMU) is a hardware component that is the core part of the low-power management system and is responsible for powering up and down different power domains of the chip, to achieve the best balance among chip performance, power consumption, and wake-up latency.

### 11.2 Terminology

The following terms related to low-power management are defined in the context of the ESP32-H2 Technical Reference Manual to help readers better understand this document:

| Term                        | Definition                                                                 |
|-----------------------------|-----------------------------------------------------------------------------|
| Low-power management        | Refers to the whole system that manages the chip's power consumption.      |
| Power management unit (PMU) | Refers to the specific hardware module that controls power up and down for the power domains, clocks, and power-related logic. |
| Power domain                | Refers to the smallest unit that can be independently powered up or down. A power domain can contain one or multiple modules within the chip. |
| PMU states                  | Refers to three states of the PMU's state machine. Users can configure the clock gating and power gating of a power domain in each of these states. |
| Power modes                 | Refers to the five preset power modes that power up different domains for typical application scenarios. |

### 11.3 Features

The PMU has the following features:

- Three configurable PMU states. Software can flexibly configure them according to the needs.
    - HP_ACTIVE
    - HP_SLEEP
```