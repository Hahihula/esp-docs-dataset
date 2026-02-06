Title: 
8 Module Schematics

Subtitle:
This is the reference design of the module.

Section Title (Left):
ESP8685 Core

Body Text and Diagram Annotations:

- The values of C1 and C2 vary with the selection of the crystal.
  
  - The value of R1 varies with the actual PCB board. R1 could be a resistor or inductor, the initial value is suggested to be 24 pH.

- vpp33

- GND
- VDD33
  
- ANT1
- PCBAANT
- RF ANT
- LNA_IN
- C8
- C9
- R3
- R5
- U2
- ESP8685
- 10K
- CHIP_EN

- The values of C8, L2 and C9 vary with the actual PCB board.
  
  - NC: No component.

- VDD33
  
- GPIO3
- GPIO4
- GPIO5
- GPIO7
- GPIO6
- GPIO1
- GPIO0
- GND

- R2 = 499 (40MHz@10ppm)
- U0TXD
- VDD33
- D1 ESD
  
- Test Point

- CHIP_EN
- EN
- TP1
- U0TXD
- TX
- TP2
- U0RXD
- RX
- TP3
- GND
- TP4
- GND
- TP5
- VDD33
- 3V3
- TP6
- GPIO9

Section Title (Right):
ESP8685-WROOM-03 (pin-out)

Table:

| Pin.11 | IO4 |
| Pin.1  | EN  |
| Pin.10 | GND |
| Pin.2  | GPIO1 |
| Pin.9  | TX  |
| Pin.3  | I/O6 |
| Pin.8  | RX  |
| Pin.4  | I/O7 |
| Pin.5  | GND |
| Pin.6  | IO3 |
| Pin.0  | 3V3 |

Figure Caption:
Figure 8-1. Schematics

Side Text (Left):
ESP8685-WROOM-03 Datasheet v1.2
Submit Documentation Feedback