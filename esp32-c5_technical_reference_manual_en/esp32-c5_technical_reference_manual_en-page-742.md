

```markdown
Chapter 18 Permission Control (PMS)

Figure 18.5-1. APM Controller Architecture

Note:
For more information about the "Low-speed mode" and "High-speed mode" in the figure, please refer to 6 System and Memory.

As shown in the figure, SYS_APM has four controllers:

*   HP_APM_CTRL, configured by the HP_APM_REG register module.
*   LP_APMO_CTRL, configured by the LP_APMO_REG register module.
*   LP_APM_CTRL, configured by the LP_APM_REG register module.
*   CPU_APM_CTRL, configured by the CPU_APM_REG register module.

PERI_APM has two controllers:

*   HP_PERI_APM_CTRL, configured by the TEE_REG register module.
*   LP_PERI_APM_CTRL, configured by the LP_TEE_REG register module.

The access paths and permission management configuration for each APM controller are as follows.

*   HP_APM_CTRL manages five access paths, namely M0 – M4 in the figure. Permission management of each path can be enabled by configuring HP_APM_FUNC_CTRL_REG (enabled by default).
*   LP_APMO_CTRL manages one access path, namely M0 in the figure. Permission management of this path can be enabled by configuring LP_APMO_FUNC_CTRL_REG (enabled by default).
*   LP_APM_CTRL manages two access paths, namely M0 – M1 in the figure. Permission management of this path can be enabled by configuring LP_APM_FUNC_CTRL_REG (enabled by default).
*   CPU_APM_CTRL manages four access paths, namely M0 – M3 highlighted in red in the figure. Permission management of this path can be enabled by configuring CPU_APM_FUNC_CTRL_REG (enabled by default).

Espressif Systems
742
ESP32-C5 TRM (Version 1.0)
Submit Documentation Feedback
```