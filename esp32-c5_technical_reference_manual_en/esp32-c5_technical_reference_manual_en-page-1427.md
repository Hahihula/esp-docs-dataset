

```markdown
Register 38.32. TWAIFD_ERR_NORM_ERR_FD_REG (0x0034)

| Bit Range | Description                  |
|-----------|------------------------------|
| 16-15     | TWAIFD_ERR_FD_VAL            |
|           |                              |
| 31        |                              |
|           |                              |
| 0x00      | Reset                        |

TWAIFD_ERR_NORM_VAL Represents the number of errors in the nominal bit time. (RO)

TWAIFD_ERR_FD_VAL Represents the number of errors in the data bit time. (RO)


Register 38.33. TWAIFD_CTR_PRES_REG (0x0038)

| Bit Range | Description                  |
|-----------|------------------------------|
| 12-0      | (reserved)                   |
|           |                              |
| 31        |                              |
|           |                              |
| 0x0       | Reset                        |

TWAIFD_CTPV Configures the pre-defined value to set the error counter. (WO)

TWAIFD_PTX Configures whether to set the receiver error counter to the pre-defined value.
O: Invalid
1: Set
(WT)

TWAIFD_PRX Configures whether to set the transmitter error counter to the pre-defined value.
O: Invalid
1: Set
(WT)

TWAIFD_ENORM Configures whether to erase the error counter of the nominal bit time.
O: Invalid
1: Erase
(WO)

TWAIFD_EFD Configures whether to erase the error counter of the data bit time.
O: Invalid
1: Erase
(WO)
```