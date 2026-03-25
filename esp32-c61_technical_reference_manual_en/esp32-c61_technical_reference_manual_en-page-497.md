

```markdown
Chapter 11 Low-Power Management GoBack

They are used for regulating the power supply to low-power modules, and also feature regulated output power.

11.4.1.2 Digital Power Domains

ESP32-C61 has digital power domains in the HP system and LP system as listed below.

* The HP system contains the following digital power domains:

  - CPU: includes the CPU and its supporting peripherals (such as TRACE) in the HP system.
  - Modem: consists of wireless MAC, baseband and respective peripheral controllers.
  - Internal SRAMx: As shown in Figure 11.4-1, each of SRAM0/1/2 has an independent power switch, while SRAM3 is directly connected to the regulator without a power switch.
  - Modem Power: includes modules that control the operating of the wireless section.
  - Peripherals+ROM: includes ROM, HP peripherals, and all other modules in the HP system that are not mentioned above.

* The LP system contains the following digital power domains:

  - LPSYS_OFF: includes LP peripherals APB bus, and Ipperi clk.
  - LPSYS: includes all modules in the LP system except for LPSYS_OFF, such as LP always-on peripherals (e.g., RTC timer) and PMU controller. This power domain has the highest priority among all power domains and remains powered on unless the chip is completely powered down.

Power domains in the HP system and LP system are powered by HP system regulators and LP system regulators respectively. There is an independent power switch between the regulators and each power domain, enabling up/down control of the digital power domain. With the exception of LPSYS — which remains always-on and thus does not require power gating — power control for the digital power domains can be achieved.

11.4.1.3 Analog Power Domains

As Figure 11.4-1 shows, ESP32-C61 contains the following analog power domains, among which PLL belongs to the HP system while the other domains belong to the LP system:

* External Main Clock
* Fast RC Oscillator
* PLL
* RF circuit

11.4.2 PMU

The PMU of ESP32-C61 controls power consumption-related components of each power domain, such as power and clock. PMU consists of the following major parts:

* PMU main state machine: records and switches the PMU states.
* Sleep/wake-up controller: sends sleep or wake-up requests to the PMU main state machine.
* Power controllers: control the power and clock signals depending on the power modes of the chip. The power controllers include:
```