

```markdown
Chapter 12 Event Task Matrix (ETM) GoBack


12.5 Registers

The addresses in this section are relative to Event Task Matrix base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.


Register 12.1. SOC_ETM_CH_ENA_ADO_REG (0x0000)

[Diagram: Bitfield register layout with bit positions 31–0 labeled as follows:]

Bit Positions:
31 30 29 28 27 26 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 0
+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+
|   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 Reset

SOC_ETM_CH_ENABLEDn (n: 0-31) Represents channel n enable status.
O: Disable
1: Enable
(R/WTC/WTS)


Register 12.2. SOC_ETM_CH_ENA_AD1_REG (0x000C)

[Diagram: Bitfield register layout with bit positions 31–0 labeled as follows:]

Bit Positions:
31 (reserved)
+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+
|   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 Reset

SOC_ETM_CH_ENABLEDn (n: 32-49) Represents channel n enable status.
O: Disable
1: Enable
(R/WTC/WTS)
```