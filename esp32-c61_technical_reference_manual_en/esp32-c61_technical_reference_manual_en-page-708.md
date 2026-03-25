

```markdown
| Security-Level Name | Security-Level Value | PLL_CLK (MHz) | XTAL_CLK (MHz) |
|---------------------|----------------------|---------------|----------------|
| SEC_DPA_OFF         | 0                    | 160           | 40             |
| SEC_DPA_LOW         | 1                    | [120,160]     | [20,40]        |
| SEC_DPA_MIDDLE      | 2                    | [96,160]      | [13,40]        |
| SEC_DPA_HIGH        | 3                    | [80,160]      | [8,40]         |

^ (x,y] means the operating frequency is greater than x MHz, and equal to or less than y MHz.
```

The field `HP_SYSTEM_SEC_DPA_CFG_SEL` in register `HP_SYSTEM_SEC_DPA_CONF_REG` can be:

*   0 (default): The security-level is decided by the eFuse field `EFUSE_SEC_DPA_LEVEL`.
*   1: The security-level is decided by `HP_SYSTEM_SEC_DPA_CFG_LEVEL` in register `HP_SYSTEM_SEC_DPA_CONF_REG`.

### 17.3.3 Bus Timeout Protection

ESP32-C61 supports APB bus timeout protection and allows configurable timeout threshold. When a transfer is initiated, the internal counter of the timeout protection module increments by 1 on each clock cycle.

*   If the accumulated value remains below the timeout threshold and a response is received from the slave device, the counter is cleared.
*   If the accumulated value exceeds the threshold and no response has been received, the module forces the bus return signal high to terminate the transfer. At the same time, an interrupt is triggered, and the module logs the exception address and the master ID associated with the access.

#### 17.3.3.1 CPU Peripheral Timeout Protection Register

Register `HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG` configures the timeout protection for accessing CPU peripherals, which refer to the peripherals or modules whose addresses are in the range of `0x600C_0000–0x600C_FFFF`. For details, please refer to Subsection 4.3.5 Modules/Peripherals Address Mapping in Chapter 4 System and Memory.

When a timeout occurs, the `CPU_PERI_TIMEOUT_INTR` interrupt will be triggered. The related registers are:

*   `HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG`: Enables timeout protection and configures the timeout threshold.
*   `HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR_REG`: When a timeout occurs, this register will record the address of the timeout.
*   `HP_SYSTEM_CPU_PERI_TIMEOUT_UID_REG`: When a timeout occurs, this register will record the master ID of the timeout.

#### 17.3.3.2 HP Peripheral Timeout Protection Register

Register `HP_SYSTEM_HP_PERI_TIMEOUT_CONF_REG` configures the timeout protection for accessing HP peripherals, which refer to the peripherals or modules whose addresses are in the range of
```