

```markdown
Chapter 1 High-Performance CPU

GoBack

1.9 Interrupt Controller

1.9.1 Overview

Each HP core uses the CLIC + CLINT scheme for implementing and supporting interrupts.

CLINT stands for core-local interrupts, which are sources local to the HP core subsystem for generating timer and software interrupts for each HP core.

CLIC stands for core-local interrupt controller, which provides low-latency, vectored, pre-emptive interrupts for each HP core. Each HP core CLIC unit supports 32 external interrupts and 2 CLINT interrupts.

1.9.2 CLIC

1.9.2.1 Overview

The HP core CLIC implementation follows the official specification: Core-Local Interrupt Controller (CLIC) RISC-V Privileged Architecture Extensions (10/10/2023).

Only the CLIC mode of operation is supported by the HP core, i.e. mtvec.MODE is hardwired to 0x3. Hence, the basic RISC-V interrupt handling scheme and the associated CSRs (such as mie, mip, mideleg, uie, and uip) are unavailable.

HP core supports machine mode interrupt as well as user mode interrupt delegation.

1.9.2.2 CLIC CSRs

The following machine mode CSRs are relevant for interrupt handling in the CLIC scheme:

- mstatus
- mtvec
- mtvt

- mscratch
- mepc
- mcause

- mnxti
- mintthresh
- mintstatus

- mclicibase
- mscratchcsw
- mscratchcswl

As mentioned earlier, the CLIC mode is decided by the mtvec.MODE field. In each HP core, these bits are hardwired to 0x3, indicating that only the CLIC mode is supported.

In CLIC mode, the global interrupt enable for machine mode is still dictated by the mstatus.MIE bit.

interrupt can be either vectored or non-vectored depending on the clicintattr[ ].SHV bit.

For a non-vectored interrupt, the HP core jumps to the trap handler base address as configured in mtvec.BASE field.

For a vectored interrupt, the HP core jumps to the 32-bit word address stored at the corresponding index in the vector table. For example, for the "i"th machine mode interrupt, first the 32-bit address stored at the memory location "mtvt + 4*i" will be loaded, after which the HP core will treat the loaded data as an address and jump to it. The base address of the vector table is configured in mtvt.

Upon taking an interrupt, the HP core will store the address of the instruction that was interrupted in mepc. Also, the HP core will update the value of mcause based on the interrupt's ID.
```