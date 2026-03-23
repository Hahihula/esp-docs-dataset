

```markdown
| ID | Description                     | Priority |
|----|----------------------------------|--------|
| 0  | U mode software interrupt       | 1      |
| 3  | M mode software interrupt       | 3      |
| 4  | U mode timer interrupt          | 0      |
| 7  | M mode timer interrupt          | 2      |

## 1.7 Core Local Interrupts (CLINT)

### 1.7.1 Overview

The CPU supports 4 local level-type interrupt sources with static priorities as shown below.

Table 1.7-1. Core Local Interrupt (CLINT) Sources

These interrupt sources have reserved IDs and fixed priorities which cannot be masked via the interrupt controller threshold registers for either modes.

Two of these interrupts (0 and 4) are by-default delegated to U mode as per the reset values of corresponding bits in `mideleg` CSR.

It must be noted that regardless of the fixed priority of CLINT interrupts, pending external interrupt sources always have higher priority over CLINT sources.

### 1.7.2 Features

*   4 local level-type interrupt sources with static priorities and IDs
*   Memory mapped configuration and status registers
*   Support for interrupts in both M and U modes
*   64-bit timer with interrupt with overflow flag
*   Software interrupts

### 1.7.3 Software Interrupt

M and U mode software interrupt sources are controlled by setting or clearing the memory mapped registers `MSIP` and `USIP`, respectively.

The `MSIE/USIE` bit must be set in `mie/uie` CSR for enabling the interrupt at core level for a particular mode.

Pending state of this interrupt can be checked for either mode by reading the corresponding bit `MSIP/USIP` in `mip/uip` CSR.

Note that by default U mode software interrupt with ID 0 has the corresponding bit set in `mideleg` CSR. This bit can be toggled for using the interrupt in M mode instead. Similarly the bit corresponding to M mode software interrupt can be set for using it in U mode.
```