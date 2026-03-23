

```markdown
## 12.4.1 Power Scheme

Figure 12.4-1 shows the power scheme of ESP32-C6 that mainly includes:

* Two regulators
* Analog power domains
* Digital power domains

**Figure 12.4-1. ESP32-C6 Power Scheme**

```
[Diagram: Block diagram showing power flow and components]

Analog domain:
- LP sys regulator
- HP sys regulator

Digital domain:
- External Main Clock
- Fast RC Oscillator
- PLL
- RF Circuit
- Internal SRAMx (x=0/1/2)
- Internal SRAMx (x=3)
- ROM
- CPU
- Modem
- Peripherals
- LP always-on peripherals
- LP CPU
- LP peripherals
- LP PD peripherals

Control signals: solid black arrows
Power lines: dashed red lines

LP system:
- LP always-on power supply path to PMU and LP peripherals/CPU

HP system:
- HP sys regulator powers main digital blocks including CPU, SRAM, ROM, Modem, etc.
```

### 12.4.1.1 Regulators

As shown in Figure 12.4-1, the analog part of ESP32-C6 contains two regulators that regulate the power supply to different power domains. The two regulators are:

* One HP sys regulator, used for regulating the power supply to high-performance modules. It features high drive strength, high power consumption, and regulated output power.
* One LP sys regulator, used for regulating the power supply to low-power modules. It also features regulated output power.
```