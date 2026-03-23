

```markdown
Register 7.8. GPIO_IN_REG (0x003C)

GPIO_IN_DATA_NEXT Represents the input value of GPIO0 ~ GPIO30. Each bit represents a pin input value:
O: Low level
1: High level
Bit0 ~ bit30 are corresponding to GPIO0 ~ GPIO30. Bit31 is invalid.
(RO)

Register 7.9. GPIO_STATUS_REG (0x0044)

GPIO_STATUS_INTERRUPT The interrupt status of GPIO0 ~ GPIO30, can be configured by the software.

- Bit0 ~ bit30 are corresponding to GPIO0 ~ GPIO30. Bit31 is invalid.
- Each bit represents the status of its corresponding GPIO:
  - 0: Represents the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE, or this bit is configured to 0 by the software.
  - 1: Represents the GPIO generates the interrupt configured by GPIO_PINn_INT_TYPE, or this bit is configured to 1 by the software.

(R/W/WTC)
```