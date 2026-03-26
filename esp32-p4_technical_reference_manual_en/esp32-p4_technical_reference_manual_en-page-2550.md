

```markdown
powering down the connected SPRAM clock. Note that this power saving mode is different from the power savings via SRP.

*   Data FIFO RAM Interface
    The multiple FIFOs used by the controller core are not actually located within the controller core itself, but on the Single-Port RAM (SPRAM). FIFOs are dynamically sized, thus are allocated at run-time in the SPRAM. When the CPU, DMA, or the controller core attempts to read/write to FIFOs, those accesses are routed through the data FIFO RAM interface.

## 50.4.2 Memory Layout

Figure 50.4-2 illustrates the memory layout of the registers which are used to configure and control the USB Controller Core. Note that USB External Controller uses a separate set of registers called wrap registers.

```
Figure 50.4-2. OTG_FS Register Layout
```

### 50.4.2.1 Control & Status Registers (CSRs)

*   **Core Global CSRs**
    These registers are responsible for the configuration/control/status of the global features of OTG_FS, i.e., features which are common to both Host and Device modes. These features include:
        -   OTG control (HNP, SRP, and A/B-device detection);
        -   USB configuration (Host or Device mode selection and PHY selection);
        -   and system-level interrupts.
```