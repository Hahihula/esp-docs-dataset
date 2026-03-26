

```markdown
Chapter 20 System Registers (SYSREG)

GoBack

Chapter 20

System Registers (SYSREG)

20.1 Overview

ESP32-P4 includes various features that can be configured through dedicated registers. This chapter mainly enumerates such registers. For detailed introduction about a specific feature, please go to respective chapters.

20.2 Function Description

20.2.1 HP System Registers

20.2.1.1 External Memory Encryption/Decryption Configuration

Register `HP_SYSTEM_CRYPTO_CTRL_REG` configures encryption and decryption options of the external memory (external Flash and RAM). For details, please refer to Chapter 32 External Memory Encryption and Decryption (XTS_AES).

20.2.1.2 HP Peripherals Clock Configuration and Power Control

The following registers are used to control the power signals of memory in corresponding peripherals.

* RSA: `HP_SYSTEM_HP_RSA_PD_CTRL_REG`
* ECC: `HP_SYSTEM_HP_ECC_PD_CTRL_REG`
* RSA: `HP_SYSTEM_HP_UART_PD_CTRL_REG`

The following fields in register `HP_SYSTEM_HP_PERI_MEM_CLK_FORCE_ON_REG` control the clock gating signals of memory in corresponding peripherals.

* GDMA: `HP_SYSTEM_GDMA_MEM_CLK_FORCE_ON`
* BitScrambler
    * TX memory: `HP_SYSTEM_BITSCRAMBLER_TX_MEM_CLK_FORCE_ON`
    * RX memory: `HP_SYSTEM_BITSCRAMBLER_RX_MEM_CLK_FORCE_ON`
* RMT: `HP_SYSTEM_RMT_MEM_CLK_FORCE_ON`

20.2.1.3 HP Cache Clock and Reset Configuration

ESP32-P4 allows software to directly control the clock and reset signals of HP cache.
```