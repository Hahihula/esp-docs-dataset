

```markdown
Chapter 20 System Registers (SYSREG)

- The adjustable voltage range is 0 to (0.7 * VDDPST_6) V.
- The adjustable step is 0.1 * VDDPST_6 V.

For details, please refer to Chapter 63 Analog Voltage Comparator.

20.2.2.9 Illegal Access and Unauthorized Access

ESP32-P4's buses return error response and record transfer address, transfer direction, and master id when illegal access and unauthorized access occur.

- Illegal access: access to unmapped address space
- Unauthorized access: access to mapped address space without permission

Such information will be logged in the following registers:

- For LP CPU’s access by IBUS and DBUS (IDBUS_ADDRHOLE_INTR)
  - LP_SYSTEM_IDBUS_ADDRHOLE_ADDR_REG
  - LP_SYSTEM_IDBUS_ADDRHOLE_INFO_REG
- For LP CPU’s access by AHB or an access from HP CPU (LP_ADDRHOLE_INTR):
  - LP_SYSTEM_LP_ADDRHOLE_ADDR_REG
  - LP_SYSTEM_LP_ADDRHOLE_INFO_REG

For detailed information on address space mapping, please refer to Chapter 7 System and Memory.

For detailed information on access permission management, please refer to Chapter 19 Permission Control (PMS).

20.2.2.10 LP Bus Timeout Protection

ESP32-P4 supports Timeout Protection on LP CPU’s IBUS, DBUS and AHB bus.

When a transfer is initiated, the counter inside the Timeout Protection module increments by one on each clock cycle.

- If the accumulated value remains below the timeout threshold and the slave device responds to the transfer, the internal counter is cleared.
- If the accumulated value exceeds the timeout threshold and the slave device has not responded, the Timeout Protection module takes control of the bus to return an error response to the LP CPU. At the same time, an interrupt is generated.

Related control and configuration registers are described below.

LP CPU IBUS Timeout Protection

Configure LP_SYSTEM_LP_CORE_IBUS_TIMEOUT_REG to enable timeout protection and set the timeout threshold for LP CPU accessing LPROM and LP SPM by IBUS. When a timeout occurs, the LP_CORE_IBUS_TIMEOUT_INTR interrupt will be asserted.
```