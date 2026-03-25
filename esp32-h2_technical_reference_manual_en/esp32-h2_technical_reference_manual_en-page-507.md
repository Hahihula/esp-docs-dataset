

```markdown
## 15.4.2 APM Controller Functional Description

### 15.4.2.1 Architecture

Figure 15.4-1 shows the architecture of the APM controller and the access paths managed by it.

**Figure 15.4-1. APM Controller Architecture**

As shown in the figure, the APM controller contains two functional modules: HP_APM_CTRL and LP_APM_CTRL, configured by the register modules HP_APM_REG and LP_APM_REG, respectively.

*   HP_APM_CTRL manages four access paths, namely M0 – M3 in the figure. Permission management of each path can be enabled by configuring HP_APM_FUNC_CTRL_REG (enabled by default).
*   LP_APM_CTRL manages one access path, namely MO in the figure. Permission management of this path can be enabled by configuring LP_APM_FUNC_CTRL_REG (enabled by default).

Table 15.4-2 below shows the detailed information of the two functional modules:

**Table 15.4-2. Configuring Functional Modules**

| Functional Modules | Register Modules | Number of Access Paths | Enable Permission Management | Number of Configurable Address Ranges | Enable Address Ranges |
| :------------------ | :--------------- | :--------------------- | :---------------------------- | :------------------------------------ | :-------------------- |
| HP_APM_CTRL        | HP_APM_REG       | 4                     | HP_APM_FUNC_CTRL_REG         | 16                                     | HP_APM_REGION_FILTER_EN_REG |
| LP_APM_CTRL        | LP_APM_REG       | 1                     | LP_APM_FUNC_CTRL_REG         | 4                                      | LP_APM_REGION_FILTER_EN_REG |
```