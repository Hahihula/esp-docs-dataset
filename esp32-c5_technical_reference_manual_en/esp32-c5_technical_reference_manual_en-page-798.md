

```markdown
| Security-Level Name | Security-Level Value | PLL_CLK (MHz) | XTAL_CLK (MHz) |
|---------------------|----------------------|---------------|----------------|
| SEC_DPA_OFF         | 0                    | 160           | 48             |
| SEC_DPA_LOW         | 1                    | (120,160)^A   | (24,48)^A      |
| SEC_DPA_MIDDLE      | 2                    | (96,160)^A    | (16,48)^A      |
| SEC_DPA_HIGH        | 3                    | (80,160)^A    | (9.6,48)^A     |

^A (x,y] means the operating frequency is greater than x Hz, and equal to or less than y Hz.
```

By default, the field `HP_SYSTEM_SEC_DPA_CFG_SEL` in register `HP_SYSTEM_SEC_DPA_CONF_REG` is 0. In this case, the security-level is decided by the eFuse field `EFUSE_SEC_DPA_LEVEL`. If the field `HP_SYSTEM_SEC_DPA_CFG_SEL` is set to 1, the security-level is decided by `HP_SYSTEM_SEC_DPA_CFG_LEVEL` in register `HP_SYSTEM_SEC_DPA_CONF_REG`.

## 19.3.3 HP CPU/LP CPU Debug Control

Register `HP_SYSTEM_CORE_DEBUG_RUNSTALL_ENABLE` controls the RunStall feature, which facilitates the debugging of HP CPU and LP CPU. If enabled, when any of the HP CPUs is in debug mode, the other one is stalled automatically.

For details, please refer to the Subsection 2.10.1 Debug in Chapter 2 High-Performance CPU.

## 19.3.4 Bus Timeout Protection

ESP32-C5 supports bus timeout protection and allows configurable timeout threshold. When a transfer is initiated, the internal counter of the timeout protection module increments by 1 on each clock cycle.

* If the accumulated value remains below the timeout threshold and a response is received from the slave device, the counter is cleared.
* If the accumulated value exceeds the threshold and no response has been received, the module forces the bus return signal high to terminate the transfer. At the same time, an interrupt is triggered, and the module logs the exception address and the master ID associated with the access.

### 19.3.4.1 CPU Peripheral Timeout Protection Register

Register `HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG` configures the timeout protection for accessing CPU peripherals, which refer to the peripherals or modules whose addresses are in the range of `0x600C_0000–0x600C_FFFF`. For details, please refer to Subsection 6.3.5 Modules/Peripherals Address Mapping in Chapter 6 System and Memory.

When a timeout occurs, the `CPU_PERI_TIMEOUT_INTR` interrupt will be triggered.

* `HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG`: Enables timeout protection and configures the timeout threshold.
* `HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR_REG`: When a timeout occurs, this register will record the address of the timeout.
```