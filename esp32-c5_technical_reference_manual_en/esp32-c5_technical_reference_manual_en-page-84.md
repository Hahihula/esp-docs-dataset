

```markdown
## 2.8 Interrupt Controller

### 2.8.1 Overview

The HP core uses the CLIC + CLINT scheme for implementing and supporting interrupts.

CLINT stands for core-local interrupts, which are sources local to the HP core subsystem for generating timer and software interrupts for the HP core.

CLIC stands for core-local interrupt controller, which provides low-latency, vectored, and pre-emptive interrupts for the HP core. The HP core CLIC unit supports 32 external interrupts and 2 CLINT interrupts.

### 2.8.2 CLIC

#### 2.8.2.1 Overview

The HP core CLIC implementation follows the proposal: Core-Local Interrupt Controller (CLIC) RISC-V Privileged Architecture Extensions, by RISC-V International. At the time of writing this section, the official proposal was yet to be ratified, hence, the following specifications may differ from the ratified version.

Only the CLIC mode of operation is supported by the HP core, i.e. mtvec.MODE is hardwired to 0x3. Hence, the basic RISC-V interrupt handling scheme and the associated CSRs (such as mie, mip, mideleg, uie, and uip) are unavailable.

Only machine mode interrupts are supported.

#### 2.8.2.2 CLIC CSRs

The following machine-mode CSRs are relevant for interrupt handling in the CLIC scheme:

- mstatus
- mtvec
- mtvt
- mscratch
- mepc
- mcause
- mnxti
- mintthresh
- mintstatus
- mclicbase
- mscratchcsw
- mscratchcswl

In CLIC mode, the global interrupt enable for the machine mode is still dictated by the mstatus.MIE bit.

Each interrupt can be either vectored or non-vectored depending on the clicintattr[i].SHV bit.

For a non-vectored interrupt, the HP core jumps to the trap handler base address as configured in mtvec.BASE field.

The base address of the vector table is configured in mtvt. For a vectored interrupt, the HP core jumps to the 32-bit word address stored at the corresponding index in the vector table. For example, for the "i"th machine mode interrupt, first the 32-bit address stored at the memory location "mtvt + 4*i" will be loaded, after which the HP core will treat the loaded data as an address and jump to it.

Upon taking an interrupt, the HP core will store the address of the instruction that was interrupted in mepc. Also, the HP core will update the value of mcause based on the interrupt's ID.
```