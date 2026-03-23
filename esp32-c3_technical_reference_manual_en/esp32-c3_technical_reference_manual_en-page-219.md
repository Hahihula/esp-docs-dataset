

```markdown
Chapter 9  
Low-power Management  

9.1 Introduction  

ESP32-C3 has an advanced Power Management Unit (PMU), which can flexibly power up different power domains of the chip, to achieve the best balance among chip performance, power consumption, and wakeup latency. To simplify power management for typical scenarios, ESP32-C3 has predefined four power modes, which are preset configurations that power up different combinations of power domains. On top of that, the chip also allows the users to independently power up any particular power domain to meet more complex requirements.  

9.2 Features  

ESP32-C3’s low-power management supports the following features:  
- Four predefined power modes to simplify power management for typical scenarios  
- Up to 8 KB of retention memory  
- 8 x 32-bit retention registers  
- RTC Boot supported for reduced wakeup latency  

In this chapter, we first introduce the working process of ESP32-C3’s low-power management, then introduce the predefined power modes of the chip, and at last, introduce the RTC boot of the chip.  

9.3 Functional Description  

ESP32-C3’s low-power management involves the following components:  
- Power management unit: controls the power supply to Analog, RTC and Digital power domains.  
- Power isolation unit: isolates different power domains, so any powered down power domain does not affect the powered up ones.  
- Low-power clocks: provide clocks to power domains working in low-power modes.  
- RTC timer: logs the status of the RTC main state machine in dedicated registers.  
- 8 x 32-bit “always-on” retention registers: These registers are always powered up and are not affected by any low-power modes, thus can be used for storing data that cannot be lost.  
- 6 x “always-on” pins: These pins are always powered up and are not affected by any low-power modes, which makes them suitable for working as wakeup sources when the chip is working in the low-power
```