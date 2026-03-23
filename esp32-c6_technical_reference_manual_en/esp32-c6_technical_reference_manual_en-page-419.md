

```markdown
## 12.4.1.2 Digital Power Domains

ESP32-C6 has digital power domains as listed below. The HP sys regulator powers the HP system, and there is an independent power switch between the regulator and each power domain, enabling up/down control of the digital power domain. The LP sys regulator powers the LP system.

*   The HP system contains the following digital power domains:
    -   **CPU**: It mainly includes the CPU and its supporting peripherals (such as TRACE).
    -   **Modem**: It consists of wireless MAC and baseband.
    -   **Peripherals + ROM**: It mainly includes bus, HP peripherals.
    -   **Internal SRAMx**: It is divided into four sub-power domains, as shown in Figure 12.4-1, where each of SRAMO/1/2 has an independent power switch, while SRAM3 is directly connected to the regulator without a power switch.
    -   **Modem Power**: It mainly includes modules that control the operating of the wireless section.

*   The LP system contains the following digital power domains:
    -   **LP PD peripherals**: It mainly includes LP CPU, LP peripherals.
    -   **LP always-on**: It mainly includes LP always-on peripherals (e.g., RTC timer), PMU controller. This power domain keeps powered on all the time.

## 12.4.1.3 Analog Power Domains

As Figure 12.4-1 shows, ESP32-C6 contains the following analog power domains, among which PLL belongs to the HP system while the other domains belong to the LP system:

*   External Main Clock
*   Fast RC Oscillator
*   PLL
*   RF circuit

## 12.4.2 PMU

The PMU of ESP32-C6 controls power consumption-related components of each power domain, such as power and clock. PMU consists of the following major parts:

*   **PMU main state machine**: It records and switches the PMU states.
*   **Sleep/wake-up controller**: It sends sleep or wake-up requests to the PMU main state machine.
*   **Power controllers**: They control the power and clock signals depending on the power modes of the chip. The power controllers include:
    -   **Digital power controller**: It powers up or down the digital power domains.
    -   **Analog power controller**: It enables the analog modules, such as the regulators, analog clocks, etc.
    -   **Clock controller**: It manages the clock gating of peripherals and selects analog clock sources for digital clocks.
```