

```markdown
Register 52.18. EMACMIIADDR_REG (0x0010)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 16  | MIIDEV                                                                      |
| 15  | MIIREG                                                                      |
| 11  | MIICSRCLK                                                                   |
| 10  | MMIWRITE                                                                    |
| 9   | MIIBUSY                                                                     |
| 8-2 | (reserved)                                                                  |
| 1   | (reserved)                                                                  |
| 0   | Reset                                                                      |

MIIDEV Configures which of the 32 possible PHY devices are being accessed. (R/W)

MIIREG Configures the desired address register in the selected PHY device. (R/W)

MIICSRCLK Configures the CSR clock frequency.
- 0: APB clock frequency is 80 MHz, and MDC clock frequency is APB_CLK/42
- 3: APB clock frequency is 40 MHz, and MDC clock frequency is APB_CLK/26
Other values are reserved (R/W)

MMIWRITE Configures the direction of the operation that uses MII_DATA.
- 0: Read operation
- 1: Write operation
(R/W)

MIIBUSY Configures the state of the MII.
- 0: Idle
- 1: Busy
This bit is used in combination with MIIREG and MII_DATA.
This bit should read logic 0 (default) before writing to MIIREG and MII_DATA.
To read or write to MIIREG and MII_DATA, software (the user) should set this field to 1.
MII_DATA should be kept valid (data remains unchanged) when it is accessed until this field is cleared by hardware (the MAC).
Note that ESP32-P4 MAC does not receive ACK from PHY during a read or write access to MIIREG and MII_DATA. (R/WS/SC)

Register 52.19. EMACMIIADATA_REG (0x0014)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| 16  | MII_DATA    |
| 15  |             |
| ... | ...         |
| 2   |             |
| 1   |             |
| 0   | Reset       |

MII_DATA Configures the 16-bit data value read from the PHY after a Management Read operation or the 16-bit data value to be written to the PHY before a Management Write operation. (R/W)
```