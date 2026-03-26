

```markdown
- The HP (high-performance) system regulator has strong drive capability, higher power consumption, and adjustable output voltage. It is only suitable for power-up and sleep modes.
- The LP (low-power) system regulator regulates the power supply of low-power modules. Its output voltage is also adjustable.

The DCDC voltage regulation feedback system and the HP system regulator are responsible for powering the HP system. The external DCDC can adjust its output voltage through the internal voltage feedback system. By default, the chip is powered by the HP system regulator when powered up. After power-up is complete, it is recommended to switch to the DCDC power supply for better efficiency and load capacity.

### 14.4.1.2 Digital Power Domains

- The HP system contains the following digital power domains:
    - CPU (PD_HP_CPU): Mainly includes the CPU and peripherals that support its operation.
    - Peripherals + ROM (PD_TOP): Mainly includes the bus and HP peripherals.
    - L2MEM_GO–G5: It is divided into six sub-power domains, as shown in Figure 14.4-1.
    - HP_CNNT (PD_HP_CNINT): Mainly includes USB and SDIO modules.

There is an independent power switch between the regulator and each power domain, enabling up/down control of the digital power domain.

- The LP system contains the following digital power domains:
    - LP PD peripherals (PD_LP_PERI): Mainly includes LP CPU and LP peripherals.
    - LP always-on (PD_AON): It mainly includes LP always-on peripherals (e.g., RTC timer) and PMU controller. This power domain keeps powered up all the time.

### 14.4.1.3 Analog Power Domains

- The HP system contains the following analog power domains:
    - CPLL_CLK
    - SPLL_CLK
    - Audio PLL
    - SDIO PLL

- The LP system contains the following analog power domains:
    - External Main Clock
    - Fast RC Oscillator

### 14.4.1.4 Battery Power Domain

The battery power domain (VDD_BAT) serves as a backup power domain. When all external power supplies (VDD_ANA) are turned off, the low-power system regulators, LP_SLOW_CLK, and LP_FAST_CLK can all be powered by the VDD_BAT supply.
```