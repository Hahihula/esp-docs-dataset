

```markdown
| Value of n | Source |
|------------|--------|
| 0          | HP CPU |
| 1          | Reserved |
| 2          | Reserved |
| 3          | Reserved |
| 4          | Reserved |
| 5          | TCM_MEM_MONITOR |
| 6          | TRACE |
| 7          | Reserved |
| 8          | PSRAM_MEM_MONITOR |
| 9 ~ 15     | Reserved |
| 16 ~ 31    | See the peripherals corresponding to the values 0 ~ 15 in Chapter 5 GDMA Controller (GDMA) > Table 5.4-1 GDMA Selecting Peripherals via Register Configuration. For example, 16 corresponds to the peripheral with value 0 in Table 5.4-1 GDMA Selecting Peripherals via Register Configuration, and 17 corresponds to the peripheral with value 1 in the table, and so on. |
```

You can configure `TEE_Mn_LOCK` and `LP_TEE_MO_LOCK` to lock the configuration of the master’s secure mode. Only chip reset, system reset, and core reset can unlock the configurations and restore all configurations in TEE registers to their default values.

## 18.5.2 APM Controller Functional Description

### 18.5.2.1 Architecture

Figure 18.5-1 shows the architecture of the APM controller and the access paths managed by it.
```