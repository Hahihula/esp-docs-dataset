

```markdown
| Bus^A | Environment   | Configuration Registers^B                                                                 | Access    |
|-------|---------------|---------------------------------------------------------------------------------------------|-----------|
| IBUS  | Privileged    | PMS_CORE_X_IRAMO_PMS_CONSTRAIN_SRAM_M_MODE_CACHEDATAARRAY_PMS_O^C                             | X/W/R     |
|       | Unprivileged  | PMS_CORE_X_IRAMO_PMS_CONSTRAIN_SRAM_U_MODE_CACHEDATAARRAY_PMS_O                              | X/W/R     |

^A To access the Internal SRAM0, CPU must be configured with both the usage permission and respective access permission.
^B 1: with access; 0: without access
^C For example, configuring this field to Ob101 indicates CPU's IBUS is granted with instruction execution and read accesses but not write access to SRAM0 in the privileged environment.

## 14.4.2.2 Internal SRAM1 Access Configuration

ESP32-C3’s Internal SRAM1 includes Block0 ~ Block2 (see details in Table 14.4-3) and can be:

* Accessed by CPU’s DBUS, IBUS and GDMA at the same time
* Further split into up to 6 regions with independent access management for more flexible permission control.

ESP32-C3’s Internal SRAM1 can be further split into up to 6 regions with 5 split lines. Users can configure different access to each region independently.

To be more specific, the Internal SRAM1 can be first split into Instruction Region and Data Region by IRam0_DRam0_split_line:

* **Instruction Region:**
    - Then the Instruction Region should be only configured to be accessed by IBUS;
    - And can be further split into three split regions by IRam0_split_line_0 and IRam0_split_line_1.
* **Data Region:**
    - The Data Region should be only configured to be accessed by DBUS;
    - And can be further split into three split regions by DRam0_split_line_0 and DRam0_split_line_1.

See illustration in Figure 14.4-1 and Table 14.4-5 below.
```

![Figure 14.4-1. Split Lines for Internal SRAM1](image-placeholder)

*Internal SRAM 1*

| instr_region_0 | Block0                                                                 |
|----------------|-------------------------------------------------------------------------|
|                | IBUS Permission: IRam0_PMS_0                                            |
|                | DBUS Permission: DRam0_PMS_0                                            |
|                | IRam0_split_line_1                                                     |

| instr_region_1 | Block0                                                                 |
|----------------|-------------------------------------------------------------------------|
|                | IBUS Permission: IRam0_PMS_1                                            |
|                | DBUS Permission: DRam0_PMS_1                                            |
|                | IRam0_split_line_0                                                     |

| instr_region_2 | Block1                                                                 |
|----------------|-------------------------------------------------------------------------|
|                | IBUS Permission: IRam0_PMS_2                                            |
|                | DBUS Permission: DRam0_PMS_2                                            |
|                | IRam0_DRam0_split_line                                                 |

| data_region_0  | Block2                                                                 |
|----------------|-------------------------------------------------------------------------|
|                | IBUS Permission: IRam0_PMS_3                                            |
|                | DBUS Permission: DRam0_PMS_3                                            |
|                | IRam0_split_line_0                                                     |

| data_region_1  | Block2                                                                 |
|----------------|-------------------------------------------------------------------------|
|                | IBUS Permission: IRam0_PMS_4 (implied by pattern)                       |
|                | DBUS Permission: DRam0_PMS_4                                            |
|                | IRam0_split_line_1                                                     |

| data_region_2  | Block2                                                                 |
|----------------|-------------------------------------------------------------------------|
|                | IBUS Permission: IRam0_PMS_5 (implied by pattern)                       |
|                | DBUS Permission: DRam0_PMS_5                                            |
|                | IRam0_split_line_1                                                     |

*Note: The above table is a textual representation of the diagram in Figure 14.4-1, as the actual image cannot be rendered here.*