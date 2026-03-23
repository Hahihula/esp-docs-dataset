

```markdown
## Figure 16.3-1. APM Controller Structure

### Note:
For the difference between Low speed mode and High speed mode in the figure, please refer to System and Memory.

As shown in the Figure 16.3-1, APM controller contains 3 functional modules: HP_APM_CTRL, LP_APM0_CTRL and LP_APM_CTRL, configured by the register modules HP_APM_REG, LP_APM0_REG and LP_APM_REG respectively.

*   HP_APM_CTRL manages 4 access paths, namely MO-M3 in the figure 16.3-1. Permission management of each path can be enabled by configuring HP_APM_FUNC_CTRL_REG (enabled by default).
*   LP_APM0_CTRL manages one access path, namely MO in the figure 16.3-1. Permission management of this path can be enabled by configuring LP_APM0_FUNC_CTRL_REG (enabled by default).
*   LP_APM_CTRL manages 2 access paths, namely MO and M1 in the figure 16.3-1. Permission management of each path can be enabled by configuring LP_APM_FUNC_CTRL_REG (enabled by default).

The table 16.3-1 below shows the detailed information of each functional module:

### Table 16.3-1. Configuring Access Path

| Register Modules | Functional Modules | Access Path No. | Enable Permission Management | Configurable Address Ranges No. | Enable Address Ranges |
|------------------|--------------------|-----------------|------------------------------|--------------------------------|------------------------|
| HP_APM_REG       | HP_APM_CTRL        | 4               | HP_APM_FUNC_CTRL_REG         | 16                             | HP_APM_REGION_FILTER_EN_REG |
```