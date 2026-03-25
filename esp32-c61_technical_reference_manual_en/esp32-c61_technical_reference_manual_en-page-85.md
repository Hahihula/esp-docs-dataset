

```markdown
| ID | Description |
|----|-------------|
| 3  | M mode software interrupt |
| 7  | M mode timer interrupt |

### 1.8.3.2 Features
* Two local level-type machine mode interrupt sources with programmable priorities
* Memory-mapped configuration and status registers
* 64-bit timer with interrupt functionality, overflow flags, and three sampling modes
* Software interrupt

### 1.8.3.3 Software Interrupt
An M mode software interrupt is controlled by setting or clearing the memory-mapped register MSIP.
The register bit clicintie[3] must be set for enabling the software interrupt at the core level.
Pending state of this interrupt can be checked by reading the corresponding bit of clicintip register of interrupt 3 in CLIC, that is clicintip[3] bit.

### 1.8.3.4 Timer Counter and Interrupt
The timer counter can be enabled by setting the mtime_EN bit in mtimectl. mtimecmplo and mtimecmphi registers are set to the value for comparison with system timer with lower and higher 32 bits respectively. The CPU provides two local memory-mapped 32-bit wide registers mtimeloadlo and mtimeloadhi, which has both read/write access, to load the system timer with a specific value.
Interrupt for M mode is asserted when 64-bit value of system timer value exceeds the 64-bit combined value of mtimecmplo and mtinecmphi.
Pending state of timer interrupt is reflected as IP bit of clicintip register of interrupt 7 in CLIC.
For de-asserting the pending timer interrupt in M mode, either IE bit of clicintie register of interrupt 7 in CLIC has to be cleared or the value of the mtinecmplo and mtinecmphi register needs to be updated.

### 1.8.3.5 Register Summary
The addresses in this section are relative to CPU sub-system base address i.e. 0x20000000.
```