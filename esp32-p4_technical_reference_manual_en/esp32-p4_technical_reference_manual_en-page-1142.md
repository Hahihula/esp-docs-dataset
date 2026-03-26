

```markdown
Figure 19.3-1. APM Architecture

Legend:
- Blue circle: access permission managed by HP_PERI_PMS_REG
- White circle (outline): access permission managed by LP2HP_PERI_PMS_REG
- Pink/magenta dot: access permission managed by HP_DMA_PMS_REG
- Orange circle: access permission managed by HP2LP_PERI_PMS_REG

Note:
- For register group names “HP2LP” and “LP2HP”, the “HP” refers to HP CPU0/1, and “LP” refers to LP CPU.
- From Table 19.1-1, it can be seen that HP CPU and LP CPU access different address spaces of HP ROM, HP L2MEM, external flash, and external RAM. For HP CPU0/1, HP APM manages their direct access to internal and external memory without going through the cache.
- LP_PERI_PMS_REG includes eight additional configurable address ranges for HP APM and LP APM to manage the access permissions to peripheral registers, including HP CPU PERI, HP PERI, and LP PERI.

19.3.2 Address Ranges and Permissions Management

APM manages address ranges, which can be fixed or configurable. DMA APM can manage up to 32 configurable address ranges. In addition to the fixed address ranges, HP APM and LP APM can also manage in total eight configurable address ranges.

19.3.2.1 Address Ranges Managed by HP APM and LP APM

In the access paths controlled by HP APM and LP APM, the internal memory and external memory use fixed address ranges for access control, while peripheral registers not only support fixed address ranges permission control but also support eight configurable address ranges.
```