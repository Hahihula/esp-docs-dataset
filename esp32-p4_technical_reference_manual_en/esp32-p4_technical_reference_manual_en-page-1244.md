

```markdown
Chapter 20 System Registers (SYSREG)

GoBack

* HP CPU and other AHB masters (ICM_CPU_ADDRHOLE_INT)
    - `HP_SYSTEM_ICM_CPU_ADDRHOLE_ADDR_REG`
    - `HP_SYSTEM_ICM_CPU_ADDRHOLE_INFO_REG`
* AXI masters (ICM_SYS_ADDRHOLE_INT)
    - `HP_SYSTEM_ICM_SYS_ADDRHOLE_ADDR_REG`
    - `HP_SYSTEM_ICM_SYS_ADDRHOLE_INFO_REG`

For detailed information on address space mapping, please refer to Chapter 7 System and Memory.

For detailed information on access permission management, please refer to Chapter 19 Permission Control (PMS).

20.2.1.14 HP CPU Bus Timeout Protection

ESP32-P4 supports Timeout Protection on HP CPU’s IBUS, DBUS and AHB bus.

When a transfer is initiated, the counter inside the Timeout Protection module increments by one on each clock cycle.

* If the accumulated value remains below the timeout threshold and the slave device responds to the transfer, the internal counter is cleared.
* If the accumulated value exceeds the timeout threshold and the slave device has not responded, the Timeout Protection module takes control of the bus to return an error response to the HP CPU. At the same time, an interrupt is generated.

Related control and configuration registers are described below.

HP CPU IBUS Timeout Protection

Configure `HP_SYSTEM_HP_CORE_IBUS_TIMEOUT_REG` to enable timeout protection and set the timeout threshold for HP CPU accessing HP SPM, L2MEM and EXT MEM by IBUS.

When a timeout occurs, the `HP_COREx_IBUS_TIMEOUT_INT` interrupt will be asserted.

HP CPU DBUS Timeout Protection

Configure `HP_SYSTEM_HP_CORE_DBUS_TIMEOUT_REG` to enable timeout protection and set the timeout threshold for HP CPU accessing HP SPM, L2MEM and EXT MEM by DBUS.

When a timeout occurs, the `HP_COREx_DBUS_TIMEOUT_INT` interrupt will be asserted.

HP CPU AHB BUS Timeout Protection

Configure `HP_SYSTEM_HP_CORE_AHB_TIMEOUT_REG` to enable timeout protection and set the timeout threshold for HP CPU accessing LP peripherals, HP peripherals registers by AHB bus.

When a timeout occurs, the `HP_COREx_AHB_TIMEOUT_INT` interrupt will be asserted.
```