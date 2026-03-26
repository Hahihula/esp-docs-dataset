

```markdown
Chapter 8 eFuse Controller (EFUSE)
GoBack

There are several internal interrupt sources from eFuse controller that can generate the above interrupt signal.
The interrupt sources from eFuse controller are listed with their trigger conditions and the resulted interrupt
signal in Table 8.4-1.

Table 8.4-1. eFuse's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition                      | Interrupt Signal |
|----------------------------|-----------------------------------------|------------------|
| EFUSE_PGM_DONE_INT         | Programming of eFuse completes          |                  |
| EFUSE_READ_DONE_INT        | Reading of eFuse completes              | EFUSE_INT        |

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 8.5 Register Summary.
```