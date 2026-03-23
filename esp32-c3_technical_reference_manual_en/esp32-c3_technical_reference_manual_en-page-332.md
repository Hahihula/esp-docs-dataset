

```markdown
| Accessed Address | Access Alignment | Read | Write |
|:-----------------|:------------------|:------|:-------|
||Word aligned|√|INTR|
||Byte aligned|√|INTR|
|0x2|Half-word aligned|√|INTR|
||Word aligned|√|INTR|
||Byte aligned|√|INTR|
|0x3|Half-word aligned|√|INTR|
||Word aligned|√|INTR|

Table 14.7-7. Interrupt Registers for Unauthorized Access Alignment

<table><thead><tr><th>Registers</th><th>Bit</th><th>Description</th></tr></thead><tbody><tr><td rowspan="2">PMS_CORE_0_PIF_PMS_MONITOR_4_REG</td><td>[1]</td><td>Enables interrupt</td></tr><tr><td>[0]</td><td>Cleared interrupt signal and logged information</td></tr><tr><td>PMS_CORE_0_PIF_PMS_MONITOR_5_REG</td><td>[4:3]<br/>[2:1]<br/>[0]</td><td>Stores the privileged mode the CPU was in when the unauthorized access happened. Ob01: privileged environment; Ob10: unprivileged environment<br/>Stores the unauthorized access type. 0: byte aligned; 1: half-word aligned; 2: word aligned<br/>Stores the interrupt status. 0: no interrupt; 1: interrupt</td></tr><tr><td>PMS_CORE_0_PIF_PMS_MONITOR_6_REG</td><td>[31:0]</td><td>Stores the address of the unauthorized access</td></tr></tbody></table>

## 14.8 Register Locks

All ESP32-C3's permission control related registers can be locked by respective lock registers. When the lock registers are configured to 1, these registers themselves and their related permission control registers are all protected from modification until the next CPU reset.

Note that there isn't a one-to-one correspondence between the lock registers and permission control registers. See details in Table 14.8-1.

Table 14.8-1. Lock Registers and Related Permission Control Registers

<table><thead><tr><th>Lock Registers</th><th>Related Permission Control Registers</th></tr></thead><tbody><tr><td colspan="2"><strong>Lock privileged Mode Configuration</strong></td></tr><tr><td rowspan="2">PMS_PRIVILEGE_MODE_SEL_LOCK_REG</td><td>PMS_PRIVILEGE_MODE_SEL_LOCK_REG</td></tr><tr><td>PMS_PRIVILEGE_MODE_SEL_REG</td></tr><tr><td colspan="2"><strong>Lock Internal SRAM Usuage and Access Configuration</strong></td></tr><tr><td rowspan="3">PMS_INTERNAL_SRAM_USAGE_O_REG</td><td>PMS_INTERNAL_SRAM_USAGE_O_REG</td></tr><tr><td>PMS_INTERNAL_SRAM_USAGE_1_REG</td></tr><tr><td>PMS_INTERNAL_SRAM_USAGE_4_REG</td></tr><tr><td rowspan="3">PMS_CORE_X_IRAMO_PMS_CONSTRAIN_O_REG</td><td>PMS_CORE_X_IRAMO_PMS_CONSTRAIN_O_REG</td></tr><tr><td>PMS_CORE_X_IRAMO_PMS_CONSTRAIN_1_REG</td></tr><tr><td>PMS_CORE_X_IRAMO_PMS_CONSTRAIN_2_REG</td></tr><tr><td>PMS_CORE_m_IRAMO_PMS_MONITOR_O_REG</td><td>PMS_CORE_m_IRAMO_PMS_MONITOR_O_REG</td></tr></tbody></table>
```