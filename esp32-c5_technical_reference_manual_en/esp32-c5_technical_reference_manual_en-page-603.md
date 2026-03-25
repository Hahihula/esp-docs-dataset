

```markdown
- Peripherals + ROM: It mainly includes bus, HP peripherals.
- Internal SRAMx: It is divided into four sub-power domains, as shown in Figure 13.4-1, where each of SRAM0/1/2 has an independent power switch, while SRAM3 is directly connected to the regulator without a power switch.
- Modem Power: It mainly includes modules that control the operating of the wireless section.

There is an independent power switch between the regulator and each power domain, enabling up/down control of the digital power domain.

• The LP system contains the following digital power domains:
  - LP PD peripherals: It mainly includes the LP CPU and LP peripherals.
  - LP always-on: It mainly includes LP always-on peripherals (e.g., RTC timer) and PMU controller. This power domain keeps powered up all the time.

13.4.1.3 Analog Power Domains

• The HP system contains the following analog power domains:
  - PLL
• The LP system contains the following analog power domains:
  - External Main Clock
  - Fast RC Oscillator
  - RF circuit

13.4.2 PMU

The PMU of ESP32-C5 controls power consumption-related components of each power domain, such as power and clock. PMU consists of the following major parts:

• PMU main state machine: It records and switches the PMU states.
• Sleep/wake-up controller: It sends sleep or wake-up requests to the PMU main state machine.
• Power controllers: They control the power and clock signals depending on the power modes of the chip. The power controllers include:
  - Digital power controller: It powers up or down the digital power domains.
  - Analog power controller: It enables the analog modules, such as the regulators, analog clocks, etc.
  - Clock controller: It manages the clock gating of peripherals and selects analog clock sources for digital clocks.
  - Data backup controller: It controls the data backup and restore process when the chip switches between PMU states.
  - System controller: It controls some system-level modules, such as suspending watchdog functionality in sleep mode (when the CPU is unavailable).

The PMU workflow involves the following steps:
```