

```markdown
Register 20.115. LP_SYSTEM_LP_CORE_ERR_RESP_DIS_REG (0x01BC)

LP_SYSTEM_LP_CORE_ERR_RESP_DIS   Configures whether or not to disable error response for respective LP CPU buses.
bit-0: IBUS
bit-1: DBUS
bit-2: AHB bus
(R/W)


Register 20.116. LP_SYSTEM_RNG_CFG_REG (0x01C0)

LP_SYSTEM_RNG_TIMER_EN   Configures whether or not to enable RNG timer.
O: Disable
1: Enable
(R/W)

LP_SYSTEM_RNG_TIMER_PSCALE   Configures the clock division factor for the RNG timer. (R/W)

LP_SYSTEM_RNG_SAR_ENABLE   Configures whether or not to enable RNG_SARADC.
O: Disable
1: Enable
(R/W)

LP_SYSTEM_RNG_SAR_DATA   Represents the analog SAR3_CAP value, which is used for debugging RNG_SARADC sample count. (RO)
```