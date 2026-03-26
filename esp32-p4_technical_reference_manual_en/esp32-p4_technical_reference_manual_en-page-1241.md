

```markdown
Chapter 20 System Registers (SYSREG)

The following fields in register HP_SYSTEM_HP_CACHE_CLK_CONFIG_REG control the clock signals of different HP cache. Writing 1 to respective fields enables the clock for respective cache.

* L1 ichache 0: `HP_SYSTEM_L1_IO_CACHE_CLK_ON`
* L1 ichache 1: `HP_SYSTEM_L1_I1_CACHE_CLK_ON`
* L1 dcache: `HP_SYSTEM_L1_D_CACHE_CLK_ON`
* L2 cache: `HP_SYSTEM_L2_CACHE_CLK_ON`

The following fields in register HP_SYSTEM_CACHE_RESET_CONFIG_REG control the reset signals of different HP cache. Writing 1 and then 0 to respective fields resets respective cache.

* L1 ichache 0: `HP_SYSTEM_L1_IO_CACHE_RESET`
* L1 ichache 1: `HP_SYSTEM_L1_I1_CACHE_RESET`
* L1 dcache: `HP_SYSTEM_L1_D_CACHE_RESET`

20.2.1.4 HP SPM and HP L2MEM Clock Configuration

The following register fields control the clock signals of HP SPM (Scratchpad Memory) and HP L2MEM. Writing 1 to respective register fields forcibly enable the clock of respective memory.

* HP SPM: `HP_SYSTEM_HP_SPM_CLK_FORCE_ON`
* L2MEM: `HP_SYSTEM_L2_MEM_CLK_FORCE_ON`
* L2ROM: `HP_SYSTEM_L2_ROM_CLK_FORCE_ON`

20.2.1.5 HP SPM Parity Check Configuration

ESP32-P4's has implemented Parity Check in HP SPM to detect one-bit memory flip error.

This feature can be configured and controlled via the following registers:

* `HP_SYSTEM_HP_SPM_PARITY_CHECK_CTRL_REG`: write 1 to enable the parity check in HP SPM.
* `HP_SYSTEM_HP_SPM_INIT_REG`: configures the initialization of HP SPM before enabling the parity check.

* Interrupt (`HP_SPM_PARITY_ERR_INT`) related registers:
    - `HP_SYSTEM_HP_SPM_INT_RAW_REG`: the raw interrupt status of `HP_SPM_PARITY_ERR_INT`
    - `HP_SYSTEM_HP_SPM_INT_ST_REG`: the masked interrupt status of `HP_SPM_PARITY_ERR_INT`
    - `HP_SYSTEM_HP_SPM_INT_ENA_REG`: write 1 to enable `HP_SPM_PARITY_ERR_INT`
    - `HP_SYSTEM_HP_SPM_INT_CLR_REG`: write 1 to clear `HP_SPM_PARITY_ERR_INT`

* `HP_SYSTEM_HP_SPM_PARITY_INT_RECORD_REG`: records the address when `HP_SPM_PARITY_ERR_INT` occurs.

* `HP_SYSTEM_HP_SPM_ERR_RESP_CTRL_REG`: write 1 so HP SPM reports parity error to the HP CPU and triggers exception.
```