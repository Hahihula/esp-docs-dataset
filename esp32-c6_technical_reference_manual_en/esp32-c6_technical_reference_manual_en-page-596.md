

```markdown
| Security-Level Name | Security-Level Value | PLL_CLK (MHz) | XTAL_CLK (MHz) |
|---------------------|----------------------|---------------|----------------|
| SEC_DPA_OFF         | 0                    | 160           | 40             |
| SEC_DPA_LOW         | 1                    | [120,160]     | [20,40]        |
| SEC_DPA_MIDDLE      | 2                    | [96,160]      | [33.3,40]      |
| SEC_DPA_HIGH        | 3                    | [80,160]      | [10,40]        |

^ (x,y] means the operating frequency is greater than x Hz, and equal to or less than y Hz.
```

By default, the field `HP_SYSTEM_SEC_DPA_CFG_SEL` in register `HP_SYSTEM_SEC_DPA_CONF_REG` is 0. In this case, the security-level is decided by the eFuse field `EFUSE_SEC_DPA_LEVEL`. If the field `HP_SYSTEM_SEC_DPA_CFG_SEL` is set to 1, the security-level is decided by `HP_SYSTEM_SEC_DPA_CFG_LEVEL` in register `HP_SYSTEM_SEC_DPA_CONF_REG`.

### 17.3.3 HP Core/LP Core Debug Control

The following register is used to debug between HP CPU and LP CPU. For more information on how to debug HP CPU and LP CPU, please refer to the Subsection 1.10 Debug in Chapter 1 High-Performance CPU.

*   `HP_SYSTEM_CORE_DEBUG_RUNSTALL_ENABLE`: Enable this bit to enable debug RunStall feature between HP CPU and LP CPU.

### 17.3.4 Bus Timeout Protection

The Bus Timeout Protection function can be enabled and the timeout threshold can be configured through the configuration register. When a transfer is initiated, the counter inside the Timeout Protection module will increase by one every clock cycle. When the accumulated value is less than the timeout threshold and the bus receives a response from the slave, the internal counter is cleared. When the accumulated value is greater than the timeout threshold, if the slave device has not responded to the transfer, the Timeout Protection module will force the bus return signal to be pulled high. At the same time, it will report the interrupt and record the abnormal access address and master ID.

#### 17.3.4.1 CPU Peripheral Timeout Protection Register

`HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG` is the timeout protection configuration register for accessing CPU peripheral registers. CPU peripherals refer to the peripherals or modules whose addresses are in the range of `0x600C_0000 ~ 0x600C_FFFF`. For corresponding peripheral information, please refer to Subsection 5.3.5 Modules/Peripherals Address Mapping in Chapter 5 System and Memory.

When a timeout occurs, the CPU_PERI_TIMEOUT_INTR interrupt will be asserted.

*   `HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG`: Enables timeout protection and configures the timeout threshold.
*   `HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR_REG`: When a timeout occurs, this register will record the address of the timeout.
*   `HP_SYSTEM_CPU_PERI_TIMEOUT_UID_REG`: When a timeout occurs, this register will record the address of the timeout.
```