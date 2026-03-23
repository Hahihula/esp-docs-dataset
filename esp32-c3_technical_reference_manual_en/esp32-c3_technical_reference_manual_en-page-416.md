

```markdown
prepare it for the next world switch.

However, it's worth noting that you cannot call the application in Non-secure world immediately after configuring the World Controller. For reasons such as CPU pre-indexed addressing and pipeline, it is possible that the CPU has already executed the application in Non-secure World before the World Controller configuration is effective, meaning the CPU runs unsecured application in the Secure World.

Therefore, you need to make sure the CPU only calls applications in the Non-secure world after the World Controller configuration takes effect. This can be guaranteed by declaring the applications in the Non-secure World as "noinline".

### 15.4.2 From Non-secure World to Secure World

```c
void main ( void ){
...
Function B entry addr ← ENTRY_ADDR(X)
ENTRY_CHECK=1<<X } configuration
...
Function B → Entry Secure World
}
```

**Figure 15.4-2. Switching From Non-secure World to Secure World**

CPU can only switch from Non-secure World to Secure World via Interrupts (or Exceptions). After configuring the World Controller, the CPU can switch back from Non-secure World to Secure World upon the configured Interrupt trigger.

## Configuring the World Controller

The detailed steps to configure the World Controller to switch the CPU from Non-secure World to Secure World are described below:

1. Configure the entry base address of interrupts or exception WCL_CORE_O_MTVEC_BASE_REG. After that, the World controller populates the monitored addresses for each entry as follows:
    - Exception entry: `WCL_CORE_O_MTVEC_BASE_REG + 0x00`
    - Interrupt entries: `WCL_CORE_O_MTVEC_BASE_REG + 4*i (i = 1~31)`

Note that this register must be configured to the mtvec CSR register of the CPU. When modifying the CPU's mtvec CSR registers, this register also must be updated. For details, please refer to Chapter 1 ESP-RISC-V CPU.
```